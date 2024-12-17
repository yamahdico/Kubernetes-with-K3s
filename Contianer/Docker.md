---

### **1. اطلاعات پایه‌ای**
1. **بررسی نسخه داکر:**
   ```bash
   docker --version
   ```
   نمایش نسخه نصب‌شده داکر.

2. **اطلاعات کامل داکر:**
   ```bash
   docker info
   ```
   نمایش اطلاعات کلی درباره تنظیمات و وضعیت داکر.

---

### **2. مدیریت ایمیج‌ها**
1. **جستجوی یک ایمیج:**
   ```bash
   docker search <image-name>
   ```
   جستجوی ایمیج مورد نظر در Docker Hub.

2. **دانلود یک ایمیج:**
   ```bash
   docker pull <image-name>
   ```
   دانلود ایمیج از Docker Hub.

3. **مشاهده لیست ایمیج‌ها:**
   ```bash
   docker images
   ```
   مشاهده تمامی ایمیج‌های موجود در سیستم.

4. **حذف یک ایمیج:**
   ```bash
   docker rmi <image-id>
   ```
   حذف ایمیج با استفاده از شناسه (ID) یا نام.

---

### **3. مدیریت کانتینرها**
1. **اجرای یک کانتینر:**
   ```bash
   docker run <image-name>
   ```
   اجرای یک کانتینر از یک ایمیج.

2. **اجرای کانتینر در پس‌زمینه:**
   ```bash
   docker run -d <image-name>
   ```
   اجرای کانتینر به صورت دیمون (پس‌زمینه).

3. **اجرای کانتینر با پورت مشخص:**
   ```bash
   docker run -d -p <host-port>:<container-port> <image-name>
   ```
   نگاشت پورت‌های سیستم میزبان به کانتینر.

4. **مشاهده کانتینرهای فعال:**
   ```bash
   docker ps
   ```
   نمایش لیست کانتینرهای در حال اجرا.

5. **مشاهده همه کانتینرها:**
   ```bash
   docker ps -a
   ```
   نمایش لیست تمامی کانتینرها (فعال و غیرفعال).

6. **توقف یک کانتینر:**
   ```bash
   docker stop <container-id>
   ```
   توقف اجرای یک کانتینر.

7. **حذف یک کانتینر:**
   ```bash
   docker rm <container-id>
   ```
   حذف یک کانتینر (غیرفعال).

8. **مشاهده لاگ‌های یک کانتینر:**
   ```bash
   docker logs <container-id>
   ```
   نمایش خروجی‌های یک کانتینر.

9. **اتصال به داخل کانتینر:**
   ```bash
   docker exec -it <container-id> /bin/bash
   ```
   اجرای دستور در داخل کانتینر یا دسترسی به ترمینال آن.

---

### **4. مدیریت حجم‌ها (Volumes)**
1. **ایجاد یک ولوم:**
   ```bash
   docker volume create <volume-name>
   ```

2. **مشاهده لیست ولوم‌ها:**
   ```bash
   docker volume ls
   ```

3. **اتصال ولوم به کانتینر:**
   ```bash
   docker run -d -v <volume-name>:/path/in/container <image-name>
   ```

---

### **5. داکر Compose**
1. **اجرای داکر کامپوز:**
   ```bash
   docker-compose up
   ```
   اجرای تمام سرویس‌های تعریف‌شده در فایل `docker-compose.yml`.

2. **توقف سرویس‌ها:**
   ```bash
   docker-compose down
   ```

---

### **6. پاک‌سازی سیستم**
1. **حذف تمامی کانتینرها:**
   ```bash
   docker rm $(docker ps -a -q)
   ```

2. **حذف تمامی ایمیج‌ها:**
   ```bash
   docker rmi $(docker images -q)
   ```

3. **حذف فایل‌های بی‌استفاده:**
   ```bash
   docker system prune
   ```

---