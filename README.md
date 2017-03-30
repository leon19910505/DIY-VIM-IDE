# DIY-VIM-IDE
打造vim， diy 自己的ide
Install
下载 vundle 管理工具
 git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
 
 下载我的vimrc 文件，并改为 .vimrc 
 或者创建 ~/.vimrc 文件，copy 我的配置
 mac 默认在用户目录下，也就是~/   ,是用户级别的配置，但是会覆盖全局， 全局的.vimrc　在etc 下面
 

 值得一提的是，当尝试使用source .vimrc 的时候会报错，可以不用管，确保vendle的目录正确， 然后运行就可以了（在source这里纠结了一晚上，实在强迫症source，可以！source）
 
 然后打vim运行， :PluginInstall   进行安装插件， over
