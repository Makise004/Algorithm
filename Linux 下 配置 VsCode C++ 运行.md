## Linux 下 配置 VsCode C++ 运行

### 下载C/C++ 插件

### 确保安装gcc

```
sudo apt update # 更新软件包源 
sudo apt-get install build-essential gdb
gcc -v
```


### 插件安装

<div>
    <img src="C:\Users\user\Desktop\dasda.png" /> 
</div>

###  编译运行

点击右上角的三角形按钮就能运行程序。

有的时候这时会发现不能正常运行程序,这时候可能需要点击左下角的齿轮Manage并选择(settings)，搜索code runner run in terminal并将搜索出的这一项勾上。

输入code runner，找到clear Previous Output选项。

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "C/C++",
            "type": "cppdbg",
            "request": "launch",
            "program": "${fileDirname}/${fileBasenameNoExtension}",
            "args": [],
            "stopAtEntry": false,
            "cwd": "${workspaceFolder}",
            "environment": [],
            "externalConsole": false,
            "MIMode": "gdb",
            "preLaunchTask": "compile",
            "setupCommands": [
                {
                    "description": "Enable pretty-printing for gdb",
                    "text": "-enable-pretty-printing",
                    "ignoreFailures": true
                }
            ]
        }
    ]
}
```