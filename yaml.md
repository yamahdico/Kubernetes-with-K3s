برای تبدیل دستور `docker run` به یک فایل YAML مناسب برای یک **Deployment** در Kubernetes، ابتدا باید مشخص کنیم که چه ویژگی‌هایی در فایل Kubernetes نیاز است. 

در زیر، نمونه‌ای از یک فایل YAML برای **Deployment** که دستور `docker run -it --entrypoint /bin/ash n8nio/n8n` را شبیه‌سازی می‌کند، آورده شده است:

### Deployment YAML
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: n8n-deployment
  labels:
    app: n8n
spec:
  replicas: 1
  selector:
    matchLabels:
      app: n8n
  template:
    metadata:
      labels:
        app: n8n
    spec:
      containers:
      - name: n8n-container
        image: n8nio/n8n
        command: ["/bin/ash"]
        tty: true # برای پشتیبانی از TTY (شبیه -t در Docker)
        stdin: true # برای فعال کردن ورودی تعاملی (شبیه -i در Docker)
```

---

### توضیحات:

‎
- آیتم اول

سیبسیبسیب

‎

‎
- آیتم اول

سیبسیبسیب
‎



‎
- آیتم اول

سیبسیبسیب



- آیتم سوم




:::rtl
1. تست
2. تست دو
:::


1. **`apiVersion: apps/v1`**:
   تعیین نسخه API برای یک Deployment.

2. **`kind: Deployment`**:
   نوع منبع Kubernetes که یک Deployment را ایجاد می‌کند.

3. **`metadata`**:
   اطلاعات مربوط به نام و برچسب‌های Deployment.

4. **`spec`**:
   مشخصات اصلی Deployment:
   - **`replicas`**: تعداد نمونه‌هایی که می‌خواهید اجرا شوند. در اینجا روی ۱ تنظیم شده است.
   - **`selector`**: مشخص می‌کند که این Deployment چه پادهایی را مدیریت می‌کند.
   - **`template`**: قالبی برای ایجاد پادها.

5. **`containers`**:
   - **`name`**: نام کانتینر.
   - **`image`**: تصویری که باید برای اجرای کانتینر استفاده شود.
   - **`command`**: فرمانی که در هنگام شروع کانتینر اجرا می‌شود. در اینجا، `/bin/ash` به‌عنوان نقطه ورود (`--entrypoint`) تنظیم شده است.
   - **`tty: true`**: فعال کردن TTY.
   - **`stdin: true`**: برای فعال کردن ورودی تعاملی.

---

### اعمال فایل YAML:
برای اجرای این Deployment:
1. فایل YAML را ذخیره کنید، مثلاً با نام `n8n-deployment.yaml`.
2. دستور زیر را اجرا کنید:
   ```bash
   kubectl apply -f n8n-deployment.yaml
   ```
3. برای دسترسی به پاد:
   ```bash
   kubectl exec -it <pod-name> -- /bin/ash
   ```
   نام پاد را می‌توانید با دستور `kubectl get pods` پیدا کنید.

این روش دستور Docker را به طور کامل در Kubernetes بازآفرینی می‌کند.
