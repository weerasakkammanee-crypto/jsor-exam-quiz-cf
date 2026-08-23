# jsor-exam-quiz (Cloudflare Workers deploy)

ไฟล์เว็บแอปข้อสอบ จ.ส.อ. เลื่อนฐานะเป็นนายทหารสัญญาบัตร (ไฟล์เดียวจบ index.html) สำหรับ deploy บน Cloudflare Workers ผ่าน Git integration

โฟลเดอร์นี้มีแค่ 3 ไฟล์ ไม่มีคลังข้อสอบ/ไฟล์เบื้องหลังปนอยู่ (เพื่อความปลอดภัย):
- index.html — ตัวเว็บแอป (โหลดคลังข้อสอบจากเซิร์ฟเวอร์ Apps Script ตอนล็อกอิน ไม่ได้ฝังคำตอบไว้ในไฟล์นี้)
- wrangler.jsonc — ค่าตั้งค่า Worker (ชื่อ Worker ต้องตรงกับที่ตั้งในหน้า Cloudflare dashboard ตอน import)
- package.json — ระบุ wrangler เป็น dev dependency ให้ Cloudflare Workers Builds เรียก `npx wrangler deploy` ได้เอง

ขั้นตอน deploy: ดูคำแนะนำที่ส่งมาพร้อมกันในแชท
