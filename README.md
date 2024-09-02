# Assignment1 Manual Cloud-based Web Deployment 

# Strapi 
strapi คือโปรแกรม headless cms(เป็นการจัดการเนื้อหาที่ถูกออกแบบมาเพื่อใช้ในการแยกส่วนเนื้อหาออกจากส่วนการแสดงผลหน้าเว็บไซต์) ใช้ในการสร้าง API ด้วยภาษา JavaScript โดยไม่ต้องทำการเขียนโค้ด สามารถสร้าง API ได้โดยการจัดการผ่านหน้า Dashboard ของ strapi

# ตัวอย่างการใช้งานของ strapi
	1.สื่อสารกับ Application ต่างๆ 
	2.จัดเนื้อหา เช่น images,pdf หรือ audio files 
	3.การสร้าง content websites 
	4.การพัฒนาโมบายแอปพลิเคชัน
# องค์ประกอบของ strapi
	1.Admin panel 
	2.Content Manager 
	3.Content-Type Builder 
	4.Media Library 
	5.Plugins 
	6.Database Layer 
	7.File Uploads
# ขั้นตอนการติดตั้ง
## 1.เปิด cmd(commmand prompt) 
	cmd
## 2.เขียนคำสั่ง npx create-strapi-app@latest my-project เพื่อใช้ในการสร้าง project ของ strapi โดย "my-project" สามารถเปลี่ยนชื่อตามต้องการได้
	npx create-strapi-app@latest my-project
## 3.เลือกขั้นตอนการติดตั้งมี 2 ขั้นตอน 1.Quickstart 2.Custom โดยเลือกเป็น Quickstart
	? Choose your installation type (Use arrow keys)
	> Quickstart (recommended)
  	  Custom (manual settings)
## 4.เลือก Login/Sign up หรือ skip โดยทำการเลือก Login หากมีบัญชีอยู่แล้ว
	? Please log in or sign up. (Use arrow keys)
	> Login/Sign up
  	  Skip
## 5.หากพบ error Cannot find module '@swc/core-win32-x64-msvc'
	npm install @swc/core
ให้ทำการติดตั้ง swc binding โดยใช้คำสั่ง 'npm install @swc/core'

# ขั้นตอนการ push โค้ดขึ้น github
## 1.ใช้คำสั่ง git init เพื่อสร้าง repository ขึ้นมา
	git init
## 2.ใช้คำสั่ง git add เพิ่มไฟล์ที่ต้องการเปลี่ยนแปลงไปยัง stagin area
	git add <ไฟล์ที่ต้องการ>
## 3.ใช้คำสั่ง git commit -m บันทึกการเปลี่ยนเปลี่ยนแปลงและเพิ่มข้อความอธิบายสำหรับการ push แต่ละครั้ง
	git commit -m <ข้อความที่ต้องการใส่>
## 4.ใช้คำสั่ง git branch -M เพื่อสลับไปยัง branch ที่ต้องการ
	git branch -M main
## 5.ใช้คำสั่ง git remote add origin เพื่อทำการ push โค้ดไปยัง repository ที่ต้องการ
	git remote add origin <url ของ repository>
## 6.ใช้คำสั่ง git push -u origin main ทำการ push โค้ดที่ได้ทำการเปลี่ยนแปลงไปยัง repository
	git push -u origin main

# ขั้นตอนการ clone โค้ด
## 1.ทำการสร้าง SSH key เพื่อ clone โค้ด
	ssh-keygen -t ed25519 -C "your_email@example.com"
## 2.ทำการเพิ่ม SSH key ที่เพิ่มเข้ามาใหม่ไปยัง github โดยใช้คำสั่งคัดลอก SSH key 
	$ clip < ~/.ssh/id_ed25519.pub
## 3.ใช้คำสั่ง git clone เพื่อ clone โค้ดจาก repository ที่ต้องการโดย clone เป็น SSH
	git clone <git@github.com:ชื่อ repository>

# จัดการไฟล์เพื่อให้สามารรัน strapi ได้
## 1.ทำการติดตั้ง npm ใน Linux
	npm install 
## 2.เพิ่มไฟล์ .env โดยเปลี่ยนชื่อจากไฟล์ .env.example
	mv .env.example .env

อ้างอิง: itGENIUS,การพัฒนา API Service ด้วย Strapi,เข้าถึงได้จาก https://www.itgenius.co.th/API-Services-Strapi.html  
อ้างอิง: Patiphan Phengpao,สอนใช้งาน Strapi | Headless CMS สำหรับสร้างและจัดการ API แบบง่ายๆ,เข้าถึงได้จาก https://www.youtube.com/watch?v=2rhJj_Bccng   
อ้างอิง: Max Veerapat Kumchom,ออกแบบสร้าง APIs แบบโคตรเร็ว จัดการเนื้อหาแบบโคตรง่าย ด้วย Strapi Headless CMS,เข้าถึงได้จาก https://tinyurl.com/yey2rv2z  
อ้างอิง: GitHub Docs,Generating a new SSH key and adding it to the ssh-agent,เข้าถึงได้จาก https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent   
อ้างอิง: GitHub Docs,Adding a new SSH key to your GitHub account,เข้าถึงได้จาก https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account

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
