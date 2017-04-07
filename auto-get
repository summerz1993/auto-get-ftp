#/bin/bash

echo "ftp file audto download start"

GET_DATE=`date -d '1 days ago' +%Y%m%d`
GET_DIR=/home/weihu/zg-ftp-file/txt-file
IP_ADDRESS=172.30.35.5
USER_NAME=rxc_ftp
USER_PWD=ZGXT_rxc_ftp!1
LOCAL_FTP=/usr/bin/ftp
FILE_NAME=*#$GET_DATE#*.txt

echo "clean GET_DIR start"
cd $GET_DIR
rm -fr *.txt

$LOCAL_FTP -n <<!
open $IP_ADDRESS
user $USER_NAME $USER_PWD
binary
lcd $GET_DIR
prompt off
mget $FILE_NAME

close
bye
!
exit 0
