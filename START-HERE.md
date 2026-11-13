# Start Here — First Computer Session

You do not need to know coding to start. Follow these steps in order.
If anything errors, copy the exact error message and ask for help.

## What you need
- A computer (Windows or Mac)
- Your GitHub account: natewyre13
- A free Vercel account (for hosting) — create it with GitHub login later

## Step 1: Install 3 free tools
1. Node.js LTS version 22 or newer: https://nodejs.org (download LTS)
   This repo needs Node >= 22.22.3. After install, check it:
   `node --version` should show v22 or higher.
2. VS Code: https://code.visualstudio.com
3. Git: https://git-scm.com/downloads (Windows: accept defaults)

## Step 2: Get the code onto your computer
Open a terminal (Windows: PowerShell. Mac: Terminal) and run:

```
git clone https://github.com/natewyre13/astrowind.git
cd astrowind
npm install
```

`npm install` downloads the template's parts. It takes a few minutes
the first time. Warnings are normal. Errors in red are not — copy them
if you see any.

## Step 3: Run it locally
```
npm run dev
```
Open the address it prints (usually http://localhost:4321) in your
browser. You should see the AstroWind demo site. That means setup works.
Press Ctrl+C in the terminal to stop it.

## Step 4: Deploy a blank site (so you have a live link)
1. Go to https://vercel.com and sign in with GitHub.
2. Add New Project, import `natewyre13/astrowind`.
3. Accept the defaults (Astro is detected automatically) and Deploy.
4. You will get a live `*.vercel.app` link. It will show the demo site
   for now. That is expected. We replace the demo pages next.

## Step 5: Tell Muse it works
Reply in the Side Gig Money chat with:
- "Dev server works" and/or your Vercel link
- Any error messages, if you hit any

Then we build the calculator page together, one small change at a time.

## Optional: rename the repo
This repo is currently named `astrowind` because it is a fork. You can
rename it on GitHub under Settings > General to something like
`window-cleaning-quote-calculator`. GitHub keeps old links working.
Rename BEFORE you clone if you want the folder name to match, or leave
the name as-is — the name does not affect the website. Do not rename
in the middle of a build session without saying so, or the folder
and remote will get out of sync.
