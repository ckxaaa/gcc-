#安装bzip2  
1：获取bzip2安装包并且解压  
前往: https://sourceforge.net/projects/bzip2/files/latest/download 下载安装包  
tar xf bzip2-1.0.6.tar.gz  
cd bzip2-1.0.6  
make -f Makefile-libbz2_so  
make && make install  
#安装C++库  
centos系统：  
yum install glibc-headers gcc-c++ -y  
Ubuntu系统:  
apt-get install build-essential g++ -y  

#升级gcc版本  
手动源码安装  
1：获取gcc安装包并且解压  
wget http://ftp.gnu.org/gnu/gcc/gcc-8.2.0/gcc-8.2.0.tar.gz  
tar xf gcc-8.2.0.tar.gz  
cd gcc-8.2.0  
2：下载、配置、安装依赖库  
./contrib/download_prerequisites  
3：建立一个目录供编译出的文件存放  
mkdir gcc-build-8.2.0  
cd gcc-build-8.2.0  
4：生成Makefile文件  
../configure -enable-checking=release -enable-languages=c,c++ -disable-multilib  
5：编译：make   
6:安装：make install  
7:查看版本：gcc --version  


