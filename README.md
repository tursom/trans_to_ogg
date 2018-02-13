# trans_to_ogg
transogg listfile [output dir]

需要安装mplayer和oggenc

将要转码的文件的路径全部储存在listfile中（可自定名称），使用本命令即可
[output dir]为输出的目录，默认为"out"

例：
./transogg list1 /tmp/music/ogg

ls *.mp3 2>/dev/null > /dev/shm/mp3filelist; ./transogg /dev/shm/mp3filelist; rm /dev/shm/mp3filelist
#批量转码mp3

ps：可将本脚本放入/usr/local/bin中，方便随时调用
