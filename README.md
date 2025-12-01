# Bank   this is navya

# 🚀 **EXERCISE-2: JENKINS EMAIL NOTIFICATION (SHORT VERSION)**

Here are the *exact click-wise steps* to set up *Gmail email notifications in Jenkins* — no confusion, just click → click → type.

---

# ✅ *PART 1 — Install Email Extension Plugin*

### *1. Open Jenkins Dashboard*

→ Click *Manage Jenkins*
→ Click system

### *2. Install plugin*

→ Open *Available* tab
→ Search: *Email Extension Plugin*
→ Tick the checkbox
→ Click *Install without restart*
→ After install, click *Go back to Dashboard*

---

# ✅ *PART 2 — Configure Gmail SMTP (Basic E-mail Notification)*

### *1. Go to main settings*

→ Click *Manage Jenkins*
→ Click *Configure System*

### *2. Find: E-mail Notification*

Scroll down until you see *E-mail Notification*

### *3. Fill settings*

→ In *SMTP server* type: smtp.gmail.com
Advanced → Tick *Use SMTP Authentication*
 → *User Name:* your Gmail (example: [pranavi@gmail.com](mailto:pranavi@gmail.com))
 → *Password:* (leave empty for now)
→ Tick *Use SSL*
→ In *SMTP Port* type: 465
→ (Optional) *Reply-To Address:* your email

### *4. Don’t save yet — go to part 3*

---

# ✅ *PART 3 — Create Gmail App Password*
((((Gmail profile --manage google account--security sigin---2 step verifiucation --enter password
 --app passwords  -- app name =jenkins ok 
 click copy paste password )))
### *1. Open Google account*

→ Visit *myaccount.google.com*

### *2. Security*

→ Click *Security*
→ Scroll to *Signing in to Google*
→ Click *2-Step Verification*
→ Turn it ON (enter OTP)

### *3. Create App Password*

→ After 2-step is on, go back to *Security*
→ Click *App Passwords*
→ Enter password
→ In Select app, choose *Other (Custom name)*
→ Type: Jenkins
→ Click *Generate*

### *4. Copy the 16-digit password*

(Google shows a yellow box with 16 letters)
→ Copy it
→ Save in Notepad

---

# ✅ *PART 4 — Add Gmail Credentials to Jenkins*

### *1. Back to Jenkins → Configure System*

→ Go to *E-mail Notification* again

### *2. Add password*

→ Tick *Use SMTP Authentication*
→ *User Name:* your Gmail
→ *Password:* paste the 16-digit app password

### *3. Save*

→ Scroll bottom → Click *Save*

---

# ✅ *PART 5 — Configure Extended Email Notification*

### *1. Go again*

→ Manage Jenkins
→ Configure System
→ Scroll to *Extended E-mail Notification*

### *2. Fill settings*

→ *SMTP Server:* smtp.gmail.com
→ *Port:* 465
→ Tick *Use SSL*
→ *Credentials:*
 → Click *Add*
 → Enter:
  • Username → Gmail
  • Password → 16-digit app password
 → Click *Add* → Select this credential

### *3. Save*

→ Scroll down → *Save*

---

# ✅ *PART 6 — Test Email from Jenkins*

### *1. Test from Basic Email*

→ Manage Jenkins
→ Configure System
→ Go to *E-mail Notification*
→ Click *Test configuration*
→ Enter your email
→ Click *Test*

### *2. Test from Extended Email*

→ Go to *Extended E-mail Notification*
→ Click *Test configuration*
→ Enter your email
→ Click *Test*

📩 You should get an email from Jenkins.

---

# ✅ *PART 7 — Add Email Notification to a Job*

### *1. Open the Job*

→ Go to *Dashboard*
→ Click your job
→ Click *Configure*

### *2. Add post-build action*

→ Scroll to bottom
→ Click *Add Post-build Action*
→ Select *Editable Email Notification*

### *3. Fill job settings*

→ *Project Recipient List:* enter emails
→ *Triggers:* tick *Failure, **Success, or **Always*
→ *Subject/Content:* leave default or edit
→ Click *Save*

---

# 📌 Done! Jenkins email notification is fully set.

If you want, I can also send:
✔ Screenshot-style instructions
✔ Exact Gmail error fixes (AUTH failed, port blocked, etc.)
✔ Steps for Outlook/Yahoo SMTP too

Just tell me!

---
