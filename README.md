# Household Finance V1
Web app React/Vite + Supabase + Netlify Function Telegram.

## Local
npm install
copy .env.example .env
npm run dev

Without Supabase env, the UI opens in demo mode. With Supabase env, login is required.

## Supabase
Create a project, run `supabase/schema.sql` in SQL Editor, enable Email/Password auth, create a user, then add accounts for that user.

## Netlify
Connect GitHub repository. Build: `npm run build`; Publish: `dist`. Set VITE_SUPABASE_URL and VITE_SUPABASE_ANON_KEY. For Telegram function set TELEGRAM_BOT_TOKEN, SUPABASE_URL and SUPABASE_SERVICE_ROLE_KEY. Set webhook to https://YOUR-DOMAIN/.netlify/functions/telegram-webhook

IMPORTANT: service role key is server-side only. Telegram account linking is intentionally not auto-enabled in V1; V2 should use a one-time pairing code.
