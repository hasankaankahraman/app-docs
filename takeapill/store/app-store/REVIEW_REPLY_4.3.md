# App Review yanıtı (Guideline 4.3(a), spam)

Build 1.0.0 (3) ile birlikte gönderilir. İngilizce metni "Reply to App Review"
alanına, kısa sürümünü de App Review Information > Notes alanına yapıştırın.
Ret sürerse aynı metinle App Review Board'a itiraz edin
(developer.apple.com/contact/app-store/?topic=appeal).

## Göndermeden önce (App Store Connect)

- [ ] Apple Developer > Identifiers: `com.takeapill.takeapill` ve
      `com.takeapill.takeapill.TakeAPillWidget` için App Groups açık,
      `group.com.takeapill.takeapill` ikisine de atanmış (Xcode otomatik
      imzalama bunu ilk cihaz derlemesinde yapar).
- [ ] Birincil dil: English (U.S.); Türkçe yerelleştirme ekli.
- [ ] Ad, alt başlık, anahtar kelimeler, açıklama, promosyon metni:
      `store/app-store/metadata/en-US` ve `metadata/tr`.
- [ ] Ekran görüntüleri: `store/app-store/iphone-6.9/<en|tr>` ve
      `ipad-13/<en|tr>` (6.3" seti kaldırıldı; 6.9" ölçeklenir).
- [ ] Gizlilik etiketi değişmez: Data Not Collected.
- [ ] Gerçek cihazda: widget ekle, "Aldım"a bas (uygulama kapalıyken de),
      alarm modunda kilit ekranı, PDF rapor paylaşımı.

---

Hello,

Thank you for the review. We've taken the feedback seriously and this build
substantially expands what makes Take a Pill different. The app is written
from scratch by me in Flutter with native Swift code (WidgetKit, AlarmKit,
App Intents); no purchased template or white-label code is used, and this is
currently my only app on the App Store.

**What sets it apart from other medication reminders:**

1. **Meal-anchored scheduling.** Users set their daily routine once (wake-up,
   breakfast, lunch, dinner, bedtime) and enter doses relative to it, e.g.
   "30 minutes before breakfast". Times are calculated from the routine and
   move automatically when it changes.
2. **Interactive Home Screen and Lock Screen widget (new).** Shows today's
   progress and the next doses; a "Taken" button marks a dose directly from
   the Home Screen via an App Intent, cancels that dose's pending reminders
   and alarm, and syncs to the app's history and stock.
3. **Real alarms with AlarmKit (iOS 26+).** Doses can ring as system alarms on
   the Lock Screen and in the Dynamic Island, with Snooze and Open.
4. **Visual pill builder (new).** Users draw each medication as it really
   looks (shape, one or two colors, score line), shown in lists and the
   widget, to avoid mixing up similar pills.
5. **Stock and expiry tracking (new).** Each "Taken" is subtracted from the
   stock; the app forecasts the run-out date from the schedule, alerts ahead
   of time with a shortcut to nearby pharmacies in Maps, and reminds before
   the expiry date.
6. **PDF adherence report (new).** A 7/30/90-day report with overall
   adherence, taken/skipped/missed doses per medication and a daily chart,
   generated on device and shared via the share sheet (e.g. to a doctor).
7. **English and Turkish (new)**, following the system language, with an
   in-app language setting.
8. **Fully on-device.** No account, server, ads or analytics.

**How to review the distinctive parts (no login needed):**
1. Complete onboarding; choose "Alarm" to see AlarmKit on iOS 26.
2. Add a medication: on the Dose step pick a shape and colors; on the
   Schedule step choose "When: Breakfast, 30 min before"; on the Duration
   step turn on "Track stock" with a small number (e.g. 3).
3. The Today screen shows a "running low" card with Add box / Find a pharmacy.
4. Add the "Take a Pill" widget to the Home Screen and tap "Taken".
5. History > share button creates the PDF report.

If any specific part of the app or its metadata still appears similar to
another app, I'd be grateful to know which, so I can address it directly.

Thank you,
Hasan Kaan Kahraman

---

## Notes alanı için kısa sürüm

Original app, no template. Distinct features: meal-anchored scheduling,
interactive Home/Lock Screen widget with a "Taken" App Intent, AlarmKit
alarms (iOS 26), visual pill builder, stock forecast with pharmacy shortcut
and expiry reminders, on-device PDF adherence report, English/Turkish. No
account needed. To try: add a medication with "Track stock" = 3, then add
the widget and tap "Taken".
