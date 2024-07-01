# CMC
1、打开cmd（Windows）或者 Terminal终端（macOS）

2、执行

arp -a 192.168.1.1
得到MAC地址


第二步 开启Telnet
1、在浏览器中输入http:/192.168.1.1/cgi-bin/telnetenable.cgi?telnetenable=1&key=MAC值

2、此时，你应该看到“telnet开启”

第三步 获取超级密码
1、打开cmd（Windows）或者 Terminal终端（macOS）

2、执行
telnet 192.168.1.1
你应该看到login：

你应该看到这个
3、然后，在login:后面执行

admin
对话框会提示你输入密码

在Password:后面输入Fh@加上你获取的MAC的后6位，比如说我这里就是Fh@MAC后6位

这时，对话框会出现一个#

注：输密码的时候是没有显示的（密码保护机制），如果怕输错可以用记事本编辑好密码之后复制粘贴。粘贴时要用右键，不要用Ctrl-V！

4、执行

load_cli factory
show admin_name
show admin_pwd
对话框会显示

成功！
里面admin_name=后面的CMCCAdmin就是超级账户名，admin_pwd=后面的CMCCAdmin开头的一串就是超级密码

5、访问192.168.1.1，把账户名和密码输进去，就进入管理员模式
