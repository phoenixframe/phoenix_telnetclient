# phoenix_telnetclient
phoenixframework平台的一个模块，用于对socketserver进行操作<br>
<br>
支持以下命令：<br>
1.!setname - setdisplayname,format: !setname=your name<br>
2.!showusers - show all users<br>
3.!showorders - show all instruct<br>
4.!start - start program ex:!start iexplore.exe<br>
5.!shell - start shell command ex:!shell sh test.sh 111<br>
6.!export - export a file ,if filepath have block,use '^' instead,ex:!export e:\\test\\test.txt isappend(true/false) datas<br>
7.!file - return a file content,ex:!file test.txt UTF-8<br>
8.!runsh - return Linux or Windows command result,ex:!runsh svn info<br>
9.!addfilewatch - add a file watching dog,max:100,ex:!addfilewatch a.log<br>
10.!getwatchstring - return file watch string,ex:!getwatchstring a.log<br>
11.!stopfilewatch - stop a file watching dog,ex:!stopfilewatch a.log<br>
12.!scanfile - scanfile a file by keyword,ex:!scanfile a.log test 1,1:contains keyword,0:not contains<br>
13.exit - exit client,ex:exit<br>
<br>
该工具用于部署到远程机器上，既是客户端也可以作为服务端，可以通过telnet命令或socket客户端给它发送命令，它可以完成一系列远程操作。<br>
支持两种启动模式：<br>
1.java -jar TCPServer.jar 7788 ,这种模式接收一个命令一个操作方式<br>
2.java -jar TCPServer.jar 7788 monitor ，这种模式用于对一个对象持续监控，并每秒通知一次客户端，客户端连接之后，除非客户端发送停止命令，否则保持一直连接。<br>
还可以作为简单的聊天工具~~
