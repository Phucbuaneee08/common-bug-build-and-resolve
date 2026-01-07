## ❌ Lỗi
> Dán nguyên error message hoặc mô tả ngắn gọn

Execution failed for task ':app:checkReleaseDuplicateClasses'.
> A failure occurred while executing com.android.build.gradle.internal.tasks.CheckDuplicatesRunnable
   > Duplicate class android.support.v4.app.INotificationSideChannel found in modules core-1.13.1.aar -> core-1.13.1-runtime (androidx.core:core:1.13.1) and support-compat-27.1.1.aar -> support-compat-27.1.1-runtime (com.android.support:support-compat:27.1.1)
     Duplicate class android.support.v4.app.INotificationSideChannel$Stub found in modules core-1.13.1.aar -> core-1.13.1-runtime (androidx.core:core:1.13.1) and support-compat-27.1.1.aar -> support-compat-27.1.1-runtime (com.android.support:support-compat:27.1.1)
     Duplicate class android.support.v4.app.INotificationSideChannel$Stub$Proxy found in modules core-1.13.1.aar -> core-1.13.1-runtime (androidx.core:core:1.13.1) and support-compat-27.1.1.aar -> support-compat-27.1.1-runtime (com.android.support:support-compat:27.1.1)
     Duplicate class android.support.v4.os.IResultReceiver found in modules core-1.13.1.aar -> core-1.13.1-runtime (androidx.core:core:1.13.1) and support-compat-27.1.1.aar -> support-compat-27.1.1-runtime (com.android.support:support-compat:27.1.1)
     Duplicate class android.support.v4.os.IResultReceiver$Stub found in modules core-1.13.1.aar -> core-1.13.1-runtime (androidx.core:core:1.13.1) and support-compat-27.1.1.aar -> support-compat-27.1.1-runtime (com.android.support:support-compat:27.1.1)
     Duplicate class android.support.v4.os.IResultReceiver$Stub$Proxy found in modules core-1.13.1.aar -> core-1.13.1-runtime (androidx.core:core:1.13.1) and support-compat-27.1.1.aar -> support-compat-27.1.1-runtime (com.android.support:support-compat:27.1.1)
     Duplicate class android.support.v4.os.ResultReceiver found in modules core-1.13.1.aar -> core-1.13.1-runtime (androidx.core:core:1.13.1) and support-compat-27.1.1.aar -> support-compat-27.1.1-runtime (com.android.support:support-compat:27.1.1)
     Duplicate class android.support.v4.os.ResultReceiver$1 found in modules core-1.13.1.aar -> core-1.13.1-runtime (androidx.core:core:1.13.1) and support-compat-27.1.1.aar -> support-compat-27.1.1-runtime (com.android.support:support-compat:27.1.1)
     Duplicate class android.support.v4.os.ResultReceiver$MyResultReceiver found in modules core-1.13.1.aar -> core-1.13.1-runtime (androidx.core:core:1.13.1) and support-compat-27.1.1.aar -> support-compat-27.1.1-runtime (com.android.support:support-compat:27.1.1)
     Duplicate class android.support.v4.os.ResultReceiver$MyRunnable found in modules core-1.13.1.aar -> core-1.13.1-runtime (androidx.core:core:1.13.1) and support-compat-27.1.1.aar -> support-compat-27.1.1-runtime (com.android.support:support-compat:27.1.1)
---

## 🧩 Môi trường
- React Native: 
- Expo: 0.79.5
- Platform: Android 
- OS: Window
- Node: 
- Yarn / npm:
- Build Tool : Expo - Managed Workflow
---

## 🧠 Nguyên nhân
Giải thích **vì sao lỗi xảy ra**  
(Dependency conflict? Version mismatch? Cache?)

---

## ✅ Cách giải quyết
### Cách 1 (recommended)
- bật jetifier trong file "android/gradle.properties"
- android.enableJetifier=true

```bash
# command / steps