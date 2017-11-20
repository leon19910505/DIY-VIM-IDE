# DIY-VIM-IDE
打造vim， diy 自己的ide
# Install
 * 下载 vundle 管理工具
 ```
   git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
 ```
 * config 
   mac 默认在用户目录下，也就是~/   ,是用户级别的配置，但是会覆盖全局， 全局的.vimrc　在etc 下面
 ```
  vim ~/.vimrc
 ``` 
   copy下面的配置
 ```vim
   set nocompatible              " 去除VI一致性,必须
   filetype plugin  off                  " 必须

   " 设置包括vundle和初始化相关的runtime path
   set rtp+=~/.vim/bundle/Vundle.vim
   call vundle#begin()

   " 让vundle管理插件版本,必须
   Plugin 'VundleVim/Vundle.vim'
   Plugin 'altercation/vim-colors-solarized'
   Plugin 'scrooloose/nerdtree'
   Plugin 'kien/ctrlp.vim'
   Plugin 'tomasr/molokai'
   call vundle#end()            " 必须
   filetype plugin indent on    " 必须 加载vim自带和插件相应的语法和文件类型相关脚本
   " 忽视插件改变缩进,可以使用以下替代:
   "filetype plugin on
   " 简要帮助文档
   " :PluginList       - 列出所有已配置的插件
   " :PluginInstall    - 安装插件,追加 `!` 用以更新或使用 :PluginUpdate
   " :PluginSearch foo - 搜索 foo ; 追加 `!` 清除本地缓存
   " :PluginClean      - 清除未使用插件,需要确认; 追加 `!` 自动批准移除未使用插件
   "
   " 查阅 :h vundle 获取更多细节和wiki以及FAQ
   " 将你自己对非插件片段放在这行之后
   "
   set cursorline
   set incsearch " 输入搜索内容时就显示搜索结果
   set hlsearch " 搜索时高亮显示被找到的文本
   set modelines=0
   set backspace=2
   set number
   "syntax on " 自动语法高亮
   " 打开javascript折叠
   let b:javascript_fold=1
   "自动打开nerdtree
   "autocmd vimenter * NERDTree

   "Nerd Tree
   let NERDChristmasTree=0
   let NERDTreeWinSize=40
   let NERDTreeChDirMode=2
   let NERDTreeIgnore=['\~$', '\.pyc$', '\.swp$']
   let NERDTreeShowBookmarks=1
   "autocmd vimenter * if !argc() | NERDTree | endif " Automatically open a NERDTree if no files where specified
   autocmd bufenter * if (winnr("$") == 1 && exists("b:NERDTreeType") && b:NERDTreeType == "primary") | q | endif " Close vim if the only window left open is a NERDTree
   nmap <F5> :NERDTreeToggle<cr>

   ":CtrlP 快捷键
   nmap <F6> :CtrlP<cr>
   "主题配色
   syntax enable
   "set background=dark
   "colorscheme solarized
   colorscheme molokai
   set cursorline
   highlight CursorLine   cterm=NONE ctermbg=white ctermfg=black guibg=NONE guifg=NONE
   highlight CursorColumn cterm=NONE ctermbg=white ctermfg=black guibg=NONE guifg=NONE

 ```
 * 然后输入安装命令，enter 进行安装
 ```
      :PluginInstall
 ```
# 刷新vim配置 
```
 source ~/.vimrc
```
