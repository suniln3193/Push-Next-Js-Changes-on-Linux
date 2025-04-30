
# Deploying Next.js Updates on a Linux Server

Follow these steps to update and deploy your Next.js site hosted on a Linux server (VPS).

---

## Step 1: SSH into the Linux Server
```bash
ssh username@your-server-ip
```

---

## Step 2: Navigate to Your Project Folder
```bash
cd /path/to/your/nextjs-app
```

---

## Step 3: Pull Latest Code from Git
```bash
git pull origin main  # or the correct branch
```

---

## Step 4: Install Dependencies
```bash
npm install
```

---

## Step 5: Build the App
```bash
npm run build
```

---

## Step 6: Restart the App Server

### If using PM2:
```bash
pm2 restart your-app-name
```

### If using next start with screen/tmux:
```bash
# Stop current process
Ctrl+C  # inside screen/tmux

# Start again
npm run start
```

---

## Optional: Setup PM2 (if not already)
```bash
npm install -g pm2
pm2 start npm --name "nextjs-app" -- start
pm2 save
pm2 startup
```

---

## Done!
Your site should now reflect the latest changes.
