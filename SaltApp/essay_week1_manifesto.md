# 📝 Essay Draft: Why I’m Building Faith-Based Apps in Public
**Author:** Utobivbi Q. Oghenetega  
**Target Publication:** Medium (Week 1 Manifesto)  
**Pillar:** Manifesto / Origin Story  

---

# Why I’m Building Faith-Based Apps in Public (and Why Craft Matters to God)

There’s a trap most creative people fall into when trying to build things that matter.

We split our lives into neat, separate boxes:
* Over here is our **faith** — personal, spiritual, quiet.
* Over there is our **craft** — our design systems, code architectures, UX research, and AI workflows.
* And somewhere in between is our **content** — whatever we post to stay relevant online.

For a long time, I felt that tension. In the indie hacker and tech space, people talk endlessly about MRR, growth loops, and vibecoding SaaS apps for secular markets. In faith circles, software is often treated as an afterthought — clunky interfaces, outdated usability, and templates from 2012.

I kept asking myself: **Why should software built for God’s kingdom have worse UX than a food delivery app?**

If we believe our work is an act of stewardship and worship, shouldn't our product craft, usability heuristics, and visual hierarchy be the best available?

That’s why I’m stepping out to do something transparent, public, and focused: **I am building 3 faith-centered apps in public over the next 90 days using AI-assisted development (vibecoding), and I’m documenting everything I learn about faith, UX craft, and product design along the way.**

---

## The Intersection: Faith × Vibecoding × UX Design

I’m not interested in building hobbyist side projects that sit on local hosts. I want to build software with elite user experience — tools that respect human psychology, reduce cognitive friction, and delight users.

Every week as I read through foundational product design literature — from Steve Krug’s *Don’t Make Me Think* to Don Norman’s *Design of Everyday Things* and Wathan & Schoger’s *Refactoring UI* — I will apply those exact usability principles directly into the code.

By leveraging modern AI-assisted development (vibecoding), I can compress what used to take months of engineering into fast, 5-day build cycles. This leaves maximum room to focus on what matters most: **UX discernment, human interaction, and real user feedback.**

---

## Introducing App 1: Salt 🧂

To start this 90-day journey, I’m building **Salt** — a daily challenge & community story app ("Gist Corner").

### The Problem
Most faith apps are passive. We read a devotion, close the tab, and go about our day. But faith was meant to be lived out in real-world action — paying someone’s bus fare, helping a neighbor, or sending an encouraging word to a forgotten friend.

### The UX Solution & Norman-Compliant Heuristics
**Salt** turns daily faith into real-world action through three distinct interaction design pillars. In building this app, I wanted to move away from conventional "lazy software design" (which relies on premature authentication walls, jarring browser alert errors, and clunky layouts) and instead build with strict obedience to **Don Norman’s Interaction Design Heuristics** (*The Design of Everyday Things*):

1. **Deferred Authentication (Eliminating Upfront Friction):**
   A classic Norman principle is minimizing the Gulf of Execution. Most apps force users to sign up before experiencing any value. Salt flips this: users can accept today’s challenge and read Gist testimonies immediately on download. When they do decide to register, they simply create a Streak Profile (Name, Email, Password) and can instantly skip the remaining configuration questions (like reminders and goals) to enter the app directly, keeping signup friction to a minimum.
2. **Physical Constraints & Error Prevention (Alert-Free Interfaces):**
   Norman emphasizes that good design should make errors impossible rather than showing warnings after they occur. Previously, if a user tried to submit a Gist testimony with a blank text field, standard design would display a jarring browser popup telling them to type. In Salt, we implemented semantic/physical constraints: the "Send" and "Create Account" buttons are physically disabled and visually faded (`opacity: 0.35; cursor: not-allowed`) by default. As the user inputs valid data, the buttons dynamically unlock, spring to full color, and glow—preventing submission errors before they can happen.
3. **Viscosity, Real-Time Vector Renders & Gamified Sketching (Liquid Glass & Canvas Loops):**
   Feedback is the system status communicator. Instead of using static image files that suffer from layout lag or browser cache delays, Salt uses real-time vector graphics drawn on HTML5 `<canvas>` elements to represent the active Companion Guide (Blended, Sage, or Guardian). The guide features a glowing heart representing their spiritual soul. When tapped, the lines of the guide animate and "sketch themselves in" before the dialogue speech bubble pops up. Combined with confetti bursts, chimes, and state changes (breathing, cross-legged reflection, or victory jumps), the app responds with a tactile, living feedback loop.

### The Behavioral Thread: Albert Bandura's Social Cognitive Theory
But *why* is Salt structured this way? Why pair a micro-challenge with a testimony feed and an interactive companion character? 

The answer lies in **Albert Bandura’s Social Cognitive Theory**, which is the psychological thread Salt is woven on. Bandura famously showed that human learning and behavior are not just passive reactions to stimuli, but are shaped by a dynamic, reciprocal interaction between the person, their environment, and their behavior (*Reciprocal Determinism*). 

Salt leverages three pillars of Bandura's theory to drive spiritual behavioral activation:
1. **Self-Efficacy through Mastery Experiences:** You don't build self-efficacy—the deep-seated belief in your capability to act—by reading text. You build it through successful action. By offering low-friction daily micro-challenges, Salt builds user confidence in living out their faith, one micro-victory at a time.
2. **Observational Learning & Vicarious Experiences:** Bandura's theory posits that when we see peers succeed, it raises our own self-efficacy. This is why the **Gist Corner** feed is the heartbeat of Salt. Seeing a post from someone down the street sharing how they completed today’s challenge acts as a vicarious experience that models behavior, prompting you to think: *"If they can step out and do it, so can I."*
3. **Interactive Affordance & Reinforcement:** Our environment influences our physiological and emotional states. By integrating the **procedurally drawn Line-Art Companion Guide** that reacts dynamically to user behavior—breathing calmly, folding its arms in deep reflection, and celebrating challenge completion with physical confetti—Salt designs a positive, reinforcing environment that rewards behavioral activation. On tap, the character sketches its outlines live on the canvas, providing a playful, gamified, and responsive interaction.

---

## What to Expect Next

Every week, I’ll be sharing:
* **Build Logs:** Screenshots, prompt workflows, design decisions, and what broke.
* **Faith & Craft Essays:** Reflections on work, stewardship, discernment, and creative calling.
* **Process Teardowns:** Prompt engineering, UI breakdowns, and usability lessons.

Whether you're a builder, a designer, a person of faith, or just someone curious about where AI development is taking product design — welcome. 

Let's build things that matter, with craft that honors God.

— **Utobivbi Q. Oghenetega**  
*Follow along on X [@yourhandle] and subscribe here on Medium for weekly essays.*
