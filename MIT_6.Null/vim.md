# vim
- `i` 插入(insert)模式
- `o` (open)向下方新的一行再进入插入模式
  - `O` 向上方插入新的一行
- `R` 替换(replace)模式
- `:` 命令行式
  - `:q` 退出(quit) （关闭窗口）
  - `:w` 保存(write) （写）
  - `:wq` 保存然后退出
- `:e` {文件名} 打开要编辑(edit)的文件
- `:ls` 显示打开的缓存
- `:help` {标题} 打开帮助文档
- `:help :w` 打开 :w 命令的帮助文档
    
## 删除
- `x` 删除一个字符
  - `dd` 删除整行(delete)
  - `dw` 删除一个词
  - `cd` 删除整行并进入插入状态(change)
  - `10dd` 删除 10 整行
- `s` 替换字符(删除字符并且进入插入模式)  
## 撤销与恢复
- `u` 撤销
  - `ctrl+r`恢复撤销
  
## 移动
- 基本移动: `hjkl` （左， 下， 上， 右）
- 词： `w` (word)（下一个词）， `b` (back)（返回词初）， `e` (end)（前进到词尾）
- 跳转到第9行：`:11`
- 行： `-2` （行初）， `^` （第一个非空格字符）， `$` （行尾）
- 屏幕： `H` （屏幕首行）， `M` （屏幕中间）， `L` （屏幕底部）
- 翻页： `Ctrl-u` （上翻）， `Ctrl-d` （下翻）
- 文件： `gg` （文件头）， `G` （文件尾）
- 找当前行中的 d,e,f: `fd` `fe`
- `%` (找到配对，比如括号或者 /* */ 之类的注释对)

## copy and paste
使用 Visual 模式来选择文本(在 Visual 模式可以使用移动快捷键)
- `v` 字符可视化(visual)模式
  - `C-v`块可视化模式
  - `Ctrl+v` 进入行可视化模式                 

### 复制
- `y` (copy) 复制
  - `yy` 复制当前行
  - `yw` 复制这个词
### 粘贴
- `p` (paste) 粘贴(在光标位置后)
  - `P` 在光标位置前粘贴
  - `10p` 粘贴 10 次 
  
### 剪贴
- `d` 在 Visual 模式下对选定文本按 `d` 就是剪切
### 改变字符大小写
- `~`

### 复制粘贴与 Windows 的交互
- vim有12个粘贴板，分别是 `0、1、2、...、9`、`a`、`“`、`＋`
  - `"1yy` 复制当前行存在 1 号剪贴板
    - `"1p` 粘贴 1 号剪贴板的内容    
  - `+` 是系统剪切板，可以将其与内部和外部交互
    - `"+yy` 复制 vim 中的当前行的内容，可以在 Windows 用 Ctrl + V 粘贴
    - `"+p` 粘贴从 Windows 复制的内容
  - `wsl` 中 vim 与 系统剪切板 的交互
    - `:w !clip.exe`
  
## 搜素
- `/111` 搜素111
- `n`/`N` 导航(navigation)匹配
  - `n` 下一个
  - `N` 上一个
  
## 多窗口
-  用 `:sp` / `:vsp` 来分割窗口
-  同一个缓存可以在多个窗口中显示。

### 窗口命令
- `ctrl+w s`     水平分割窗口
- `ctrl+w w`     切换窗口
- `ctrl+w q`     退出当前窗口(由于同时有多个文件，此命令不会影响其他窗口)
- `ctrl+w v`     垂直分割窗口
- `:sh`          打开 terminal/shell

## 计数
数字+命令，会执行该命令若干次
- `5j` 下移五行

## 修饰词
- `i` 表示内部(inside)
  - `ci(` 改变当前括号的内容
- `a` 表示内部+字符(around)
  - `da'` 删除单引号内部的内容，包括单引号

##

