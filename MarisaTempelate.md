
```c++
// *****************************************
// *  @brief   
// *  @author  神经大条的偷心大盗
// *  @file    .cpp
// *  @version 1.0
// *****************************************
#include<iostream>
#include<cstdio>
#include<cstring>
#include<string>
#include<algorithm>
#include<vector>
#include<queue>
#include<deque>
#include<stack>
#include<map>
#include<set>
#include<unordered_map>
#include<unordered_set>
#include<bitset>
#include<cmath>
#include<functional>
using namespace std;

template <typename T> 
inline void read(T &x) {
    int f = 1; x = 0; char s = getchar();
    while (s < '0' || s > '9') { if (s == '-') f = -1; s = getchar(); }
    while (s <= '9' && s >= '0') x = x * 10 + (s ^ 48), s = getchar();
    x *= f;
}

inline void sread(string &s){
    char ch = getchar();
    while(ch == ' ' || ch == '\n' || ch == '\t') ch = getchar();
    while(ch != ' ' && ch != '\n' && ch != '\t') s += ch, ch = getchar();
}

typedef long long ll;
typedef unsigned long long ull;
typedef pair<int, int> pii;
typedef pair<ll, ll> pll;
typedef pair<int, pii> piii;
typedef pair<double, double> pdd;
typedef pair<char, int> pci;
typedef pair<string, int> psi;
#define PI acos(-1.0)
#define fi first
#define se second
#define pb push_back
#define pf push_front
#define qb pop_back
#define qf pop_front
#define eb emplace_back
#define MP make_pair
#define LB lower_bound
#define UB upper_bound
#define umap unordered_map
#define uset unordered_set
#define pque priority_queue
#define all(a) begin(a), end(a)
#define rall(a) rbegin(a), rend(a)
#define mst(a, x) memset(a, x, sizeof(a))
#define mcp(a, b) memcpy(a, b, sizeof(b))
#define lowbit(x) x & (-x)
#define ios ios::sync_with_stdio(false), cin.tie(0), cout.tie(0)
inline int bitcnt(ll x) {int res = 0; while(x) x = x & (x - 1), res ++ ; return res;}
inline ll gcd(ll a, ll b) {return b ? gcd(b, a % b) : a;}
inline ll qmi(ll a, ll b, int p) {ll res = 1; a %= p; while(b){if(b & 1) res = (res * a) % p; b >>= 1, a = (a * a) % p;} return res;}
const int dx[8] = {1, -1, 0, 0, 1, -1, 1, -1};
const int dy[8] = {0, 0, 1, -1, -1, 1, 1, -1};
const double eps = 1e-6;
const int inf = 0x3f3f3f3f, mod = 1e9 + 7;
const ll INF = 0x3f3f3f3f3f3f3f3f;
const int N = 1e5 + 10, M = (N << 1);



int main(){
    ios;

    int T = 1; // cin >> T;
    while(T -- ){

    }

    return 0;
}
```