# OWASP Application Security Verification Standard 4.0.3

## [2.5.6 Credential Recovery](https://owasp.org/www-project-application-security-verification-standard/)

- Verify forgotten password, and other recovery paths use a secure recovery mechanism, such as time-based OTP (TOTP) or other soft token, mobile push, or another offline recovery mechanism.

## [ChatGPT](https://chatgpt.com)

- ควรใช้กลไกที่ปลอดภัยในการกู้คืนรหัสผ่านหรือข้อมูลรับรอง เช่น TOTP, โทเค็นซอฟต์แวร์, การแจ้งเตือนผ่านมือถือ หรือวิธีออฟไลน์อื่น ๆ เพื่อเพิ่มความปลอดภัยและลดความเสี่ยงจากการโจมตี.

## [Gemini](https://gemini.google.com/app)

- เพื่อให้มั่นใจในความปลอดภัยของการกู้คืนบัญชี ระบบควรใช้กลไกการกู้คืนรหัสผ่านที่ปลอดภัย เช่น TOTP, soft token, mobile push หรือวิธีการกู้คืนแบบออฟไลน์ เพื่อป้องกันการเข้าถึงบัญชีโดยไม่ได้รับอนุญาต

## Summary

- เราควรออกแบบและสร้างระบบที่ใช้สำหรับกู้คืนบัญชีหรือรหัสผ่านให้ปลอดภัย เช่นการใช้เทคนิค TOTP, soft token, mobile push หรือ offline recovery เพื่อป้องกันการเข้าถึงบัญชีโดยไม่ได้รับอนุญาต และลดความเสี่ยงจากการถูกโจมตีโดยผู้ไม่ประสงค์ดี

## Sample in Daily Life

1. TOTP (Time-based One-Time Password)
    - เวลาลืมรหัสผ่าน Facebook หรือ Google แล้วกด "ลืมรหัสผ่าน"
    - ระบบจะให้เลือกวิธียืนยันตัวตน เช่น ผ่านแอป Google Authenticator หรือ Authy
    - แอปจะสร้างรหัส OTP ที่เปลี่ยนทุก ๆ 30 วินาที
    - เรานำรหัสนั้นมากรอกในหน้ากู้คืนรหัสผ่านเพื่อยืนยันตัวตน

2. Mobile Push Notification
    - เวลาที่จะเข้าสู่ระบบแอปธนาคารบนมือถือแต่ลืมรหัสผ่าน
    - แอปจะแจ้งเตือน (Push Notification) ไปยังอุปกรณ์ที่เชื่อมต่อ เช่น โทรศัพท์มือถือ
    - กดอนุมัติหรือยืนยันการกู้คืนรหัสผ่านจากการแจ้งเตือนนั้น
      
3. Offline Recovery Mechanism
    - ในบางบริการ (เช่น บริการคลาวด์) ผู้ใช้สามารถสร้าง Recovery Codes หรือ Backup Codes ได้
    - รหัสเหล่านี้สามารถพิมพ์หรือบันทึกเก็บไว้ออฟไลน์
    - เมื่อลืมรหัสผ่านและไม่สามารถเข้าถึงอุปกรณ์ยืนยันตัวตน ระบบจะขอให้กรอก Recovery Code แทน
