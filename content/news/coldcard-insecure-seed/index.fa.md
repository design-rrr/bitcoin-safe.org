---
title: "Seed ناامن COLDCARD"
date: "2026-08-02"
draft: false
description: "راهنمایی کوتاه برای انتقال دارایی از Seed ساخته‌شده روی دستگاه Coinkite."
---

[Coinkite یک ضعف در تولید Seed در firmwareهای آسیب‌پذیر COLDCARD را افشا کرده است](https://blog.coinkite.com/coldcard-mk3-seed-generation-warning/). همچنین [تحلیل فنی Block درباره fallback قابل پیش‌بینی RNG و reseed سی‌ودوبیتی](https://engineering.block.xyz/blog/predictable-rng-fallback-and-32-bit-reseed-in-coldcard-firmware) را ببینید. به‌روزرسانی firmware یک Seed موجود را اصلاح نمی‌کند.

**اگر Seed را با هر محصول Coinkite ساخته‌اید، هرچه زودتر مهاجرت کنید!**

## چک‌لیست مهاجرت

1. روی یک **دستگاه امضاکننده غیر از COLDCARD** ([دستگاه‌های پشتیبانی‌شده را ببینید]({{< ref "library/supported-hardware-signers" >}}))، با راه‌انداز Bitcoin-Safe یک wallet کاملاً جدید بسازید: یک [wallet تک‌امضایی]({{< ref "library/setup-singlesig-wallet" >}}) یا [wallet چندامضایی]({{< ref "library/setup-multisig-wallet" >}}) را انتخاب کنید. Seed قدیمی را دوباره استفاده نکنید.
   - اگر هیچ امضاکننده سخت‌افزاری غیر از COLDCARD در دسترس نیست، [MetroVault]({{< ref "library/supported-hardware-signers/metrovault" >}}) روی یک دستگاه Android اختصاصی که به تنظیمات کارخانه بازنشانی شده، آفلاین نگه داشته می‌شود و فقط برای امضا استفاده می‌شود، یک گزینه است.
   - آزمون دریافت و ارسال راه‌انداز را کامل کنید تا مطمئن شوید wallet جدید درست راه‌اندازی شده است: نسخه پشتیبان و یک آدرس دریافت را روی امضاکننده جدید بررسی کنید، مقدار کمی برای آزمایش دریافت کنید و آن را با موفقیت به یک آدرس تأییدشده دیگر در همان wallet جدید بفرستید.
2. تراکنش مهاجرت را امضا کنید، اما **آن را به روش معمول پخش نکنید**. تراکنش خام امضاشده را کپی کنید و مستقیماً از طریق [MARA Slipstream](https://slipstream.mara.com/) بفرستید تا مدت قرار گرفتن کلیدهای عمومی wallet قدیمی در mempool عمومی کاهش یابد.
3. COLDCARD قدیمی را تا زمانی که تمام موجودی به wallet جدید رسیده و تأیید شده است نگه دارید، سپس firmware آن را به آخرین نسخه ارتقا دهید.

اگر به کسی برای مهاجرت کمک می‌کنید، هرگز از او نخواهید کلمات Seed را به اشتراک بگذارد، عکس بگیرد یا تایپ کند. Seed باید خصوصی بماند و فقط روی دستگاه امضاکننده وارد شود.
