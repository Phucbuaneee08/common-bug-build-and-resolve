# Expo Build Guide – Managed Workflow
👉 Không chỉnh sửa native code (không có thư mục `android/` và `ios/`).

### Khi nào nên dùng?
- App chủ yếu là UI + logic JavaScript
- Không cần native module đặc biệt
- Muốn build nhanh, ít lỗi

---

### Bước 1: Cài đặt công cụ
```bash
npm install -g expo-cli eas-cli
```

---

### Bước 2: Tạo project Managed
```bash
npx create-expo-app myApp
cd myApp
```

Hoặc với project có sẵn:
```bash
npx expo start
```

---

### Bước 3: Cấu hình app
Chỉnh sửa `app.json` hoặc `app.config.js`

```json
{
  "expo": {
    "name": "My App",
    "slug": "my-app",
    "version": "1.0.0",
    "sdkVersion": "51.0.0",
    "platforms": ["ios", "android"],
    "android": {
      "package": "com.philipngo.myapp"
    },
    "ios": {
      "bundleIdentifier": "com.philipngo.myapp"
    }
  }
}
```

---

### Bước 4: Đăng nhập Expo Dev
```bash
eas login
```

---

### Bước 5: Cấu hình EAS Build
```bash
eas build:configure
```
➡️ Tạo file `eas.json`

---

### Bước 6: Build app bằng EAS

**Android**
```bash
eas build -p android
```
