# NY Bot Host
Production-oriented Telegram bot hosting SaaS foundation for Supabase + Render.

Features: Supabase auth, user dashboard, admin role, bot token verification, Python/Node projects, source/editor UI, env/deployment model, logs/metrics schema, subscriptions, audit logs, and Render provisioning hook.

Never expose SUPABASE_SERVICE_ROLE_KEY, RENDER_API_KEY, or ENCRYPTION_KEY to the browser.

1. Run `supabase/migrations/001_platform.sql` on the existing project.
2. Configure server env.
3. `npm install && npm run build && npm start`.
4. Push to GitHub and connect Render using `render.yaml`.
5. For real customer bot isolation, provision one Render service per bot through the private worker/provider adapter; do not execute arbitrary uploaded code inside the control-plane web process.
