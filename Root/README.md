# Telegram Bot Hosting Bot 🤖

A powerful Telegram bot for hosting and running Python/JS scripts with auto-dependency installation.

## Features ✨
- Upload and run Python (.py) and JavaScript (.js) files
- Auto-install missing Python packages via pip
- Auto-install missing Node.js modules via npm
- ZIP file support with requirements.txt/package.json auto-install
- User file management with limits
- Subscription system with different tiers
- Admin controls and broadcast functionality
- Process management (start/stop/restart/delete)
- Log viewing for running scripts
- Flask web server for keep-alive on Render

## Deployment 🚀

### On Render
1. Fork this repository
2. Go to [Render Dashboard](https://dashboard.render.com)
3. Click "New +" → "Web Service"
4. Connect your GitHub repository
5. Configure:
   - **Name**: telegram-bot-host
   - **Environment**: Python 3
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `python host.py`
6. Add environment variables (if needed):
   - `PORT`: 10000 (auto-set by Render)
7. Click "Create Web Service"

### Environment Variables
No environment variables required - all config is in `host.py`

## Configuration ⚙️
Edit `host.py` to set your own:
- `TOKEN`: Your Telegram Bot Token from @BotFather
- `OWNER_ID`: Your Telegram User ID
- `ADMIN_ID`: Admin User ID
- `YOUR_USERNAME`: Your Telegram username
- `UPDATE_CHANNEL`: Your channel link

## Commands 📋
- `/start` - Start bot and show main menu
- `/uploadfile` - Upload Python/JS/ZIP files
- `/checkfiles` - View and manage your files
- `/botspeed` - Check bot response speed
- `/statistics` - View bot statistics
- `/adminpanel` - Admin panel (admin only)

## File Limits 📁
- Free Users: 20 files
- Subscribed Users: 15 files
- Admins: 99999 files
- Owner: Unlimited

## Security 🔒
- Bot can be locked/unlocked by admins
- File type validation (.py, .js, .zip only)
- File size limit: 20MB
- User isolation with separate folders
- Safe ZIP extraction

## Support 📞
For issues and support, contact: @Its_MeVishall