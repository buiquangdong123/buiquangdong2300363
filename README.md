# BÀI THỰC HÀNH LINUX VÀ PHẦN MỀM MÃ NGUỒN MỞ

**Họ và tên:** Bùi Quang Đông

**Mã sinh viên:** 2300363

## Câu 2. Tao nhom va nguoi dung

```bash
groupadd hocvien
groupadd admin

useradd -m -g hocvien hv1
useradd -m -g hocvien hv2
useradd -m -g hocvien hv3

useradd -m -g admin admin1
useradd -m -g admin admin2

echo "hv1:1234567" | chpasswd
echo "hv2:1234567" | chpasswd
echo "hv3:1234567" | chpasswd
echo "admin1:1234567" | chpasswd
echo "admin2:1234567" | chpasswd
```

Kiểm tra:

```bash
cat /etc/group | grep hocvien
cat /etc/group | grep admin
cat /etc/passwd | grep hv
cat /etc/passwd | grep admin
```

---

## Câu 3. Chinh sua description

```bash
usermod -c "Nguoi dung quan tri he thong" admin1
usermod -c "Nguoi dung quan tri he thong" admin2
```

Kiểm tra:

```bash
getent passwd admin1
getent passwd admin2
```

---

## Câu 9. Thiet lap quyen mac đinh

```bash
umask 027
```

Kiểm tra:

```bash
umask
```

Tạo file và thư mục:

```bash
touch baitap.txt
mkdir baitap
```

Kiểm tra quyền:

```bash
ls -l baitap.txt
ls -ld baitap
```

Kết quả mong muốn:

```
-rw-r-----
drwxr-x---
```

---

## Câu 10. Theo doi và thong ke su dung tai nguyen he thong

```bash
top
ps -u hv1
ps -u admin1
du -sh /home/*
id hv1
who
w
```
