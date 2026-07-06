+++
title = "راهنمای نحوه Markdown"
date = "2022-10-20"
description = "نمونه مقاله‌ای که نحوه پایه‌ای Markdown و قالب‌بندی عناصر HTML را نشان می‌دهد."
[taxonomies]
tags = ["markdown", "css", "html"]
[extra]
cover.image = "images/markdown-syntax.png"
cover.alt = "لوگوی Markdown"
+++

این مقاله نمونه‌ای از نحوه پایه‌ای Markdown را ارائه می‌دهد که می‌تواند در فایل‌های محتوای Zola استفاده شود، همچنین نشان می‌دهد که آیا عناصر پایه‌ای HTML در پوسته Kita با CSS تزئین شده‌اند یا خیر.

<!--more-->

## عنوان‌ها

عناصر HTML زیر `<h1>`—`<h6>` شش سطح از عنوان‌های بخش را نشان می‌دهند. `<h1>` بالاترین سطح بخش است در حالی که `<h6>` پایین‌ترین سطح است.

# H1

## H2

### H3

#### H4

##### H5

###### H6

## پاراگراف

Xerum, quo qui aut unt expliquam qui dolut labo. Aque venitatiusda cum, voluptionse latur sitiae dolessi aut parist aut dollo enim qui voluptate ma dolestendit peritin re plis aut quas inctum laceat est volestemque commosa as cus endigna tectur, offic to cor sequas etum rerum idem sintibus eiur? Quianimin porecus evelectur, cum que nis nust voloribus ratem aut omnimi, sitatur? Quiatem. Nam, omnis sum am facea corem alique molestrunt et eos evelece arcillit ut aut eos eos nus, sin conecerem erum fuga. Ri oditatquam, ad quibus unda veliamenimin cusam et facea ipsamus es exerum sitate dolores editium rerore eost, temped molorro ratiae volorro te reribus dolorer sperchicium faceata tiustia prat.

Itatur? Quiatae cullecum rem ent aut odis in re eossequodi nonsequ idebis ne sapicia is sinveli squiatum, core et que aut hariosam ex eat.

## نقل‌قول‌ها

عنصر نقل‌قول محتوایی را نشان می‌دهد که از منبع دیگری نقل شده است، به صورت اختیاری با ارجاعی که باید در عنصر `footer` یا `cite` باشد، و به صورت اختیاری با تغییرات درون‌خطی مانند حاشیه‌نویسی و اختصارات.

### نقل‌قول بدون ارجاع

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
> **توجه** که می‌توانید از _نحوه Markdown_ در داخل نقل‌قول استفاده کنید.

### نقل‌قول با ارجاع

> Don't communicate by sharing memory, share memory by communicating.<br>
> — <cite>Rob Pike[^1]</cite>

[^1]: نقل‌قول فوق از [سخنرانی](https://www.youtube.com/watch?v=PAAkCSZUG1c) Rob Pike در Gopherfest، ۱۸ نوامبر ۲۰۱۵ برگرفته شده است.

## پیوندها

برای ایجاد پیوند، متن پیوند را در داخل براکت قرار دهید و سپس بلافاصله URL را در داخل پرانتز قرار دهید.

[GitHub](https://github.com)

برای تبدیل سریع URL یا آدرس ایمیل به پیوند، آن را در داخل براکت زاویه‌دار قرار دهید.

<https://github.com>

## تصاویر

![Markdown Guide](/images/markdown-syntax.png)

## جداول

جداول بخشی از مشخصات پایه‌ای Markdown نیستند، اما Zola به صورت پیش‌فرض از آنها پشتیبانی می‌کند.

| نام  | سن |
| ----- | --- |
| Bob   | 27  |
| Alice | 23  |

### Markdown درون‌خطی در جداول

| ایتالیک   | بولد     | کد   |
| --------- | -------- | ------ |
| _ایتالیک_ | **بولد** | `کد` |

## بلوک‌های کد

### بلوک کد با backticks

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Example HTML5 Document</title>
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```

### بلوک کد با تورفتگی چهار فاصله

    <!doctype html>
    <html lang="en">
    <head>
      <meta charset="utf-8">
      <title>Example HTML5 Document</title>
    </head>
    <body>
      <p>Test</p>
    </body>
    </html>

## هشدار به سبک GitHub

> [!NOTE]
> اطلاعات مفیدی که کاربران باید بدانند، حتی زمانی که محتوا را مرور می‌کنند.

> [!TIP]
> توصیه‌های مفید برای انجام بهتر یا راحت‌تر کارها.

> [!IMPORTANT]
> اطلاعات کلیدی که کاربران برای دستیابی به هدف خود باید بدانند.

> [!WARNING]
> اطلاعات فوری که نیاز به توجه فوری کاربر برای جلوگیری از مشکلات دارد.

> [!CAUTION]
> توصیه در مورد خطرات یا نتایج منفی اقدامات خاص.

## انواع لیست

### لیست مرتب

1. آیتم اول
2. آیتم دوم
3. آیتم سوم

### لیست نامرتب

- آیتم لیست
- آیتم دیگر
- و آیتم دیگر

### لیست تو در تو

- میوه
  - سیب
  - پرتقال
  - موز
- لبنیات
  - شیر
  - پنیر

## عناصر دیگر — abbr, sub, sup, kbd, mark

<abbr title="Graphics Interchange Format">GIF</abbr> یک فرمت تصویر بیت‌مپ است.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

دکمه <kbd><kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>Delete</kbd></kbd> را فشار دهید تا نشست پایان یابد.

بیشتر <mark>سمندرها</mark> شبانه هستند و حشرات، کرم‌ها و سایر موجودات کوچک را شکار می‌کنند.
