# Assignment1 Manual Cloud-based Web Deployment 

# Strapi 
strapi คือโปรแกรม headless cms(เป็นการจัดการเนื้อหาที่ถูกออกแบบมาเพื่อใช้ในการแยกส่วนเนื้อหาออกจากส่วนการแสดงผลหน้าเว็บไซต์) ใช้ในการสร้าง API ด้วยภาษา JavaScript โดยไม่ต้องทำการเขียนโค้ด สามารถสร้าง API ได้โดยการจัดการผ่านหน้า Dashboard ของ strapi

## ตัวอย่างการใช้งานของ strapi
	1.สื่อสารกับ Application ต่างๆ 
	2.จัดเนื้อหา เช่น images,pdf หรือ audio files 
	3.การสร้าง content websites 
	4.การพัฒนาโมบายแอปพลิเคชัน
## องค์ประกอบของ strapi
	1.Admin panel 
	2.Content Manager 
	3.Content-Type Builder 
	4.Media Library 
	5.Plugins 
	6.Database Layer 
	7.File Uploads
## ขั้นตอนการติดตั้ง
	1.เปิด cmd(commmand prompt) 
	2.เขียนคำสั่ง npx create-strapi-app@latest my-project เพื่อใช้ในการสร้าง project ของ strapi โดย "my-project" สามารถเปลี่ยนชื่อตามต้องการได้
	3.เลือกขั้นตอนการติดตั้งมี 2 ขั้นตอน 1.Quickstart 2.Custom โดยเลือกเป็น Quickstart
	4.เลือก Login/Sign up หรือ skip โดยทำการเลือก Login หากมีบัญชีอยู่แล้ว
	5.หากพบ error Cannot find module '@swc/core-win32-x64-msvc'
	ให้ทำการติดตั้ง swc binding โดยใช้คำสั่ง 'npm install @swc/core'
	6.หากต้องการ clone ไฟล์ strapi จาก github ต้องทำการติดต้ง node และ ไฟล์ .env เพื่อให้ strapi สามารถรันได้

อ้างอิง: itGENIUS,การพัฒนา API Service ด้วย Strapi,เข้าถึงได้จาก https://www.itgenius.co.th/API-Services-Strapi.html
อ้างอิง: Patiphan Phengpao,สอนใช้งาน Strapi | Headless CMS สำหรับสร้างและจัดการ API แบบง่ายๆ,เข้าถึงได้จาก https://www.youtube.com/watch?v=2rhJj_Bccng
อ้างอิง: Max Veerapat Kumchom,ออกแบบสร้าง APIs แบบโคตรเร็ว จัดการเนื้อหาแบบโคตรง่าย ด้วย Strapi Headless CMS,เข้าถึงได้จาก https://tinyurl.com/yey2rv2z

----
# gitignore
## gitignore คือการทำให้ git รู้ว่าไฟล์ใดไม่ควรทำการ push ขึ้นบน git โดยมีดังนี้
	1.OS X ไฟล์และโฟลเดอร์ในระบบปฎิบ้ตืการของ macOS
	2.Linux ไฟล์และโฟลเดอร์ในระบบปฎิบ้ตืการของ Linux
	3.Windows ไฟล์และโฟลเดอร์ในระบบปฎิบ้ตืการของ Windows
	4.Packages ไฟล์ประเภทแพคเกจหรือไฟล์ที่มีการบีบอัด
	5.Logs and databases ไฟล์ประเภท Logs และ ฐานข้อมูล
	6.Misc โฟลเดอร์ทั่วไปที่ไม่ต้องการให้ติดตาม
	7.Node.js ไฟล์และโฟลเดอร์ Node.js
	8.Tests ไฟล์เกี่ยวกับผลการทดสอบ
	9.Strapi ไฟล์และโฟลเดอร์ที่เกี่ยวข้องกับ strapi เช่น .env

อ้างอิง: chatGPT,ประเภทของไฟล์ที่ทำการ ignore
อ้างอิง: GitHub Docs,Ignoring files,เข้าถึงได้จาก https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files

# สเปคแนะนำสำหรับการ Deploy Strapi 
## Hardware and software requirements สเปคขั้นต่ำที่แนะนำสำหรับการ deploy 
	Hardware   Recommended   Minimum 
	CPU        2+ cores      1 core
	Memory     4GB+          2GB
	Disk       32GB+         8GB
สำหรับการ deploy บน amazon ec2 เครื่องที่เลือกใช้จะเป็น t2.medium โดยมี cpu 2 cores memory 4 GB และ Disk 32GB ซึ่งเป็นสเปคขั้นแนะนำของ strapi ที่กำหนดไว้

อ้างอิง: strapi DOC,Deployment,เข้าถึงได้จากhttps://docs.strapi.io/dev-docs/deployment
