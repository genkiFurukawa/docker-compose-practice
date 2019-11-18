FROM mysql:5.7
MAINTAINER genki.furukawa@gmail.com
# 指定の場所にログを記録するファイルを作る
RUN touch /var/log/mysql/mysqld.log
# my.cnf配置
ADD ./conf.d/my.cnf /etc/mysql/my.cnf
RUN chmod 644 /etc/mysql/my.cnf