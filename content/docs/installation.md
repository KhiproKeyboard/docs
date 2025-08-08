---
title: ইনস্টলেশন গাইড
weight: 1
---

# ক্ষিপ্র ইনস্টলেশন গাইড

ক্ষিপ্র বিভিন্ন প্ল্যাটফর্মে ইনস্টল করার সম্পূর্ণ গাইড।

## লিনাক্সে ইনস্টলেশন

### ধাপ ১: পূর্বশর্ত ইনস্টল করুন

ক্ষিপ্র চালানোর জন্য আপনার সিস্টেমে `m17n` ইনস্টল থাকা প্রয়োজন। আপনার ইনপুট মেথড অনুযায়ী `Fcitx-m17n` বা `ibus-m17n` ইনস্টল করুন।

বুদ্ধিদীপ্ত সাজেশনের জন্য `ibus-typing-booster` ইনস্টল করতে হবে। এক্ষেত্রে `ibus-m17n` ব্যবহার করা ভালো।

#### ডেবিয়ান/উবুন্টু ভিত্তিক ডিস্ট্রোর জন্য:

```bash
sudo apt install ibus-m17n ibus-typing-booster
```

#### ফেডোরার জন্য:

```bash
sudo dnf install ibus-m17n ibus-typing-booster
```

### ধাপ ২: ক্ষিপ্র ইনস্টল করুন

নিচের কমান্ডটি টার্মিনালে চালিয়ে দিন। এটি স্বয়ংক্রিয়ভাবে সর্বশেষ সংস্করণ ইনস্টল করে দেবে:

#### IBus ব্যবহারকারীদের জন্য:

```bash
sudo rm /usr/share/m17n/bn-khipro*.mim; cd ~/; rm -rf khipro-m17n; git clone https://github.com/rank-coder/khipro-m17n.git; cd ~/khipro-m17n; sudo cp bn-khipro*.mim /usr/share/m17n/
```

#### Fcitx5 ব্যবহারকারীদের জন্য:

```bash
sudo rm /usr/share/m17n/bn-khipro*.mim && cd ~/ && sudo rm -rf ~/khipro-m17n && git clone https://github.com/rank-coder/khipro-m17n.git && cd ~/khipro-m17n && sudo cp bn-khipro*.mim /usr/share/m17n/ && fcitx5 restart
```

### ধাপ ৩: কনফিগার করুন

ইনস্টলেশন শেষে আপনার কম্পিউটার রিস্টার্ট করুন অথবা লগ-আউট করে আবার লগ-ইন করুন।

সেরা অভিজ্ঞতার জন্য আপনার সিস্টেমের ইনপুট মেথড সেটিংসে গিয়ে 'Bengali (khipro-m17n)' যুক্ত করুন এবং `ibus-typing-booster`-এর সেটিংস কনফিগার করুন।

বিস্তারিত কনফিগারেশনের জন্য [কনফিগারেশন](../configuration) পেজ দেখুন।

---

## উইন্ডোজে ইনস্টলেশন

### Borno কীবোর্ডে ক্ষিপ্র

Codepotro-এর জনপ্রিয় কীবোর্ড Borno Native-এর নতুন সংস্করণে ক্ষিপ্র লেআউট বিল্ট-ইন থাকছে।

**ইনস্টলেশন ধাপ:**

1. [Codepotro-এর টেলিগ্রাম সাপোর্ট গ্রুপ](https://t.me/codepotro) থেকে সর্বশেষ সংস্করণ ডাউনলোড করুন
2. অ্যাপ্লিকেশনটি ইনস্টল করুন
3. কীবোর্ড সেটিংস থেকে ক্ষিপ্র লেআউট নির্বাচন করুন

### Nms Kontho-তে ক্ষিপ্র

Nms Kontho অ্যাপ্লিকেশনের জন্য তৈরি কাস্টম লেআউট ব্যবহার করুন।

**ইনস্টলেশন ধাপ:**

1. [NMS Kontho](https://nabil-bot.github.io/Kontho/) ইনস্টল করুন
2. [Khipro NMS লেআউট](https://github.com/NabilSnigdho/khipro-nms/raw/refs/heads/main/Khipro.nmsLayout) ডাউনলোড করুন
3. ডাউনলোড করা লেআউটটি ইম্পোর্ট করুন
4. NMS Kontho রিস্টার্ট করুন
5. ক্ষিপ্র লেআউট নির্বাচন করুন

---

## অ্যান্ড্রয়েডে ইনস্টলেশন

{{< callout type="info" >}}
**আসছে শীঘ্রই!** অ্যান্ড্রয়েড ব্যবহারকারীদের জন্যেও সুখবর আসছে! Codepotro টিম তাদের জনপ্রিয় `Borno Android` কীবোর্ডে ক্ষিপ্র যুক্ত করার কাজ করছে।
{{< /callout >}}

[Borno Android কীবোর্ড](https://play.google.com/store/apps/details?id=com.codepotro.borno.keyboard) দেখুন Google Play Store-এ।

---

## সমস্যা সমাধান

### সাধারণ সমস্যা

{{< callout type="warning" >}}
**ইনস্টলেশনের পরে ক্ষিপ্র দেখাচ্ছে না?**

- কম্পিউটার রিস্টার্ট করুন বা লগ-আউট করে আবার লগ-ইন করুন
- ইনপুট মেথড সেটিংস চেক করুন
- m17n সঠিকভাবে ইনস্টল হয়েছে কিনা যাচাই করুন
{{< /callout >}}

### আরও সাহায্যের জন্য

- [টেলিগ্রাম গ্রুপ](https://t.me/+oXLVpYDtyDNmYzll) - সরাসরি আলোচনা ও সাপোর্টের জন্য
- [গিটহাব ইস্যুস](https://github.com/KhiproKeyboard) - বাগ রিপোর্ট ও ফিচার রিকোয়েস্টের জন্য

---

**পরবর্তী ধাপ:** [ম্যাপিং ও সিনট্যাক্স](../mapping-syntax) শিখুন