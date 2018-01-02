#Vim

[vim class1 -basic motions and commands](https://www.youtube.com/watch?v=Nim4_f5QUxA)    
[vim class2](https://www.youtube.com/watch?v=2pqipq-UEwQ)
宏

- g+g (go to beginning)    
- G(jump to the end of file)
- shift+z+z (= Esc+ : +wq)
- Esc+q+! (force quit)
- Esc(ctrl + c)

##Mode
- Insert
- Normal
- Command(:w filename - save the file)
- Visual

Insert -> Normal : ESC/Ctrl+[
Insert -> Command : (Insert -> Normal) -> :
Command -> Normal : Enter

##Pen to the page 

**(i=insert、a=append、r=replace)**
   
- i - Enter insert mode at cursor
- I - Enter insert mode at first non-blank character
- a - Enter insert mode after cursor
- A - Enter insert mode at the end of the line

- o - Enter insert mode on the next line
- O - Enter insert mode on the previous line


- s - Delete character under cursor and enter insert mode
- S - Delete line and begin insert at beginning of same line


- C - Delete from cursor to end of line and begin insert

##Scanning the canvas

------k    
h-----------L   
------j

*2j(move down two lines)*

##Basics
- w - Forward to the beginning of next word(Example, cw-change word, diw-delete word)
- W - Forward to the beginning of next WORD(after whiteSpace)
- b - Backward to the next beginning of a word
- B - Backward to the next beginning of a WORD
- e - Forword to the next end of word
- E - Forword to the next end of WORD
- 0/home - Move to the zeroth character of the line
- $ - Move to the last character of the line
- ^ - Move to the first non-blank character of the line
- H - 光标移到当前屏幕最上方行的第一个字符
- M - 光标移到当前屏幕最中间行的第一个字符
- L - 光标移到当前屏幕最下方行的第一个字符
- G - 到此文件最后一行
- nG - 移动到第n行
- gg - 相当于1G, 即回到行首
- n+Enter - 光标下移n行
- 

1. [n]f<o> - Forward until (nth)(o) (Inclusive)
2. [n]F<o> - Backward until (nth)(o) (Inclusive)
3. [n]t<o> - Forward until (nth)(o) (Exclusive)
4. [n]T<o> - Backward until (nth)(o) (Exclusive)

#Search：
- / search forward
- ? search backward
- '*' 聚焦当前cursor forword(bounded)
- n - next result, forward
- N - next result, backward
- '#' 当前cursor下的指令 backward(bounded)

*:set ignorecase -- will search ignore case*
*/\c forward -- will case insensitive to find forward*

#Replace
- :%s/foo/bar/g (在当前文件查找foo替换成bar)
- :s/foo/bar/g (在当前行查找foo替换成bar)
- :%s/foo/bar/gc
- :%s/\<foo\>/bar/gci/I (foo only whole words, ask for confirmation, case insensitive/sensitive)
- n1,n2s/foo/bar/g（在n1行n2行查找foo替换成bar）

##Copy/Paste
- y - Yank. Example: 2yy(copy current two lines)
- p - 将已复制的粘贴到光标所在下一行
- P - 将已复制的粘贴到光标所在上一行
- v - visual selection

##Delete：
- x/X 删除光标处字符, 光标前的字符
- dd（删除所在行） 
- ndd（删除光标所在行以下n行）
- d1G（删除光标所在行到第一行所有数据）
- dG（删除光标所在行到最后一行所有数据）
- d$（删除光标所在行到同行最后一个字符）
- d0（删除光标所在行到同行第一个字符）
- :1,8d(删除1~8行) OR VggGd

##Undo
- u 恢复前一次所做的删除
- ctrl+R (undo change)
- .（重复上一个操作）

##Scroll
- ctrl+f(屏幕向上滚动一页)
- ctrl+b(屏幕向下滚动一页)
- ctrl+u(屏幕向下滚动半页)
- ctrl+d(屏幕向下滚动半页)

##i f b
- i 向两侧扩张选择能match的string，Example，(, {, [
- f/t 向左侧扩张选择, cursor就在当前character下/前
- b 向右侧扩展选择
Example：yiw(delete word)


##vim symmary |
| 动词 | y | p | d |
| :--- | ---: | :---: | :---: |
| 操作 | i | f | b | 
| 选择 | （ | ）| sentence（.） | 
| 选择 | { | } | paragraphs(empty line) |
| 选择 | [[ | ]] | section |
| format | = |

##convenient
- zz center window
- "+ y copy to system clipboard
- * (search word)
- :reg (look history copy record)
- % (go to last matched braket)



####VS
- ctrl+'-'(last cursor)
- ctrl+y(undo change in vs)

####System
- cmd+ctrl+f (maximum screen)








