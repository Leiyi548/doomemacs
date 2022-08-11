# doom安装和使用

- [doomemacs-docs](https://github.com/doomemacs/doomemacs/blob/master/docs/index.org)
- [doomemacs-github](https://github.com/doomemacs/doomemacs/tree/master)

## 1. 安装

```sh
git clone --depth 1 https://github.com/doomemacs/doomemacs ~/.emacs.d
~/.emacs.d/bin/doom install
```

## 2. 常用SPC命令

### 2.1. SPC f：文件操作

f：打开/查找文件
d：打开目录（Dired）
s：保存文件
r：最近文件列表
y：拷贝当前文件名（路径）
C：大写，拷贝当前文件（询问目标位置）
D：大写，删除当前文件
R：大写，重命名/移动文件
S：另存

### 2.2. SPC b：缓冲区操作

- b：缓冲区列表
- n/[：切换到前一个缓冲区
- p/]：切换到后一个缓冲区
- s：保存当前缓冲区（使用命令和 SPC f s 可能不同）
- S：保存所有缓冲区
- d/k：关闭当前缓冲区
- O：关闭其他缓冲区
- K：关闭所有缓冲区
- z：隐藏/最小化当前缓冲区
- Z：关闭所有隐藏的缓冲区

### 2.3. SPC w：窗口操作
- v：垂直分割窗口
- s：水平分割窗口
- h/j/k/l：在窗口间移动光标（激活编辑窗口）
- w/W：向前/后窗口移动光标（比hjkl顺手）
- H/J/K/L：窗口位置置换/移动命令
- T：从新的窗口打开这个文件
- q：关闭当前窗口
- n：和s作用相同
- m：最大化当前窗口（全部、水平或垂直最大化，有提示）
- =：等分所有窗口（其他调整大小的命令不大实用，不如自己绑定按键）

### 2.4. SPC o：打开其他程序/界面

- p：打开/关闭treemacs目录树 （需要开启 treemacs）
- T：打开终端 （需要开启 vterm）
- f：打开一个新窗口（显示当前缓冲区内容，等于在多窗口中同时编辑一个文件，内容同步！）
- a：org agenda (SPC a A 等于 SPC o a a)


### 2.5.SPC t：切换（toggle）
- l：行号
- b：字体模式
- F：全屏模式等

### 2.6. SPC h：帮助（help）

- t：改变主题
- b+b：搜索keybinding
- r：reload

### 2.7. SPC p：Project
- t：list project todos
- s：save project files

### 2.8. SPC q: Quit

-q：quit emacs
-Q: quit emacs not save


## 3. 基础设置

重新加载 doomemacs配置 `~/.emacs.d/bin/doom sync`

### 3.1. 改变字体

``` emacs-lisp
;; Font Setting
(setq doom-font (font-spec :family "FiraCode Nerd Font" :size 18)
      doom-variable-pitch-font (font-spec :family "FiraCode Nerd Font" :size 18)
      doom-big-font (font-spec :family "FiraCode Nerd Font" :size 24))
(after! doom-themes
  (setq doom-themes-enable-bold t
        doom-themes-enable-italic t))
(custom-set-faces!
  '(font-lock-comment-face :slant italic)
  '(font-lock-keyword-face :slant italic))
```

## 4. whichkey 使用

这个 winchkey 和vim上的差不多，都是提示你键盘绑定，可是它显示的不多，所以我们想要得到这个键位对应更多的信息，那么我们就需要使用 `C-h` 然后就会在这个层次上进行搜索获得信息。

## 相关项目

- [github-spacemacs](https://github.com/syl20bnr/spacemacs)
- [spacemac-doc](https://develop.spacemacs.org/doc/DOCUMENTATION.html)
