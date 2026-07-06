+++
title = "کدهای کوتاه"
date = "2022-10-20"
description = "کدهای کوتاه پوسته Kita."
[taxonomies]
tags = ["markdown", "css", "html"]
[extra]
mermaid = true
+++

پوسته Kita چندین کد کوتاه ارائه می‌دهد.

تا به حال درباره کدهای کوتاه نشنیده‌اید؟ برای اطلاعات بیشتر [مستندات Zola](https://www.getzola.org/documentation/content/shortcodes/) را ببینید.

## Mermaid

برای استفاده از Mermaid در صفحه خود، باید `extra.mermaid = true` را در frontmatter صفحه تنظیم کنید.

```markdown
+++
title = "عنوان صفحه شما"

[extra]
mermaid = true
+++
```

سپس می‌توانید از کد کوتاه `mermaid()` استفاده کنید:

```markdown
{%/* mermaid() */%}

graph TD;
A-->B;
A-->C;
B-->D;
C-->D;

{%/* end */%}
```

این به صورت زیر نمایش داده می‌شود:

{% mermaid() %}

graph TD;
A-->B;
A-->C;
B-->D;
C-->D;

{% end %}

علاوه بر این، می‌توانید بلوک کد را داخل کد کوتاه `mermaid()` استفاده کنید و بلوک کد نادیده گرفته می‌شود.

بلوک کد از شکستن قالب‌بندی mermaid توسط فرمت‌کننده جلوگیری می‌کند.

````markdown
{%/* mermaid() */%}

```mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
```

{%/* end */%}
````

این به صورت زیر نمایش داده می‌شود:

{% mermaid() %}

```mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
```

{% end %}

## هشدار

کد کوتاه `admonition()` یک بنر نمایش می‌دهد تا به شما کمک کند توجه را در صفحه خود قرار دهید.

این روش دیگری برای نوشتن هشدار به سبک GitHub است، اما از عناوین سفارشی پشتیبانی می‌کند.

می‌توانید از کد کوتاه `admonition()` به صورت زیر استفاده کنید:

```markdown
{%/* admonition(type="note", title="نکته") */%}
هشدار `note`.
{%/* end */%}
```

{% admonition(type="note", title="یادداشت") %}
هشدار `note`.
{% end %}

{% admonition(type="tip", title="نکته") %}
هشدار `tip`.
{% end %}

{% admonition(type="important", title="مهم") %}
هشدار `important`.
{% end %}

{% admonition(type="warning", title="هشدار") %}
هشدار `warning`.
{% end %}

{% admonition(type="caution", title="احتیاط") %}
هشدار `caution`.
{% end %}

## گالری

کد کوتاه `gallery()` یک گالری تصویر قابل کلیک ساده فقط HTML است که تمام تصاویر را از دارایی‌های صفحه نمایش می‌دهد.

این از [مستندات Zola](https://www.getzola.org/documentation/content/image-processing/) گرفته شده است

```markdown
{{/* gallery() */}}
```

{{ gallery() }}

## SVG درون‌خطی

کد کوتاه `inline_svg()` برای جاسازی تصاویر SVG مستقیماً در یک صفحه وب استفاده می‌شود، به جای شامل کردن آنها از طریق تگ `<img>`.

می‌توانید از کدهای کوتاه `inline_svg()` به صورت زیر استفاده کنید:

```markdown
{%/* inline_svg() */%}
![Van de Graaf canon](Van_de_Graaf_canon_in_book_design.svg)
{%/* end */%}
```

{% inline_svg() %}
![Van de Graaf canon](Van_de_Graaf_canon_in_book_design.svg)
{% end %}

اگر نمی‌خواهید زیرنویس زیر تصویر نمایش داده شود، می‌توانید متن `alt` تصویر Markdown را به رشته خالی، `Inline SVG`، `inline-svg` یا `inline_svg` تنظیم کنید.

```markdown
{%/* inline_svg() */%}
![](Van_de_Graaf_canon_in_book_design.svg)
{%/* end */%}

{%/* inline_svg() */%}
![Inline SVG](Van_de_Graaf_canon_in_book_design.svg)
{%/* end */%}

{%/* inline_svg() */%}
![inline-svg](Van_de_Graaf_canon_in_book_design.svg)
{%/* end */%}

{%/* inline_svg() */%}
![inline_svg](Van_de_Graaf_canon_in_book_design.svg)
{%/* end */%}
```

{% inline_svg() %}
![Inline SVG](Van_de_Graaf_canon_in_book_design.svg)
{% end %}
