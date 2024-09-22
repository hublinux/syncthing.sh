Linux版
一键安装syncthing
#获取适合您的操作系统的最新版本的 Syncthing

curl -s https://api.github.com/repos/syncthing/syncthing/releases/latest | grep browser_download_url | grep linux-amd64 | cut -d '"' -f 4 | wget -qi -

#解压Syncthing

tar xvf syncthing-linux-amd64*.tar.gz

#将二进制文件复制到 /usr/local/bin 目录

sudo cp syncthing-linux-amd64-*/syncthing  /usr/local/bin/

#检查 Syncthing 版本确认二进制文件已复制

syncthing --version

#启动syncthing服务

/usr/local/bin/syncthing  serve --gui-address=0.0.0.0:8384 > /dev/null 2>&1 &
