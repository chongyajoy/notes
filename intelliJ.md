#how to config mvn
.bash_profile
export M2_HOME=/usr/Local/apache-maven-*
export PATH=$PATH: $M2_HOME/bin
JAVA HOME=/Library/Java/JavaVirtualMachines/*/Contents

#config zsh
在Mac上配置Zsh（Z Shell）可以极大地提升你的终端使用体验，特别是通过使用插件和主题来增强功能和外观。下面是一步步如何在Mac上配置Zsh的指南：

步骤 1: 安装和设置Zsh为默认Shell
安装Zsh（如果尚未预装）：
大多数最新的Mac OS版本已经预装了Zsh。你可以通过在终端中运行zsh --version来检查是否已安装。如果需要安装或更新，可以使用Homebrew（如果已安装）：
bash
Copy code
brew install zsh
将Zsh设置为默认shell：
你可以通过以下命令设置Zsh为你的默认shell：
bash
Copy code
chsh -s /bin/zsh


步骤 2: 配置Zsh
编辑.zshrc文件：
Zsh的配置信息存储在家目录下的.zshrc文件中。你可以使用任意文本编辑器编辑这个文件。如果文件不存在，你可以创建它：
bash
Copy code
touch ~/.zshrc
open -a TextEdit ~/.zshrc
基本配置：
你可以在.zshrc文件中添加别名、环境变量等设置。例如，设置别名和环境变量：
bash
Copy code
alias ll='ls -lah'
export PATH="/usr/local/bin:$PATH"


步骤 3: 安装Oh My Zsh
Oh My Zsh是一个流行的开源框架，用于管理Zsh的配置。它包含了许多插件和主题，可以简化和美化你的Shell环境。

安装Oh My Zsh：
通过curl或wget可以安装Oh My Zsh：
bash
Copy code
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
或者使用wget：
bash
Copy code
sh -c "$(wget -O- https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
配置主题和插件：
Oh My Zsh的配置文件是~/.zshrc。你可以在这个文件中更改主题（通过修改ZSH_THEME变量）和启用插件（通过添加插件到plugins=(...)数组中）。
主题：例如，设置ZSH_THEME="agnoster"。
插件：例如，添加常用插件：plugins=(git z sudo)

步骤 4: 应用更改
每次编辑完.zshrc文件后，你需要通过以下命令使更改生效：

bash
Copy code
source ~/.zshrc