# อัปโหลดโปรเจกต์ขึ้น GitHub

โฟลเดอร์นี้เตรียมไว้สำหรับอัปโหลดเป็น source code ของ CommissionQueue

## สิ่งที่ไม่รวมไว้

- ฐานข้อมูลจริง `*.db`
- ไฟล์ build `bin/` และ `obj/`
- ผลทดสอบและไฟล์ชั่วคราว
- รูปภาพร้านใน `wwwroot/uploads/shops/`
- แพ็กเกจ Windows ที่ publish แล้ว

## อัปโหลดด้วย GitHub Desktop

1. เปิด GitHub Desktop
2. เลือก **Add existing repository** แล้วเลือกโฟลเดอร์นี้
3. กด **Create repository** หรือ **Publish repository**
4. ตั้งชื่อ repository และเลือก Private หากโค้ดยังไม่ต้องการเผยแพร่

## รันหลังดาวน์โหลดจาก GitHub

ต้องติดตั้ง .NET 10 SDK ก่อน แล้วเปิด PowerShell ในโฟลเดอร์โปรเจกต์:

```powershell
dotnet restore
dotnet run --project CommissionQueue.csproj --launch-profile http
```

จากนั้นเปิด `http://localhost:5080/`

ฐานข้อมูลใหม่จะถูกสร้างและระบบจะพาไปหน้า `/Setup` เพื่อสร้างร้านและบัญชี Admin ใหม่
