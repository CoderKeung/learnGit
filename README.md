- **Git配置文件目录**

```bash
# --system 写入系统文件目录 /etc/gitconfig 
# --global 写入本地文件目录 ~/.gitconfig 或 ~/.config/git/config 
# --local  写入本地仓库目录 
git config --list --show-origin 
```

- **设置用户信息**

```bash
git config --global user.name "UserName"
git config --global user.email "UserEmail@gmail.com"
```
	
- **设置默认打开文本编辑器**

```bash
git config --global core.editor nvim
```

- **检查配置**

```bash
git config --list
```

- **精简检查Git状态**

```bash
git status -s # git status --short
```

- **忽略文件**
	- 仓库目录中创建  `.gitignore` 文件，语法如下：
	-  [所有语言的.gitignore文件](https://github.com/github/gitignore) 

```bash
# 注释内容与空行被自动忽略
*.a # 忽略所有以 .a 为后缀的文件
!lib.a # 跟踪所有 lib.a 文件
/LIB # 只忽略当前目录的 LIB 文件
LIB/ # 忽略所有的 LIB 目录
# 忽略 doc/notes.txt，但不忽略 doc/server/arch.txt
doc/*.txt
# 忽略 doc/ 目录及其所有子目录下的 .pdf 文件
doc/**/*.pdf
```

- **查看将要提交的修改**
	- `git diff` 本身只显示尚未暂存的改动

```bash
# git diff --cached
git diff --staged
```

