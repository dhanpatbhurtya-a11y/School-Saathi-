SCHOOL SAATHI — SINGLE SCHOOL PACKAGE
=====================================
यह पैकेज सिर्फ Govt. Sen. Sec. School Asa Khera के मौजूदा School Saathi HTML सॉफ्टवेयर के लिए है। इसमें multi-school login या cloud database नहीं जोड़ा गया है।

फाइलें:
- index.html: मौजूदा software + PWA metadata/service worker registration
- manifest.webmanifest: मोबाइल पर installable app की जानकारी
- service-worker.js: वेबसाइट के shell को offline cache करने की शुरुआत

कैसे चलाएँ:
1. ZIP extract करें।
2. वेबसाइट के रूप में चलाने के लिए इन फाइलों को HTTPS hosting पर upload करें (उदाहरण: Firebase Hosting / GitHub Pages)।
3. वेबसाइट को Chrome Android में खोलें; browser menu में "Install app" या "Add to Home screen" विकल्प दिख सकता है।
4. Offline shell caching तभी काम करेगी जब साइट पहली बार internet के साथ खुली हो और service worker सफलतापूर्वक install हुआ हो।

जरूरी सीमाएँ:
- यह package अभी public/live website पर deploy नहीं हुआ है।
- Service worker सिर्फ app shell cache करता है; यह database sync नहीं बनाता।
- मूल software का localStorage/browser data उसी device/browser तक सीमित है। दूसरे मोबाइल/कंप्यूटर पर अपने-आप नहीं आएगा।
- अगर मूल HTML में external dependencies/remote content हों तो वे offline में उपलब्ध न भी हों।
- एक school के लिए इस्तेमाल में student records की backup व्यवस्था रखें; browser data clear होने पर local records खो सकते हैं।
- बाद में चाहें तो सुरक्षित cloud database + sign-in + cross-device sync जोड़ा जा सकता है, पर पहले उसे अलग से implement/test करना होगा।
