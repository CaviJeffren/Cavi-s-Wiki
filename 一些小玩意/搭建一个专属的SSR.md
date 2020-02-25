嗯哼？
本文为记录自己搭建SSR的过程，以免过后重装的时候忘掉了又要百度╮(╯▽╰)╭
1、拥有一个服务器，不记了。
2、使用xshell登录服务器：
    使用xshell登录服务器后命令行输入会出现卡顿，可使用vi /etc/ssh/sshd_config修改dns设置，将UseDNS yes改为UseDNS no。此步骤为安装ssr前置条件，否则可能会出现ssr无法连接的问题。
3、安装ssr：
    使用wget --no-check-certificate https://freed.ga/github/shadowsocksR.sh; bash shadowsocksR.sh安装ssr，并完成密码和端口设置。
    安装完成后记录ssr信息，使用shadowsocksR进行连接，此时ssr已搭建完成。
4、可使用锐速对服务器进行加速：
    安装锐速需要降级内核，若为CentOS7 x64系统，使用wget --no-check-certificate -O rskernel.sh https://raw.githubusercontent.com/hombo125/doubi/master/rskernel.sh && bash rskernel.sh
指令降级内核，降级完成后服务器将重启。
    系统重启成功后重新连接，输入yum install net-tools -y && wget --no-check-certificate -O appex.sh https://raw.githubusercontent.com/0oVicero0/serverSpeeder_Install/master/appex.sh && bash appex.sh install
指令安装锐速，安装过程中需进行三次配置选择，选择分别为nyy，一路回车，锐速安装完毕。

That's all.
