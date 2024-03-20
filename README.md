بالطبع، إليك النص المنسق والمصحح:

```markdown
# تثبيت نظام Kali Linux على Termux

## المتطلبات:
- 1 كيكا (1GB) رام
- 2 كيكا (2GB) تخزين
- تطبيق Termux
- عارض RVNC
- اتصال بالإنترنت
```
## الخطوات:

1. تحديث الحزم:
   ```shell
   pkg update
   pkg install openssl-tool
   ```

2. تثبيت حزمة wget:
   ```sh
   pkg install wget
   ```

3. تثبيت حزمة Kali Linux:
   ```shell
   wget -O install-nethunter-termux https://offs.ec/2MceZWr
   chmod +x install-nethunter-termux
   shell
   ./install-nethunter-termux
   ```

4. اختيار نوع الأداء:
   - اختر النوع المطلوب: NetHunter ARM64 (full/minimal/nano)

5. انتظر حتى يتم تحميل وتثبيت النظام.

6. عندما يطلب منك حذف الملفات، اختر "N".

7. انتظر قليلاً حتى يتم فك الضغط وتحميل ال rootfs.

8. اكتب الأمر `nethunter` للدخول إلى نظام Kali Linux.

9. إذا أردت واجهة رسومية، قم بتثبيت RVNC واتبع الخطوات المذكورة.

10. لحل مشكلة "[Process completed (signal 9) - press Enter]"، قم بتنفيذ الأوامر التالية:
    ```shell
    apt install android-tools
    adb
    adb pair Yor_Ip
    adb shell "/system/bin/dumpsys activity settings | grep max_phantom_processes"
    adb shell "/system/bin/dumpsys activity processes -a"
    adb shell "/system/bin/device_config set_sync_disabled_for_tests persistent"
    adb shell "/system/bin/device_config put activity_manager max_phantom_processes 2147483647"
    adb shell settings put global settings_enable_monitor_phantom_procs false
    ```

11. قم بتشغيل Termux واكتب الأمر
12. ```shell
    nh```
13.  ثم
14.  ```shell
     ethunter kex```

15. انتقل إلى تطبيق RVNC واتبع الخطوات المذكورة للاتصال بنظام Kali Linux.

مبروك! لقد قمت بتثبيت نظام Kali Linux بنجاح على جهازك باستخدام Termux.

هذا يشرح الخطوات بشكل أفضل ويصحح الأخطاء التي تم اكتشافها، بالإضافة إلى تنسيقه كملف `README.md` لرفعه في مستودع المشروع على منصة GitHub أو ما شابه.
ونفذ هذه الاوامر بالترتيب
```shell
nethunter kex &```
وأفتح التطبيق 
واضغط ال (+) الموجود اسفل الشاشه بعدها يضهر لك مربعين الاول تكتب به
```shell
localhost:5901```
الثاني  تكتب به اي شيء مثلا
my Test Net hunter

تضغط Create 
بعدها connect
بعدها يوجهك لشاشه شبه حمراء تضغط Ok الفوق الشاشه


لحل مشكلة
[Process completed (signal 9) - press Enter]
ببساطه حمل اولا 
apt install android-tools
بعدها تضغط y
بعدها
adb
بعدها اذهب للاعدادات> خيارات المطورين>

 تصحيح اخطاء. usp  (فعلها) 

تصحيح الاخطاء لاسلكيا شغلها وانسخ ip الخاص بك
مثل 192.168.0.104:49285 الخ..  انسخه فقط 


بعدها 
adb pair Yor_Ip
بعدها يطلب منك رقم تأخذه من كلمة الاتصال عن طريق رمز (الاقتران بواسطة رمز الاقتران) 

تكتب الرمز 
وبعدها اضغط ok او اتصال لكي يتصل 

وبعدها تنفذ هذه الاوامر تنسخها كلها دفعه واحده وتنفذها

adb shell "/system/bin/dumpsys activity settings | grep max_phantom_processes"

adb shell "/system/bin/dumpsys activity processes -a"

adb shell "/system/bin/device_config set_sync_disabled_for_tests persistent"

adb shell "/system/bin/device_config put activity_manager max_phantom_processes 2147483647"

adb shell settings put global settings_enable_monitor_phantom_procs false

بعدها افتح الترمنال واكتب
nh
وبعدها
nethunter kex

بعدين روح للبرنامج وشغله ومبروك عليك الواحه الرسموميه وتضغيل التطبيق 🥱🖤

by: @x10xxx
ch: @l4vl4
