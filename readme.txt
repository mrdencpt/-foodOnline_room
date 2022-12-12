สู่ขั้นตอน up ขึ้น github.com
Create a new repository ที่่ github.com ชื่อ aa
ที่่ command line
ตัวอย่างจาก github ------------ เริ่มต้น
echo "# aa" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/mrdencpt/aa.git
git push -u origin main
-------------------
----- ย่อ ------
git init สร้าง folder git
git add -A
git commit -m "first commit"
git remote add origin https://github.com/mrdencpt/aa.git
git push origin main

------ เพิ่มเติม งานgit ------------
git status เช็คดูว่ามีไฟล์อะไรบ้าง
git add -A
git commit -m "updateล่าสุด"
git push origin main

…or create a new repository on the command line-----
echo "# uppercut" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/mrdencpt/uppercut.git
git push -u origin main

…or push an existing repository from the command line-----
git remote add origin https://github.com/mrdencpt/uppercut.git
git branch -M main
git push -u origin main

------------------------------------------------------------

pip install django==3.1

django-admin startproject myproject
python manage.py startapp myapp
ออกแบบ ตารางข้อมูลที่ models.py
แจ้งชื่อ myapp ที่ sittings.py INSTALLED_APPS
python manage.py makemigrations อ่านค่า จาก models.py
python manage.py migrate  สร้างตารางฐานข้อมูลตาม ตามfolder 
python manage.py createsuperuser สร้าง user admin
python manage.py runserver เข้า ไปดูหน้า admin
python manage.py startapp category สร้างแอ็พเสร็จ ต้องไปเพิ่มappที่ setting.py ด้วย
สร้าง ไฟล์ ที่ Models.py
python manage.py makemigrations

ติดตั้ง   vitualenv
pip install virtualenvwrapper-win
สร้าง
mkvirtualenv ชื่อ
ลบ
rmvirtualenv ชื่อ
เรียกใช้
workon ชื่อ
ยกเลิกการเรียกใช้
deactivate

เอาขึ้น server heroku ดัวย git
เช็ค heroku login
heroku create สร้าง app อัตโนมัติ
เว็บไซด์ https://elements.heroku.com/addons/heroku-postgresql
สร้างdatabase ด้วย 
heroku addons:create heroku-postgresql:hobby-dev

* ถ้าหาเส้นทาง master ไม่ได้
heroku git:remote -a fast-mountain-96396 (fast-mountain-96396=ชื่อแอ็พ)

เช็ค git enter

set ค่า settings.py
เพิ่ม floder staticfiles ที่ app food

pip install django_heroku
เพิ่มไฟล์ Procfile เนื้อหา web: gunicorn ชื่อโปรเจ็ก.wsgi
pip install gunicorn
pip freeze > requirements.txt

heroku create ชื่อโปรเจ็ค

heroku apps:info - ดูรายละเอียด
้heroku config - ดู database

git init สร้าง folder git

สู่ขั้นตอน up ขึ้น heroku
git add -A
git status เช็คดูว่ามีไฟล์อะไรบ้าง
git commit -m "producttion" ใส่คำอธิบาย git ครั้งนี้

heroku git:remote -a ชื่อแอ็พ (เส้นทางไป master)

git push heroku master
มี Error เปลี่ยนเป็น  
git push heroku main แทน

ใส่รหัส ถ้าไม่ได้ลองเปลี่ยน ' "
heroku config:set SECRET_KEY='7dszp%!%ae+f#!c6i07'
heroku config เช็ครหัส
git push heroku master ผลัก ขึ้น heroku

ถ้าไม่มีปัญหา จะหาตารางข้อมูลไม่เจอ
heroku run python manage.py migrate
heroku run python manage.py createsuperuser

dumpข้อมูลขึ้นไป heroku ด้วย สร้าง folder dumps (accounts เป็น app ที่มี ตาราง Models อยู่ 
python manage.py dumpdata accounts > dumps/accounts.json

สู่ขั้นตอน up heroku หลังจาก heroku login แล้ว
heroku run python manage.py loaddata dumps/accounts.json

คำสั่ง python manage.py collectstatic
จัดไฟล์ใหม่ตามตำแหน่ง settings.py STATIC_ROOT = BASE_DIR /'static'
จะได้ Folder static ข้างในประกอบด้วย ข้อมูลจาก static ย่อยของ projectname
