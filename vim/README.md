# 整理关于vim插件、配置等内容

## color schema

在用户根目录下创建.vim文件夹，然后在里面建立colors文件夹，里面存放配色文件。
推荐使用配色molokai，可以直接使用别人的配置：https://github.com/tomasr/molokai.git
克隆仓库后把colors里的文件放到.vim目录下的colors目录下即可

## 插件

在用户目录下创建.vim文件夹，然后在里面建立bundle文件夹，这里存放vundle插件
建议使用插件管理器vundle进行管理：git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim

注意：对于coc插件，需要nodejs，在ubuntu上需要使用curl添加仓库以安装nodejs和yarn，再用yarn进行安装。步骤如下

1. 先利用vundle初步安装，此时会提示node不是可执行命令
2. 在终端使用"curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -"命令，和"echo 'deb https://dl.yarnpkg.com/debian/ stable main' | sudo tee /etc/apt/sources.list.d/yarn.list"命令添加yarn源
3. 再继续用终端使用"curl -sL https://deb.nodesource.com/setup_16.x | sudo -E bash -"命令添加nodejs源，**注意这里setup_16.x中的数字是想要的版本号，可以去nodejs官网查最新的LTS的主版本号是多少**
4. 此时应该自动执行了apt update命令（终端上会有显示），如果没有则自行执行一下。接着"sudo apt install yarn nodejs"进行安装
5. 进入coc插件的安装位置~/.vim/vim_plugged/coc.nvim（注意这里安装位置是看vimrc中对vundle的配置决定的，位于call vundle#begin('路径')）
6. 终端输入yarn install
7. 终端输入yarn build

## 配置文件

在用户根目录下建立./vimrc文件即可配置。
收录一位大佬的配置可以参考文件vimrc_zhihuDalao.txt（针对vundle略作调整）
