# CSS Not Loading - Fix Instructions

## Quick Fix:

1. **Stop the dev server** (Ctrl+C in terminal)

2. **Clear Next.js cache:**
   ```bash
   rm -rf .next
   ```

3. **Restart dev server:**
   ```bash
   npm run dev
   ```

4. **Hard refresh browser:**
   - Mac: Cmd + Shift + R
   - Windows/Linux: Ctrl + Shift + R

## If still not working:

1. **Check if Tailwind is installed:**
   ```bash
   npm list tailwindcss
   ```

2. **Reinstall dependencies:**
   ```bash
   rm -rf node_modules package-lock.json
   npm install
   ```

3. **Verify CSS file exists:**
   ```bash
   ls -la app/globals.css
   ```

4. **Check browser console** for CSS loading errors

## Common Issues:

- **CSS file not found**: Make sure `app/globals.css` exists
- **Tailwind not compiling**: Check `tailwind.config.ts` content paths
- **Cache issue**: Clear `.next` folder and restart
- **Port conflict**: Try different port: `npm run dev -- -p 3001`

