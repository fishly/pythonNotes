## python中的io操作
  介绍基础的输入输出I/O操作

## python 输出
  1) print
     标准屏幕输出.





## python 输入
   1)raw_input(prompt)
     标准输入读取一行,并返回一个字符串
   2)input(prompt)
     input输入的是一个python表达式,若是要输入string类型的数据,则需要加上引号.




## python文件操作

1)操作流程
  - 需要先打开一个文件,创建一个file对象. file1= open(file_name,access_mode,buffering)
    1.file_name:访问文件
    2.access_mode:访问权限设置.默认为只读(r)
    3.buffering:寄存设置
    文件访问模式:
    r :只读,默认模式
    rb:二进制格式打开一个文件只读
    r+:读写模式
    rb+:二进制读写模式
    w:写模式,若已经存在则覆盖,不存在,创建新文件
    wb:二进制写入模式,若已经存在则覆盖,不存在,创建新文件
    w+:读写模式.若已经存在则覆盖,不存在,创建新文件
    wb+:二进制读写.若已经存在则覆盖,不存在,创建新文件
    a:追加模式,如果该文件已存在，文件指针将会放在文件的结尾。如果该文件不存在，创建新文件进行写入。
    ab:二进制追加模式,如果该文件已存在，文件指针将会放在文件的结尾。如果该文件不存在，创建新文件进行写入。
    a+:读写模式追加,如果该文件已存在，文件指针将会放在文件的结尾。如果该文件不存在，创建新文件进行写入。
    ab+:二进制读写追加模式,如果该文件已存在，文件指针将会放在文件的结尾。如果该文件不存在，创建新文件进行写入。

    File文件的基本属性:
    file.closed 是否已经关闭文件,true已经关闭,false未关闭.
    file.mode   file的访问模式
    file.name   文件名称
    file.softspace  如果用print输出后，必须跟一个空格符，则返回false。否则返回true

2)文件操作

  - 写操作
    write()方法可将任何字符串写入一个打开的文件。需要重点注意的是，Python字符串可以是二进制数据，而不是仅仅是文字。write()方法不会在字符串的结尾添加换行符('\n')：

  - 读操作
    read()操作,可以通过read()读取所有的内容,也可以通过file.read(length)指定每次读取的长度,读取后指针后移.
    readline()操作,按行读取
  - 文件当前位置获取
    file.tell()获取文件的指针指向的位置,返回数字.
  - 文件关闭
    file.close() 文件关闭操作.
  - 文件指针位置
    file.seek(0)重定位到文件开头.
  - 文件重命名
    os.rename(file1,file2)
  - 文件删除
     os.remove(file_name)
  - 获取当前工作目录
    os.getcwd()
  - 更改当前目录名称
    os.chdir("newdir")
  - 删除目录
    os.rmdir('dirname')


