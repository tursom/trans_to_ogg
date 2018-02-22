# trans_to_ogg
将音频（视频）批量转码为ogg音频

transogg listfile [output dir]

需要安装ffmpeg

将要转码的文件的路径全部储存在listfile中（可自定名称），使用本命令即可
[output dir]为输出的目录，默认为"out"

例：
./transogg list1 /tmp/music/ogg

ls \*.mp3 2>/dev/null > "/dev/shm/mp3filelist$$"; transogg "/dev/shm/mp3filelist$$"; rm "/dev/shm/mp3filelist$$"
#批量转码mp3（中断此命令可引发内存泄漏，请关闭所有正在运行的此命令并手动删除"/dev/shm/mp3filelist*"以及"/dev/shm/transogg*"来释放内存）

ps：可将本脚本放入/usr/local/bin中，方便随时调用

#2018/2/23 更新

添加多线程功能
