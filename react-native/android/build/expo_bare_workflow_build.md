# Expo Build Guide – Bare Workflow
## Expo Bare Workflow
👉 Có toàn quyền chỉnh sửa native code (`android/`, `ios/`).

### Khi nào nên dùng?
- Cần native SDK đặc biệt
- Dùng thư viện không hỗ trợ Managed
- App phức tạp (game, BLE, AR, Unity...)

---

### Bước 1: Tạo project Bare

**Tạo mới**
```bash
npx create-expo-app myApp --template bare-minimum
```

**Hoặc eject từ Managed**
```bash
npx expo prebuild
```
➡️ Sinh thư mục `android/` và `ios/`

---

### Bước 2: Cài tool native

**Android**
- Android Studio
- JDK 17
- ANDROID_HOME

### Bước 3: Chạy app local

**Android**
```bash
npx expo run:android
```


### Bước 4: Cấu hình EAS Build
```bash
eas build:configure
```

---

### Bước 5: Build bằng EAS

**Android**
```bash
eas build -p android
```

### Bước 6: Build local (tuỳ chọn)

**Android**
```bash
cd android
./gradlew assembleRelease   => file apk và aab sẽ được generate tại thư mục android/app/build/outputs
```