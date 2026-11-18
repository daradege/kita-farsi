+++
title = "کدهای کوتاه"
date = "2026-11-18"
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

{% raw %}
```markdown
+++
title = "عنوان صفحه شما"

[extra]
mermaid = true
+++
```
{% endraw %}

سپس می‌توانید از کد کوتاه `mermaid()` استفاده کنید:

{% raw %}
```markdown
{% <mermaid> %}

graph TD;
A-->B;
A-->C;
B-->D;
C-->D;

{% </mermaid> %}
```
{% endraw %}

این به صورت زیر نمایش داده می‌شود:

{% <mermaid> %}

graph TD;
A-->B;
A-->C;
B-->D;
C-->D;

{% </mermaid> %}

علاوه بر این، می‌توانید بلوک کد را داخل کد کوتاه `mermaid()` استفاده کنید و بلوک کد نادیده گرفته می‌شود.

بلوک کد از شکستن قالب‌بندی mermaid توسط فرمت‌کننده جلوگیری می‌کند.

{% raw %}
````markdown
{% <mermaid> %}

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

{% </mermaid> %}
````
{% endraw %}

این به صورت زیر نمایش داده می‌شود:

{% <mermaid> %}

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

{% </mermaid> %}

## هشدار

کد کوتاه `admonition()` یک بنر نمایش می‌دهد تا به شما کمک کند توجه را در صفحه خود قرار دهید.

این روش دیگری برای نوشتن هشدار به سبک GitHub است، اما از عناوین سفارشی پشتیبانی می‌کند.

می‌توانید از کد کوتاه `admonition()` به صورت زیر استفاده کنید:

{% raw %}
```markdown
{% <admonition type="note" title="نکته"> %}
هشدار `note`.
{% </admonition> %}
```
{% endraw %}

{% <admonition type="note" title="یادداشت"> %}
هشدار `note`.
{% </admonition> %}

{% <admonition type="tip" title="نکته"> %}
هشدار `tip`.
{% </admonition> %}

{% <admonition type="important" title="مهم"> %}
هشدار `important`.
{% </admonition> %}

{% <admonition type="warning" title="هشدار"> %}
هشدار `warning`.
{% </admonition> %}

{% <admonition type="caution" title="احتیاط"> %}
هشدار `caution`.
{% </admonition> %}

## گالری

کد کوتاه `gallery()` یک گالری تصویر قابل کلیک ساده فقط HTML است که تمام تصاویر را از دارایی‌های صفحه نمایش می‌دهد.

این از [مستندات Zola](https://www.getzola.org/documentation/content/image-processing/) گرفته شده است

{% raw %}
```markdown
{{ <gallery /> }}
```
{% endraw %}

{{ <gallery /> }}

## SVG درون‌خطی

کد کوتاه `inline_svg()` برای جاسازی تصاویر SVG مستقیماً در یک صفحه وب استفاده می‌شود، به جای شامل کردن آنها از طریق تگ `<img>`.

می‌توانید از کدهای کوتاه `inline_svg()` به صورت زیر استفاده کنید:

{% raw %}
```markdown
{% <inline_svg> %}
![Van de Graaf canon](Van_de_Graaf_canon_in_book_design.svg)
{% </inline_svg> %}
```
{% endraw %}

{% <inline_svg> %}
![Van de Graaf canon](Van_de_Graaf_canon_in_book_design.svg)
{% </inline_svg> %}

اگر نمی‌خواهید زیرنویس زیر تصویر نمایش داده شود، می‌توانید متن `alt` تصویر Markdown را به رشته خالی، `Inline SVG`، `inline-svg` یا `inline_svg` تنظیم کنید.

{% raw %}
```markdown
{% <inline_svg> %}
![](Van_de_Graaf_canon_in_book_design.svg)
{% </inline_svg> %}

{% <inline_svg> %}
![Inline SVG](Van_de_Graaf_canon_in_book_design.svg)
{% </inline_svg> %}

{% <inline_svg> %}
![inline-svg](Van_de_Graaf_canon_in_book_design.svg)
{% </inline_svg> %}

{% <inline_svg> %}
![inline_svg](Van_de_Graaf_canon_in_book_design.svg)
{% </inline_svg> %}
```
{% endraw %}

{% <inline_svg> %}
![Inline SVG](Van_de_Graaf_canon_in_book_design.svg)
{% </inline_svg> %}
