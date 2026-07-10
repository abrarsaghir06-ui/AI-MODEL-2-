# Ambassador Chatbot — Test Deployment

Ye ek chhota, complete Next.js project hai — sirf testing ke liye. Isko GitHub
pe push karke Vercel se deploy karein, chatbot check karein, aur satisfy hone
ke baad isi 3 files (`app/api/chat/route.ts`, `components/ChatWidget.tsx`,
`lib/knowledge-base.ts`) ko apni **asal ambassador.pk** codebase mein daal dein.

## Deploy Steps (Vercel)

1. Is poore folder ko naye GitHub repo mein push karein:
   ```bash
   git init
   git add .
   git commit -m "ambassador chatbot test"
   git branch -M main
   git remote add origin <aapki-nayi-repo-ka-URL>
   git push -u origin main
   ```

2. https://vercel.com par jayein → "Add New Project" → ye repo select karein

3. Deploy se pehle **Environment Variables** mein add karein:
   ```
   ANTHROPIC_API_KEY = sk-ant-xxxxxxxxxxxxxxxxxxxx
   ```

4. "Deploy" par click karein — 1-2 minute mein live URL mil jayegi
   (jese `ambassador-chatbot-test.vercel.app`)

5. Us URL kholein, neeche-daaeen chat bubble (💬) par click karein, aur sawal
   pochein — jese "custom kitchen kaise order karein?"

## Local pe test karna ho to

```bash
npm install
# .env.local file banayein aur ANTHROPIC_API_KEY=sk-ant-xxxx likhein
npm run dev
```
Phir http://localhost:3000 kholein.
