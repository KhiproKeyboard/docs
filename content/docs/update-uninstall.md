---
title: আপডেট ও আনইনস্টলেশন
weight: 4
---

# ক্ষিপ্র আপডেট ও আনইনস্টলেশন গাইড

ক্ষিপ্র কিবোর্ড আপডেট ও আনইনস্টল করার সম্পূর্ণ গাইড।

## ক্ষিপ্র আপডেট করা

আপডেট করাটা খুবই সোজা। `.mim` ফাইলের নামে ভার্শন নম্বর লেখা থাকবে। ভার্শন নম্বর দেখে নিশ্চিত করুন নতুন ভার্শন এসেছে কি-না।

{{< callout type="info" >}}
**সহজ আপডেট:** নতুন করে `.mim` ফাইল ডাউনলোড করে জায়গা মতো রেখে দিন। এটা একটা কমান্ডেই করা যায়।
{{< /callout >}}

### IBus ব্যবহারকারীদের জন্য

```bash
sudo rm /usr/share/m17n/bn-khipro*.mim; cd ~/; sudo rm -rf khipro-m17n; git clone https://github.com/rank-coder/khipro-m17n.git; cd ~/khipro-m17n; sudo cp bn-khipro*.mim /usr/share/m17n/; ibus restart; exit
```

### Fcitx5 ব্যবহারকারীদের জন্য

```bash
sudo rm /usr/share/m17n/bn-khipro*.mim && cd ~/ && sudo rm -rf ~/khipro-m17n && git clone https://github.com/rank-coder/khipro-m17n.git && cd ~/khipro-m17n && sudo cp bn-khipro*.mim /usr/share/m17n/ && fcitx5 restart && exit
```

### আপডেট সম্পন্ন করা

{{< callout type="warning" >}}
**গুরুত্বপূর্ণ:** আপডেট কমান্ড চালানোর পরে, কম্পিউটার লগআউট করে লগইন করুন অথবা রিস্টার্ট করুন।
{{< /callout >}}

---

## ক্ষিপ্র আনইনস্টল করা

আনইনস্টল করার জন্য টাইপিং বুস্টার আনইনস্টল করে তারপরে m17n আনইনস্টল করতে হবে।

{{< callout type="info" >}}
**বিশেষ নোট:** m17n আনইনস্টল করাটা জরুরি নয়, কারণ সেটি অন্য কোনো লেআউটের জন্য ডিপেন্ডেন্সি হিসেবে থাকতে পারে।
{{< /callout >}}

### ধাপ ১: ক্ষিপ্র ফাইল সরানো

প্রথমে ক্ষিপ্রের `.mim` ফাইলগুলো সিস্টেম থেকে সরিয়ে ফেলুন:

```bash
sudo rm /usr/share/m17n/bn-khipro*.mim
```

### ধাপ ২: ডাউনলোড করা ফাইল সরানো

হোম ডিরেক্টরি থেকে ক্ষিপ্র ফোল্ডার সরিয়ে ফেলুন:

```bash
rm -rf ~/khipro-m17n
```

### ধাপ ৩: ইনপুট মেথড রিস্টার্ট

```bash
# IBus ব্যবহারকারীদের জন্য
ibus restart

# Fcitx5 ব্যবহারকারীদের জন্য  
fcitx5 restart
```

### ধাপ ৪: টাইপিং বুস্টার আনইনস্টল (ঐচ্ছিক)

যদি টাইপিং বুস্টার আর ব্যবহার না করতে চান:

#### ডেবিয়ান/উবুন্টু ভিত্তিক ডিস্ট্রো:

```bash
sudo apt remove ibus-typing-booster
```

#### ফেডোরা:

```bash
sudo dnf remove ibus-typing-booster
```

### ধাপ ৫: m17n আনইনস্টল (ঐচ্ছিক)

{{< callout type="warning" >}}
**সতর্কতা:** m17n আনইনস্টল করার আগে নিশ্চিত হয়ে নিন যে আপনার সিস্টেমে অন্য কোনো বাংলা বা আন্তর্জাতিক কিবোর্ড লেআউট ব্যবহার হচ্ছে না।
{{< /callout >}}

