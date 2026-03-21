---
id: ac3f887c-299a-4087-8939-c1b40b1d1791
title: Component generator template
created_at: 2026-02-19T02:13:50.917Z
datetime: 2026-02-19T02:13:50.917Z
tags: []
context: {"deviceName":"Emmanuels-MacBook-Pro.local","hostname":"Emmanuels-MacBook-Pro.local","activeApp":"Google Chrome","timeOfDay":"night","timestamp":"2026-02-19T02:13:50.920Z"}
aiMetadata: {"topics":["relationships"],"universals":["actionable","reference","idea","reflection","question"],"confidence":0.9972081787170737,"keywords":["svelte","paste","component","prompt","components"],"modelVersion":"distilbert-mnli","processedAt":"2026-02-19T02:13:54.911Z"}
---

This is the final piece of your "Factory." To make this work, you need a prompt that doesn't just give you generic text, but actually outputs **structured Svelte components** that you can copy/paste directly into your chassis.

Here is the master prompt you will use with your AI of choice (Claude, ChatGPT, etc.) once the Tally form results come in.

---

### **The "Svelte-Scale" Component Generator Prompt**

**System Role:**

> You are an expert Frontend Engineer specializing in **SvelteKit**, **Tailwind CSS**, and **Conversion Rate Optimization (CRO)**. Your goal is to take raw client data and turn it into high-performance, accessible, and beautiful Svelte components.

**The Input Data:**

> [PASTE TALLY FORM RESPONSES HERE]

**The Task:**

> Based on the provided data, generate the following code blocks for a SvelteKit page. Use **Tailwind CSS** for all styling. Ensure the "Vibe" requested is reflected in the spacing, typography, and color shades.
> 1. **The Hero Section:** Create a high-converting Hero. Include a headline that focuses on the "Problem" and "Solution" provided. Add a primary CTA button using the "Call to Action" input.
> 2. **The Services Grid:** Generate a 3-column grid of Svelte components for the "Top 3 Services." Each should have a placeholder for an icon and a punchy description.
> 3. **The 'Why Us' Section:** Write a section that highlights the client's unique value proposition (e.g., PSU background, local experience).
> 4. **The Social Proof:** A clean testimonial slider or grid component using the provided shout-outs.
> 5. **SEO Metadata:** Provide a `<svelte:head>` block with a optimized Title and Meta Description for Local SEO (referencing their location).
> 
> 

**Style Guidelines:**

> * **Vibe:** [INSERT VIBE FROM FORM, e.g., "Rugged/Professional"]
> * **Colors:** Use Tailwind's [INSERT COLOR, e.g., "Slate"] for neutrals and [INSERT COLOR, e.g., "Blue"] for primary accents.
> * **Code Style:** Use semantic HTML5. Ensure all images have `alt` tags based on the context. Keep the code modular so I can paste it into separate `.svelte` files.
> 
> 

---

### **How to Use This in Your Workflow**

1. **The Trigger:** You get an email from Tally.so saying a new contractor has signed up.
2. **The Input:** Copy the text from their answers.
3. **The Generation:** Paste the Master Prompt + their answers into the AI.
4. **The Assembly:** * Paste the Hero code into `src/lib/components/Hero.svelte`.
* Paste the Services into `src/lib/components/Services.svelte`.
* Run `npm run dev` to see the magic.


5. **The Polish:** Spend 15 minutes swapping out the placeholder images with the ones they uploaded to Tally.

### **Pro-Engineer Tip: The "Variable" Shortcut**

In your Svelte Chassis, you can set up a `theme.js` or `constants.js` file. Instead of having the AI generate the colors every time, have it generate the **content**, and let your CSS variables handle the "look" to ensure every site you build is consistently high-quality.

---

### **Final Checklist: You are officially ready to launch.**

* [x] **Niche Identified:** Contractors & Independent Coaches.
* [x] **Tech Stack:** Svelte + Cloudflare + GitHub.
* [x] **Onboarding:** Tally.so "Content Gateway" is drafted.
* [x] **Pricing:** $499 setup / $89 monthly "Partner" fee.
* [x] **Sales Pitch:** "Process Engineer" authority & Speed-based lead magnets.
* [x] **The Factory:** AI prompt ready to turn data into code.

**What’s the very first thing you're going to do? Should I help you find those first 5 target businesses in York to start the "Lead Magnet" mockups?**
