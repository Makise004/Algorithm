```c++
// 随机化选点  + 时间戳优化
int num;  // 时间戳优化

inline int bfs2(int sx, int sy, int c1, int c2){
    int cnt = 0;
    queue<pii> q;
    q.emplace(sx, sy);
    vis[sx][sy] = ++ num;

    while(q.size()){
        auto [x, y] = q.front();
        q.pop();

        cnt ++ ;

        for(int k = 0; k < 4; k ++ ){
            int nx = x + dx[k], ny = y + dy[k];
            if(nx < 1 || nx > n || ny < 1 || ny > n) continue;
            if(vis[nx][ny] == num || (g[nx][ny] != c1 && g[nx][ny] != c2)) continue;
            q.emplace(nx, ny);
            vis[nx][ny] = num;
        }
    }

    return cnt;
}

int main(){
    ios;

    read(n);
    for(int i = 1; i <= n; i ++ )
        for(int j = 1; j <= n; j ++ ) read(g[i][j]);

    ......

    // task2 随机化
    srand(unsigned(time(NULL)));
    for(int t = 1; t <= 59900; t ++ ){
        if((double)clock() / CLOCKS_PER_SEC >= 0.9) break;
        int i = rand() % n + 1, j = rand() % n + 1;
        for(int k = 0; k < 4; k ++ ){
            int nx = i + dx[k], ny = j + dy[k];
            if(nx < 1 || nx > n || ny < 1 || ny > n || g[nx][ny] == g[i][j]) continue;
            res2 = max(res2, bfs2(i, j, g[i][j], g[nx][ny]));
        }
    }

    ......

    return 0;
}
```