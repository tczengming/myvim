# myvim

<Prev>
希望能给大家做一个参考。插件用bundle (也有人叫vundle)管理的，推荐大家使用bundle，插件安装升级很方便

只要一个vimrc

先安装bundle

git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle

然后可下载我的.vimrc替换你的.vimrc

git clone https://github.com/tczengming/myvim.git      

下载后用myvim/myvimrc替换你的.vimrc (可自行修改其内容)

然后在vim中执行

BundleInstall!    就可以自动地更新安装插件,不用再手动去网上一个个下最新包了。

缷载插件  :BundleClean


"Bundle 'Valloric/YouCompleteMe这个我注释了，建议大家改成Bundle 'Valloric/YouCompleteMe，此插件用于自动补全很强大，

开了后还要手动编译它，

cd ~/.vim/bundle/YouCompleteMe

./install.py --clang-completer

cp ~/.vim/bundle/YouCompleteMe/third_party/ycmd/cpp/ycm/.ycm_extra_conf.py ~/

这样才算安装完YouCompleteMe简称ycm

需要额外安装ctags, cscope这两个命令，用于生成tags，方便代码跳转查找：
ctags -R --c++-kinds=+p --fields=+iaS --extra=+q .
--c++-kinds=+p  : 为C++文件增加函数原型的标签
--fields=+iaS   : 在标签文件中加入继承信息(i)、类成员的访问控制信息(a)、以及函数的指纹(S)
--extra=+q      : 为标签增加类修饰符。注意，如果没有此选项，将不能对类成员补全
</Prev>
