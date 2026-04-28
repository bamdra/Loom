# 🧭 Saying what you want, well

"Intent" is just **the sentence you say to it about what you want**.

It's not a homework assignment. It's not a tech spec. **It's the thing you want, in your own words.** Three examples follow — small, medium, big — to show how much to say.

> 💡 **Not knowing exactly what you want is normal.** If you only have a vague idea, don't push yourself — just say *"I roughly want X, but I haven't decided about Y."* It will ask you back. **The questions it asks are exactly what you need to answer.**

## 🪶 Light: one sentence is plenty

> On my reading-quotes page, add a "what I read today" button in the top-right.

Things like this:
- Crisp boundary (one button)
- No real choice to weigh
- You just want it done

That's enough. **Adding more constraints will only make it fuss in places you don't care about.**

## 🌿 Medium: hand over the context

> My reading-quotes page groups entries by topic right now. I want to add a "view by month" mode —
> - Each entry already has a timestamp stored
> - Don't break the existing topic view; the two should coexist
> - For the month view, I want a calendar-grid look

Things like this:
- Touch several places
- You have **preferences it can't guess** ("calendar-grid look")
- You have **untouchables** ("don't break the topic view")

Longer, but each line is **something it couldn't infer without seeing your head**. Constraints tell it where *not* to step. They don't decide *how*.

## 🌳 Heavy: lay the open questions on the table

> I want to grow my personal quotes tool into a small social space — friends can log in, see things I've marked public, leave comments.
>
> Background:
> - All my data is in the browser today; there's no concept of "user"
> - Friends should see entries I've marked "public" and be able to comment
> - Keep it simple — no likes, no follows
>
> Open questions I haven't decided:
> - Email login or something like Google
> - "Public" toggled per-entry, or per-topic
> - Whether the data should move from the browser to a real server
>
> Let's talk through the plan first, then build.

For **bigger things**, intent should actually be a little fuzzy — explicitly listing what you haven't decided. That tells it *these are the bits we discuss together*.

If you nail every detail up front, it'll just follow. Halfway through you'll find a choice was wrong, and undoing is painful.

## 🎯 What all three share

- ✅ **Write what you already know**: how things look today, what can't change, your preferences
- ❌ **Don't pre-decide for it**: unless you really do have a strong preference, leave the *how* for the planning chat
- ❓ **Mark what's open**: anything you're not sure about, say so — let it ask you

Intent isn't best when it's longest, and not when it's shortest. **It matches the size of the thing.** Small task: one line. Big task: lay out background and uncertainties.

## 🔁 When it goes off-course

The fastest fix isn't to wipe and redo. It's to tell it: **"This drifted off, here's why — X."**

It will adjust based on what's already there, more accurately than starting over — without throwing away the good parts.

---

# 🛠️ Advanced (optional reading)

> 📌 **You won't need this section 99% of the time. Skip it freely.**
>
> This is for the *"I'm curious what's happening underneath"* crowd. It doesn't change how you use Loom.

If you've opened the file tree on the left, you'll see folders and files. They're either the team's "meeting notes" or the project itself.

- **File tree on the left** — every file in the project. Click to view contents.
- **Editor in the middle** — file contents show up here when clicked. You can peek to see what an agent changed; you can also edit (not recommended — the agent loses track until you press Sync).
- **Bottom panel** — defaults to the intent box (where you talk to the agent). The command-line tab is there for people who like it. **If you don't, ignore it.**

### A few special files you might notice

They live in a folder called `.vibeflow`. Opening them is fine; ignoring them is also fine:

- A list of **what's being worked on right now**
- A description of **the overall plan**
- A snapshot of **current progress**

Agents pass information through these files. **Updating them is the agents' job**, not yours.

### Undo · roll back

If a round of changes turns out wrong — everything is on your machine, in your project. You can undo without leaving a mess. If you're not sure how, just say to the agent: *"Roll back what you just did."* It'll handle it.

### Setting up tools

If it tells you *"I need X to keep going"* — you don't need to go look up how to install it. Just say: *"Walk me through installing it."* It will.
