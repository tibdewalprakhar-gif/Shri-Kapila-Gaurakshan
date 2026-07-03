# श्री कपिला गौरक्षण, शेगांव — वेबसाइट

साधी, जलद व Vercel वर सहज डिप्लॉय होणारी static वेबसाइट (HTML/CSS/JS — कोणतीही बिल्ड स्टेप लागत नाही).

## फाइल्स
- `index.html` — मुख्य पान (About, सेवा, देणगी, संपर्क)
- `style.css` — डिझाईन
- `script.js` — मोबाईल मेनू व वर्ष
- `assets/logo.jpeg` — आपला लोगो
- `vercel.json` — Vercel सेटिंग्स

## वेबसाईटवर आधी अद्ययावत करा (महत्त्वाचे)
1. **फोन नंबर / ईमेल** — `index.html` मध्ये `+910000000000` आणि `info@shrikapilagaurakshan.org` शोधून आपले खरे संपर्क टाका (३ ठिकाणी आहेत: hero बटण नाही, help section, contact section).
2. **बँक खाते तपशील** — "देणगी" (`#help`) विभागातील खाते क्रमांक, IFSC, बँक शाखा व UPI आयडी भरा.
3. **आकडेवारी** — "कार्य" (`#impact`) विभागात सध्या डॅश (—) आहेत; प्रत्यक्ष आकडे टाकल्यास तो विभाग अधिक प्रभावी दिसेल.
4. इच्छा असल्यास प्रत्यक्ष फोटो जोडण्यासाठी `assets` फोल्डरमध्ये images टाकून `index.html` मध्ये संदर्भ द्या.

## स्थानिक पातळीवर पाहण्यासाठी
कोणत्याही टर्मिनलमध्ये या फोल्डरमध्ये जाऊन:
```
python3 -m http.server 8080
```
मग ब्राउझरमध्ये `http://localhost:8080` उघडा.

## Vercel वर डिप्लॉय — सर्वात सोपा मार्ग (GitHub शिवाय)
1. https://vercel.com वर जाऊन खाते बनवा / लॉगिन करा.
2. Dashboard वर **"Add New… → Project"** क्लिक करा.
3. **"Deploy without Git"** किंवा इंटरफेसमधील drag-and-drop बॉक्समध्ये हा संपूर्ण फोल्डर (`shri-kapila-gaurakshan`) ड्रॅग करून टाका.
4. Framework Preset **"Other"** निवडा (कोणताही build command लागत नाही).
5. **Deploy** दाबा — काही सेकंदात लिंक तयार होईल (उदा. `shri-kapila-gaurakshan.vercel.app`).

## Vercel वर डिप्लॉय — GitHub वापरून (भविष्यात बदल करायला सोपे)
1. हा फोल्डर एक नवीन GitHub repository मध्ये अपलोड करा.
2. https://vercel.com वर **"Add New… → Project"** → आपली GitHub repo निवडा.
3. Framework Preset: **Other**, Build Command: रिकामे ठेवा, Output Directory: रिकामे ठेवा (root).
4. **Deploy** दाबा. यानंतर GitHub वर केलेला प्रत्येक बदल आपोआप वेबसाइटवर अपडेट होईल.

## स्वतःचे डोमेन जोडायचे असल्यास
Vercel प्रोजेक्ट → Settings → Domains मध्ये आपले डोमेन (उदा. `shrikapilagaurakshan.org`) टाकून DNS सूचनांचे पालन करा.
