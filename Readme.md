# 🧅 Onion mu6tx  
### 🔹 تصفح شبكة تور بضغطة زر | Dev BY mu6tx  
### 🔹 Browse Tor Network with One Click | Dev BY mu6tx  

---

[![Telegram](https://img.shields.io/badge/Join-Telegram%20Channel-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)] ( https://t.me/mu6txr )  

---

## 📖 مقدمة | Introduction  

**onion mu6tx** هي إضافة بسيطة وقوية لمتصفحي **Chrome** و **Firefox**، تتيح لك تفعيل اتصال **Tor** عبر وكيل **SOCKS5** المحلي (`127.0.0.1:9050`) بنقرة زر واحدة. كل ما عليك هو تشغيل برنامج **Tor** في الخلفية، ثم النقر على زر التبديل داخل الإضافة – وسيتم توجيه كل حركة مرور المتصفح عبر شبكة تور.  

**onion mu6tx** is a lightweight and powerful extension for **Chrome** and **Firefox** that enables **Tor** proxy (SOCKS5 at `127.0.0.1:9050`) with a single click. Just keep **Tor** running in the background, flip the switch in the extension, and all browser traffic will be routed through the Tor network.

---

## ⚙️ المتطلبات الأساسية | Prerequisites  

- متصفح **Chrome** أو **Firefox** (أحدث إصدار).  
- برنامج **Tor** مثبت ومشغل على جهازك.  

- **Chrome** or **Firefox** browser (latest version).  
- **Tor** installed and running on your machine.

---

## 🛠️ تثبيت وتشغيل تور | Installing & Running Tor  

### 🔹 نظام ويندوز | Windows  

1. قم بتحميل **Tor Expert Bundle** من الموقع الرسمي:  
   [https://www.torproject.org/download/tor/](https://www.torproject.org/download/tor/)  
2. فك الضغط عن الملف المضغوط، وستجد ملف `tor.exe`.  
3. يمكنك تشغيله يدوياً عبر فتح **موجه الأوامر (CMD)** أو **PowerShell** في مجلد البرنامج وتنفيذ:

```cmd
tor
```

**لتشغيله تلقائياً عند بدء تشغيل النظام (اختياري):**  
- أنشئ اختصاراً لـ `tor.exe` وضعه في مجلد `Startup` (يمكن الوصول إليه عبر تشغيل `shell:startup`).  
- أو استخدم **مدير المهام** ← **بدء التشغيل** لإضافته.  

> 💡 يمكنك أيضاً تثبيته باستخدام مدير الحزم مثل **Chocolatey** أو **Scoop**:
> ```cmd
> choco install tor
> ```
> أو
> ```cmd
> scoop install tor
> ```

---

### 🔹 لينكس – فيدورا | Linux – Fedora  

```bash
sudo dnf install tor
```

**التشغيل اليدوي:**  
```bash
tor
```

**التشغيل كخدمة (للبقاء في الخلفية):**  
```bash
sudo systemctl start tor
```

**لجعله يبدأ تلقائياً عند الإقلاع:**  
```bash
sudo systemctl enable tor
```

---

### 🔹 لينكس – أرش | Linux – Arch  

```bash
sudo pacman -S tor
```

**التشغيل اليدوي:**  
```bash
tor
```

**كخدمة:**  
```bash
sudo systemctl start tor
sudo systemctl enable tor
```

---

### 🔹 ماك أو إس | macOS  

باستخدام [Homebrew](https://brew.sh/):  
```bash
brew install tor
```

**التشغيل اليدوي:**  
```bash
tor
```

**كخدمة (launchd) – للتشغيل في الخلفية:**  
```bash
brew services start tor
```

**للتشغيل التلقائي عند تسجيل الدخول:**  
```bash
brew services enable tor
```

---

> ⚠️ **ملاحظة هامة:** الإضافة تفترض أن تور يعمل على المنفذ `9050` بنوع **SOCKS5**. إذا كنت تستخدم منفذاً آخر، يمكنك تعديل الكود المصدري، لكن الإعداد الافتراضي مناسب لمعظم المستخدمين.  
> **Important:** The extension assumes Tor is running on port `9050` with **SOCKS5** proxy. If you use a different port, you can modify the source code, but the default works for most users.

---

## 🧩 تثبيت الإضافة | Installing the Extension  

- **لمتصفح Chrome:**  
  - قم بتحميل الإضافة من متجر Chrome الإلكتروني (الرابط سيُضاف قريباً) أو حمّل مجلد `chrome-version` (الذي يحتوي على `manifest.json`) وثبته يدوياً عبر `chrome://extensions` (فعّل وضع المطور ثم اختر "تحميل الملفات غير المضغوطة").  
- **لمتصفح Firefox:**  
  - حمّلها من متجر إضافات Firefox أو ثبّت مجلد `firefox-version` يدوياً عبر `about:debugging` (اختر "هذا المتصفح" ثم "تحميل إضافة مؤقتة").  

- **For Chrome:**  
  - Install from the Chrome Web Store (link coming soon) or load the `chrome-version` folder (containing `manifest.json`) manually via `chrome://extensions` (enable Developer mode → Load unpacked).  
- **For Firefox:**  
  - Install from Firefox Add-ons store or load the `firefox-version` folder manually via `about:debugging` (This Firefox → Load Temporary Add-on).

---

## 🚀 كيفية الاستخدام | How to Use  

1. تأكد من أن **Tor** قيد التشغيل (كما هو موضح أعلاه).  
2. انقر على أيقونة الإضافة في شريط الأدوات.  
3. حرّك المفتاح إلى وضع **ON** (تشغيل) – ستتغير الحالة إلى "متصل عبر Tor" وستتحول النقطة إلى اللون الأخضر.  
4. الآن كل تصفحك يمر عبر شبكة تور. لإيقاف الوكيل، حرّك المفتاح إلى **OFF**.  

1. Make sure **Tor** is running.  
2. Click the extension icon in the toolbar.  
3. Toggle the switch to **ON** – the status will change to "Connected via Tor" and the dot turns green.  
4. All your browsing is now routed through Tor. To disable, switch to **OFF**.

---

## 🔒 ملاحظات أمنية | Security Notes  

- هذه الإضافة **لا تخزن** أي سجلات أو معلومات شخصية.  
- تأكد من استخدام **HTTPS** كلما أمكن للحفاظ على تشفير شامل.  
- تور يوفر إخفاء الهوية، لكنه ليس حلاً سحرياً – استخدمه بمسؤولية.  

- This extension **does not store** any logs or personal data.  
- Always use **HTTPS** when possible for end-to-end encryption.  
- Tor provides anonymity but is not a silver bullet – use responsibly.

---

## 📢 انضم إلى قناتنا على تيلغرام | Join Our Telegram Channel  

احصل على آخر التحديثات، والإصدارات الجديدة، ودعم المجتمع.  
Get the latest updates, new releases, and community support.  

[![Telegram](https://img.shields.io/badge/Join-Telegram%20Channel-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/mu6txr)  

---

## 📝 الترخيص | License  

MIT © [mu6tx](https://t.me/mu6txr)
```
