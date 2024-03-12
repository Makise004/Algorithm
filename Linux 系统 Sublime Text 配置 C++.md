## Linux 系统 Sublime Text 配置 C++ 

### build system 配置

```
sudo apt-get update
sudo apt-get install gcc
gcc -v
```

```json
{
    "cmd" : ["g++", "-std=c++14", "$file_name", "-o", "${file_base_name}", "-lm", "-Wall"],
    "file_regex": "^(..[^:]*):([0-9]+):?([0-9]+)?:? (.*)$",
    "selector" : "source.c, source.c++",
    "shell":false,
    "working_dir" : "$file_path",

    "variants":
    [
        {
            "name": "My_Run",
            "cmd": ["gnome-terminal", "-e", "bash -c \"'${file_path}/${file_base_name}' ; read -p '\nPress any key to continue...'\""]
        }
    ]
}
```

或者

```json
{
  "cmd":["bash", "-c", "g++ -std=c++14 -Wall '${file}' -o '${file_path}/${file_base_name}' && '${file_path}/${file_base_name}'"],
  "file_regex": "^(..[^:]*):([0-9]+):?([0-9]+)?:? (.*)$",
  "working_dir": "${file_path}",
  "selector": "source.c, source.c++",
  "variants":
  [
    {
      "name": "Run",
      "cmd": [ "bash", "-c", "g++ -std=c++14 '${file}' -o '${file_path}/${file_base_name}' && '${file_path}/${file_base_name}'"]
    },
    
    {  
        "name": "c_RunInCommand",
        "cmd": [ "gnome-terminal","--","bash", "-c", "g++ -std=c++14 '${file}' -o '${file_path}/${file_base_name}' && '${file_path}/${file_base_name}' && read -p '\nPress any key to continue...' "]
    }
  ]
}

```