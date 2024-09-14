# 环境搭建
## 安装 python
brew 安装 python，安装 python 时会自动安装 pip.  
检验是否成功安装
```
>> python3 --version
>> pip3 --version
```
运行 hello world 验证
```python
print("HelloWorld")
```
```
>> python3 test.py
```

## 使用虚拟环境
pip 是 python 的包管理工具，但是使用 pip 安装依赖包可能会与系统的包管理器产生冲突
```
error: externally-managed-environment

× This environment is externally managed
╰─> To install Python packages system-wide, try apt install
    python3-xyz, where xyz is the package you are trying to
    install.
```
● 可以直接使用系统的包管理器安装，比如 brew  
● 创建虚拟环境，在这个虚拟环境中安装，不会影响到系统级别的环境  
● 使用 pipx 安装

### venv
venv 是 Python 的内置模块，无需单独安装。  
venv 创建的是轻量级的虚拟环境，只适用于管理 Python 包，不适合管理非 Python 依赖项。  
适用于纯 Python 项目。  
```
-- 使用 venv 创建虚拟环境，虚拟环境路径为 当前路径/path/to/venv
>> python3 -m venv path/to/venv

-- 启动虚拟环境
>> source path/to/venv/bin/activate

-- 在虚拟环境中安装依赖包 requests
>> python3 -m pip install requests

-- 退出此虚拟环境
>> deactivate
```

### Conda
Conda 是一个跨平台的包管理工具，可以在 Windows, Linux, macOS 等操作系统上使用。  
Conda 比 venv 更强大，可以管理 Python 包以及其他语言的包。  
更适合复杂的项目，尤其是涉及到多种语言或非 Python 依赖项的项目。


## 安装机器学习基础库 sklearn
```
-- 启动虚拟环境
source path/to/venv/bin/activate

-- 在虚拟环境中安装 sklearn
python3 -m pip install scikit-learn
```


## 安装 Pycharm
官网安装 Pycharm，激活：https://www.idejihuo.com/  
创建代码仓库，选择 Python Interpreter  
1. 选择创建新的虚拟环境
2. Base Python 版本选择之前用 homebrew 安装的 Python 版本
3. 路径默认为当前项目路径/venv
