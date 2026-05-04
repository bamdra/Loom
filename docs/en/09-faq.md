# 💬 Common questions

Conversational answers. Skim the ones you care about.

## 🤖 What if I can't read the code it writes?

**You don't need to.**

Your job is to judge whether the *result* works — the webpage, tool, or app it hands you. Open it. If it does what you wanted, great. If not, tell it what's off.

The code in between is its scratch paper. You can ignore it.

## 😱 What if it screws something up — can I undo?

**Yes.**

Everything happens locally, in your project. Nothing gets pushed anywhere. If a round of changes turned out wrong, just say: *"Undo what you just did."* It'll roll back.

> 💡 If your project is already in git, undoing is even safer — you can return to any past version. If you're not familiar with git, ask the agent to set it up for you.

## 🛠️ I've never installed dev tools — can I still use this?

**Yes.**

The first time it tries to do something that needs a tool (like Node.js or Python), it'll notice and ask: *"Want me to walk you through installing it?"* Say yes, and it walks you through, step by step.

You don't need to go googling.

## 🔒 Is this private? Does my stuff get uploaded?

**It's all local.**

- Your project files: **only on your machine**
- The code it writes: **only runs on your machine**
- What you say to the agent: goes to whichever AI service you picked (you'll know which one when you set it up)

If there's something you'd rather not send to an AI service, just don't put it in your message — agents can't see what you don't say.

## 📂 Can I open multiple projects at once?

Yes. Tabs at the top, one per project. Switching doesn't lose progress.

## 🛑 It's working — I want to interrupt

Just type in the panel. It'll stop and listen. To halt completely, press ESC or type `/stop`.

## 🔄 I edited something myself — can it keep going?

Hit the **Sync button** at the top. An agent will glance at the current state and refresh the team's notes. Then it picks up from there.

## ⏰ Can I close the app and come back later?

**Yes.**

No saving needed. Just close. Reopen the same project later and it picks up exactly where you left off.

## 🐢 It's a bit slow

- Check which AI service you're connected to — some big models are just slow
- Break the work into smaller steps, one thing per round
- For bigger jobs, spend more time in the planning chat — once the plan is clear, building is fast

## 🌍 Can I move to another machine and keep going?

The app itself doesn't sync to the cloud. But your project folder contains everything — put it in git, clone on the other machine, reopen, and you're back.

## 🖥️ macOS says "unidentified developer"

Right-click the app icon → **Open**. A "Open anyway" button appears. Confirm once and macOS remembers.

If it says **"damaged"** instead of "unidentified," run this in Terminal:

```
xattr -cr "/Applications/Bamdra Loom.app"
```

## 🪟 Windows says "unknown publisher"

In the SmartScreen popup, click **More info** → **Run anyway**.

## 🐧 Linux: no app icon

AppImages need FUSE on some distros:

```
sudo apt install libfuse2
```

The deb package adds an icon to your system menu automatically.

## 🆙 How do updates work?

The app checks at startup. When a new version is ready, a download button appears in the top bar — one click downloads, then click again to relaunch.

If the auto-download fails, a dialog will pop up — you can retry, or jump to the GitHub releases page and grab the installer manually.
