# TheFeed Clients Mirror

This repository mirrors the **client** binaries from
[`sartoopjj/thefeed`](https://github.com/sartoopjj/thefeed) releases so they
can be downloaded as a single ZIP from GitHub.

The current version in this repo is recorded in [`clients/VERSION`](clients/VERSION).

---

##  راهنمای دانلود (فارسی)

### ⚡️ روش سریع (لینک مستقیم)

کافی است روی لینک زیر کلیک کنید تا کل مخزن (شامل تمامی فایل‌های کلاینت) به‌صورت یک فایل ZIP دانلود شود — نیازی به کلیک روی دکمهٔ **Code** نیست:

👉 **[دانلود مستقیم همهٔ کلاینت‌ها (ZIP)](https://github.com/sartoopjj/thefeed-files/archive/refs/heads/main.zip)**

```
https://github.com/sartoopjj/thefeed-files/archive/refs/heads/main.zip
```

پس از پایان دانلود، فایل ZIP را از حالت فشرده خارج کنید؛ تمامی فایل‌های کلاینت داخل پوشهٔ `clients/` قرار دارند.

### 🖱️ روش جایگزین (از طریق دکمهٔ Code)

اگر مایل به استفاده از رابط گرافیکی گیت‌هاب هستید:

1. به بالای همین صفحه بروید و روی دکمهٔ سبز رنگ **`Code`** کلیک کنید.
2. در منوی بازشده، روی گزینهٔ **`Download ZIP`** کلیک کنید.
3. پس از پایان دانلود، فایل ZIP را از حالت فشرده خارج کنید.
4. تمامی فایل‌های کلاینت داخل پوشهٔ `clients/` قرار دارند.

> راهنمای تصویری مرحله به مرحله:
>
> - 🟢 کلیک روی دکمهٔ **Code** (گوشهٔ بالا-راست لیست فایل‌ها)
> - 📥 کلیک روی **Download ZIP**
> - 📂 باز کردن فایل ZIP و رفتن به پوشهٔ `clients`

### فایل‌های موجود در پوشهٔ `clients/`

| پلتفرم | معماری | نام فایل |
| --- | --- | --- |
| Android (APK) | arm64 | `thefeed-android-vX.Y.Z-arm64.apk` |
| Android (binary) | arm | `thefeed-client-android-arm` |
| Android (binary) | arm64 | `thefeed-client-android-arm64` |
| macOS | Intel | `thefeed-client-vX.Y.Z-darwin-amd64` |
| macOS | Apple Silicon | `thefeed-client-vX.Y.Z-darwin-arm64` |
| FreeBSD | amd64 | `thefeed-client-vX.Y.Z-freebsd-amd64` |
| FreeBSD | arm64 | `thefeed-client-vX.Y.Z-freebsd-arm64` |
| Linux | amd64 | `thefeed-client-vX.Y.Z-linux-amd64` |
| Linux | arm64 | `thefeed-client-vX.Y.Z-linux-arm64` |
| Windows | amd64 | `thefeed-client-vX.Y.Z-windows-amd64.exe` |

> فایل‌های مربوط به **سرور** (`thefeed-server-*`) در این مخزن قرار داده نمی‌شوند؛ اگر به نسخهٔ سرور نیاز دارید مستقیماً از صفحهٔ Releases پروژهٔ اصلی دریافت کنید.

---

## 🔄 Updating the clients (maintainer)

The clients are refreshed by a manually-triggered GitHub Action.

1. Open the **Actions** tab of this repository.
2. Choose the workflow **📦 Download TheFeed Clients** in the left sidebar.
3. Click **Run workflow**.
4. Leave the `tag` input **empty** to fetch the latest published release, or
   type a specific tag (e.g. `v0.12.2`) to pin to that version.
5. Click the green **Run workflow** button.

The workflow will:

- Look up the requested release on `sartoopjj/thefeed`.
- Delete the existing `clients/` directory (old versions are removed).
- Download every client asset (`thefeed-client-*` and `thefeed-android-*`).
- Write the tag into `clients/VERSION`.
- Commit and push the result back to this repository.

Server binaries and source archives are intentionally skipped.
