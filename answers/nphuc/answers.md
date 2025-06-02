answer ?1:
 	awk '$9 ~ /^4/ {print $1}' access.log | sort | uniq -c | sort -nr | head -1\
	2 192.168.1.1
	Tai cot 9 in ra IP co ma loi 404, sap xep va dem so loi xuat hien, lay IP co nhieu loi nhat

answer ?2:
	awk -F, '$3 != "/bin/bash" {print $1 "," $2}' users.csv
	
	user2, User Two
	user3, User Three
	
	Dung dau phay lam phan cach va in ra ket qua cot thu 1 va thu 2 khi cot thu 3 khac /bin/bash	

answer ?3:
Khi su dung "sed" thay the 1 chuoi va tao ra 1 file moi config1.conf de so sanh voi file goc	
	3c3
	< port=8080
	---
	> port=8088

answer ?5:
	awk '{print $3}' error.log | sort | uniq -c | sort -nr
   	1 WARNING
   	1 ERROR
	In ra cot thu 3 co chua ma loi, dem so lan moi loi xuat hien vaf sap xep

answer ?6:
	htop hoac top
	Se hien thi cac tien trinh dang chay va tu do co the monitoring xem tien trinh nao dang su dung nhieu CPU nhat
	Cau hoi nay chua hieu ro cu the va chua biet cach tim tien trinh nao dang duoc su dung nhieu CPU nhat cua file trong 1 folder

answer ?7:
	rsync -av --include='*.conf' --exclude='*' ~/Downloads/linuxlab/essential-linux/data/ ~/Downloads/linuxlab/essential-linux/phucbackup/

	Transfer starting: 3 files
	./
	config.conf
	config1.conf

	sent 374 bytes  received 70 bytes  87058 bytes/sec
	total size is 128  speedup is 0.29
	
	rsync lenh sao chep file thong minh, -a archive mode, -v hien thi qua trinh sao chep, --inlcude='*.conf' bao gom file .conf, --exclude='*' loai tru cac file khong nam trong include

answer ?8:
	cat access.log error.log | sort | uniq -u

	192.168.1.1 - - [28/May/2025:14:32:00 +0000] "GET /index.html HTTP/1.1" 404 2326
	192.168.1.1 - - [28/May/2025:14:32:10 +0000] "GET /about.html HTTP/1.1" 404 1234
	192.168.1.2 - - [28/May/2025:14:32:05 +0000] "POST /form HTTP/1.1" 200 534
	[2025-05-28 14:00:00] ERROR Something bad happened
	[2025-05-28 14:01:00] WARNING Something odd

	Gop noi dung 2 file, sap xep va chi ra cac dong xuat hien 1 lan

answer ?9:
	zgrep -i "dummy" archive.tar.gz
	
	This is a dummy tar.gz file content.
	
	zgrep tuong tu grep nhung lam viec truc tiep voi file .gz

answer ?10:
	Trong file error.log khong chua tu "fail" khi dung lenh grep -i "fail" /usr/local/var/log/nginx/error.log 