#### ডেবিয়ান/উবুন্টু ভিত্তিক ডিস্ট্রো:

```bash
sudo apt remove ibus-m17n
# বা Fcitx ব্যবহারকারীরা:
sudo apt remove fcitx-m17n
```

#### ফেডোরা:

```bash
sudo dnf remove ibus-m17n
# বা Fcitx ব্যবহারকারীরা:
sudo dnf remove fcitx-m17n
```

### ধাপ ৬: চূড়ান্ত সেটআপ

{{< callout type="info" >}}
**সম্পূর্ণ করতে:** কম্পিউটার লগআউট করে আবার লগইন করুন বা রিস্টার্ট করুন।
{{< /callout >}}

---

## ভার্শন চেক করা

ক্ষিপ্রের বর্তমান ভার্শন চেক করতে:

```bash
ls /usr/share/m17n/bn-khipro*
```

এই কমান্ডটি আপনার সিস্টেমে ইনস্টল করা ক্ষিপ্র ফাইলের তালিকা এবং ভার্শন নম্বর দেখাবে।

---

## সাধারণ সমস্যা ও সমাধান

### সমস্যা ১: আপডেটের পরে ক্ষিপ্র কাজ করছে না

{{< callout type="warning" >}}
**সমাধান:**
1. কম্পিউটার রিস্টার্ট করুন
2. ইনপুট মেথড সেটিংস চেক করুন  
3. টাইপিং বুস্টার কনফিগারেশন আবার দেখুন
{{< /callout >}}

### সমস্যা ২: আনইনস্টলের পরেও ক্ষিপ্র দেখাচ্ছে

{{< callout type="info" >}}
**সমাধান:**
1. ক্যাশ ক্লিয়ার করুন: `ibus restart`
2. সিস্টেম রিস্টার্ট করুন
3. `/usr/share/m17n/` ডিরেক্টরিতে `bn-khipro` সংক্রান্ত কোনো ফাইল বাকি আছে কিনা চেক করুন
{{< /callout >}}

### সমস্যা ৩: Permission denied এরর

```bash
# এই কমান্ড দিয়ে চেষ্টা করুন:
sudo -i
# তারপর আপডেট/আনইনস্টল কমান্ড চালান
```

---

## ব্যাকআপ ও রিস্টোর

### কনফিগারেশন ব্যাকআপ

আপনার টাইপিং বুস্টার কনফিগারেশন ব্যাকআপ রাখতে:

```bash
# কনফিগ ব্যাকআপ
cp -r ~/.config/ibus/bus/ ~/ibus-config-backup/

# টাইপিং বুস্টার সেটিংস ব্যাকআপ
dconf dump /org/freedesktop/ibus/engine/typing-booster/ > ~/typing-booster-settings.conf
```

### কনফিগারেশন রিস্টোর

```bash
# কনফিগ রিস্টোর
cp -r ~/ibus-config-backup/ ~/.config/ibus/bus/

# টাইপিং বুস্টার সেটিংস রিস্টোর
dconf load /org/freedesktop/ibus/engine/typing-booster/ < ~/typing-booster-settings.conf
```

---

## সাহায্য ও সাপোর্ট

### সমস্যার সম্মুখীন হলে

{{< cards >}}
  {{< card link="https://t.me/+oXLVpYDtyDNmYzll" title="টেলিগ্রাম গ্রুপ" icon="external-link" >}}
  {{< card link="https://github.com/KhiproKeyboard" title="গিটহাব ইস্যুস" icon="external-link" >}}
{{< /cards >}}

### রিপোর্ট করার সময় যা যা উল্লেখ করবেন

{{< callout type="info" >}}
**সমস্যা রিপোর্ট করার সময় নিম্নলিখিত তথ্য দিন:**

- আপনার অপারেটিং সিস্টেম ও ভার্শন
- ব্যবহৃত ইনপুট মেথড (IBus/Fcitx)
- ক্ষিপ্রের ভার্শন নম্বর
- সমস্যার বিস্তারিত বর্ণনা
- এরর মেসেজ (যদি থাকে)
{{< /callout >}}

---

**পরবর্তী ধাপ:** [টাইপিং বুস্টার ছাড়া ব্যবহার](../without-typing-booster) দেখুন