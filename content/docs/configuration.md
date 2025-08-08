---
title: কনফিগারেশন গাইড
weight: 2
---

# টাইপিং বুস্টার কনফিগারেশন

ক্ষিপ্রের সাথে `ibus-typing-booster` কনফিগার করার বিস্তারিত গাইড।

## প্রাথমিক সেটআপ

টাইপিং বুস্টার ইনস্টল করা হয়ে গেলে এরপর কম্পিউটার লগ আউট করে আবার লগ ইন করতে হবে। তারপরে সিস্টেমের ইনপুট মেথড কিংবা কিবোর্ড সংক্রান্ত সেটিংস থেকে টাইপিং বুস্টার সিলেক্ট করতে হবে।

যদি আপনার ডিস্ট্রোতে সেটিংস থেকে আইবাসের সেটিংস কনফিগার করা না যায় তবে `ibus-preferences` থেকে কাজটি করতে হবে।

![IBus Preferences](https://github.com/rank-coder/khipro-m17n/assets/54497225/f479deda-0f19-4228-9eee-2ee23cf939d7)

এখান থেকে টাইপিং বুস্টারের preferences কিংবা সেটিংসে যেতে হবে।

![Typing Booster Settings](https://github.com/rank-coder/khipro-m17n/assets/54497225/8e835083-8605-4686-98bb-5fd563d102fd)

---

## ডিকশনারি ও ইনপুট মেথড কনফিগারেশন

টাইপিং বুস্টারের সেটিংস ওপেন হলে প্রথমেই দেখা যাবে **"Dictionaries & Input Methods"** ট্যাব। 

### ধাপ ১: বাংলা ডিকশনারি যুক্ত করুন

সেখান থেকে বাংলার জন্য একটা ডিকশনারি সিলেক্ট করতে হবে। বাংলার জন্য তিনটা ডিকশনারি পাবেন; যেকোনো একটি সিলেক্ট করলেই হবে।

### ধাপ ২: ক্ষিপ্র ইনপুট মেথড সেট করুন

এরপর টাইপিং বুস্টারের মধ্যেই ইনপুট মেথড হিসেবে ক্ষিপ্রকে সিলেক্ট করতে হবে এবং অন্যান্য ইনপুট মেথড রিমুভ করতে হবে।

![Dictionary and Input Method Configuration](https://github.com/user-attachments/assets/aa4385ca-44bd-45c1-8ba9-27bd1352d72c)

---

## অপশন কনফিগারেশন

**"Options"** ট্যাবে গিয়ে নিম্নলিখিত সেটিংস অফ করে দিন:

{{< callout type="warning" >}}
**গুরুত্বপূর্ণ সেটিংস যা বন্ধ করতে হবে:**
- Use inline completion
- Auto Capitalize
- Unicode Symbols & Emoji Prediction
- Add a space when committing by mouse click
- Off the record mode
{{< /callout >}}

**যা সক্রিয় রাখতে হবে:**
- **Record Mode** এর জন্য **"everything"** সিলেক্ট করুন

### বিশেষ নোট

{{< callout type="info" >}}
**"Avoid using the forward_key_event() function"** - এটাতে টিকচিহ্ন ✓ দিতে হবে যদি টাইপিং বুস্টারে কমিট করার সময় হঠাৎ একাএকা ইনসার্শন পয়েন্টার নড়ে যাওয়ার ইস্যুর সম্মুখীন হন।
{{< /callout >}}

![Options Configuration](https://github.com/user-attachments/assets/f1c3e58e-922e-4c6e-a354-072aab7f2588)

---

## কীবাইন্ডিং কনফিগারেশন

**"Keybindings"** ট্যাবে নিম্নলিখিত সেটিংস করুন:

### মূল কীবাইন্ডিং

| অ্যাকশন | কী |
|---------|-----|
| **Commit** | `Enter` |
| **Commit-candidate-1** | `Shift+J` |
| **Commit-candidate-2** | `Shift+K` |
| **Commit-candidate-3** | `Shift+L` |
| **Commit-candidate-4** | `Shift+;` |

### গুরুত্বপূর্ণ

{{< callout type="warning" >}}
**commit-candidate-1-plus-space** থেকে `1` এবং `KP_1` কী সরিয়ে দিতে হবে। এটা করার কারণ হলো বাংলার জন্য সাজেশন কমিট করার পর স্পেস যুক্ত হওয়াটা ভালো না। বাংলায় বিভক্তি, কিংবা দুই শব্দ জোড়া দিয়ে লিখতে হতে পারে।
{{< /callout >}}

{{< callout type="info" >}}
**মনে রাখবেন:** ৪ এর বেশি কী-বাইন্ডিং সেট করবেন না।
{{< /callout >}}

![Keybindings Configuration](https://github.com/user-attachments/assets/97020509-83b8-4170-a092-9f06d47e3ed3)

---

## অ্যাপিয়ারেন্স কনফিগারেশন

**"Appearance"** ট্যাবে নিম্নলিখিত সেটিংস করুন:

### সকল চেকবক্স বন্ধ করুন

{{< callout type="info" >}}
সবগুলো চেকবক্স বন্ধ করে দিন যাতে টাইপিং বুস্টার দ্রুত কাজ করে।
{{< /callout >}}

### গুরুত্বপূর্ণ সেটিংস

| সেটিং | মান |
|--------|-----|
| **Candidate window page size** | `4` |
| **Candidate window orientation** | `Horizontal` |
| **Preedit underline** | `Single` |

**কেন এই সেটিংস?**
- **Page size 4**: চারটির বেশি সাজেশন আসলে সেটা লেখার প্রতি মনোযোগ নষ্ট করতে পারে
- **Horizontal orientation**: চোখ কম নাড়িয়ে সবগুলো সাজেশন দেখা যায়

![Appearance Configuration](https://github.com/user-attachments/assets/13e63976-0286-439b-936d-7caae789dfbd)

---

## টাইপিং বুস্টার ছাড়া ব্যবহার

যারা টাইপিং বুস্টার ছাড়া ক্ষিপ্র ব্যবহার করতে চান তারা টাইপিং বুস্টার ইনস্টল না করেই ক্ষিপ্র ব্যবহার করতে পারেন। তবে এক্ষেত্রে ইন্টেলিজেন্ট সাজেশন পাওয়া যাবে না।

---

## সমস্যা সমাধান

### সাধারণ সমস্যা

{{< callout type="warning" >}}
**টাইপিং বুস্টার কাজ করছে না?**
- কম্পিউটার রিস্টার্ট করুন
- IBus রিস্টার্ট করুন: `ibus restart`
- সেটিংস আবার চেক করুন
{{< /callout >}}

### আরও সাহায্য

- [টেলিগ্রাম গ্রুপ](https://t.me/+oXLVpYDtyDNmYzll) - সরাসরি সাপোর্ট
- [গিটহাব ইস্যুস](https://github.com/KhiproKeyboard) - বাগ রিপোর্ট

---

**পরবর্তী ধাপ:** [ম্যাপিং ও সিনট্যাক্স](../mapping-syntax) শিখুন