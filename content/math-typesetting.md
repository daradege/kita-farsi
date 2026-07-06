+++
title = "قالب‌بندی ریاضی"
date = "2022-10-20"
description = "راهنمای مختصر برای راه‌اندازی KaTeX"
extra.math = true
+++

پوسته Kita از فرمول‌های ریاضی $\LaTeX$ با استفاده از [KaTeX](https://katex.org/) پشتیبانی می‌کند.

<!--more-->

- برای فعال کردن KaTeX به صورت جهانی، پارامتر `extra.math` را در پیکربندی پروژه روی `true` تنظیم کنید.
- برای فعال کردن KaTeX به ازای هر صفحه، پارامتر `extra.math = true` را در frontmatter فایل‌های محتوا درج کنید.

**توجه:** از مرجع آنلاین [Functions Supported TeX](https://katex.org/docs/supported.html) استفاده کنید.

## مثال‌ها

### ریاضی درون‌خطی

```markdown
When $x = \pi$, Euler's formula may be rewritten as $e^{i \pi} + 1 = 0$.
```

When $x = \pi$, Euler's formula may be rewritten as $e^{i \pi} + 1 = 0$.

### ریاضی بلوکی

```markdown
$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } }
$$
```

$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } }
$$
