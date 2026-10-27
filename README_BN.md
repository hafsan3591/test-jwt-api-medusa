# MEDUSA Free Fire JWT Website (বাংলা গাইড)

এই প্যাকেজে একটি responsive static frontend আছে। এটি নিজে JWT তৈরি করে না; তোমার backend API-তে POST request পাঠিয়ে token response দেখায়।

## ফাইল
- `index.html` — ওয়েবসাইট
- `README_BN.md` — এই নির্দেশনা
- `vercel.json` — Vercel static hosting config

## Backend চালু করা
1. মূল backend প্রজেক্ট: https://github.com/kaifcodec/freefire-jwt-generator-api
2. GitHub-এ **Fork** করো। মূল repo-র `app/`, `ff_proto/`, `requirements.txt`, `run.sh` ইত্যাদি সব ফাইল রাখবে।
3. Render-এ New Web Service তৈরি করে fork করা repository connect করো।
4. Build command: `pip install -r requirements.txt`
5. Start command: `./run.sh`
6. Deploy শেষ হলে Render-এর URL কপি করো। Backend-এ `POST /api/token` endpoint থাকা উচিত।

## Frontend Vercel-এ deploy করা
1. GitHub-এ নতুন repository তৈরি করো (Public/Private যেকোনোটি)।
2. ZIP extract করে `index.html`, `vercel.json`, `README_BN.md` repository-র root-এ upload করো।
3. Vercel-এ ওই repository import করে Deploy করো।
4. Website খুলে `Backend API URL`-এ Render URL বসাও, যেমন `https://your-service.onrender.com` (উদাহরণমাত্র)।
5. নিজের guest UID ও password দিয়ে পরীক্ষা করো।

## গুরুত্বপূর্ণ
- Backend CORS configuration browser request block করলে backend-এ frontend domain অনুমোদন করতে হবে।
- এই frontend credentials localStorage-এ রাখে না এবং password field submit-এর পরে clear করে। Backend/provider অবশ্যই request process করে, তাই শুধুমাত্র বিশ্বাসযোগ্য backend ব্যবহার করো।
- কোনো token/API সফলভাবে live test করা হয়নি। Free Fire protocol পরিবর্তন হলে backend-এর update লাগতে পারে।
- এটি unofficial community project; Garena-এর সঙ্গে affiliated নয়।
