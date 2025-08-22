
# How to write great library items

Library items are the building blocks of your guest messages. They contain the information Alfred uses to communicate with guests.

For simple items like the **WiFi name** or **WiFi password**, you can simply enter a short value.

But when it comes to more complex information — such as the location of a device or instructions to troubleshoot an appliance — it’s important to write content that is clear, helpful, and easy to reuse.

> **IMPORTANT** While Alfred is very good at understanding your input, reading this guide will help you get the most out of it. If you’re unsure about your writing, don’t worry — Alfred is great at finding connections and interpreting your instructions with high accuracy!


## ✅ General principles

</br>

### 🎯 Start from the guest’s perspective

Think about:
- What is the guest trying to do?
- When will they need this information?
- Should this item instruct, inform, reassure, or guide?

> **Example** **Location of hot water controls**: “Under the boiler in the bathroom”

### 📍 Be precise about locations

Always write **clear, detailed locations** that help guests find things without asking.

> **Example** ❌ “In the kitchen”  
> ✅ “Inside the cabinet under the kitchen sink”

### 🖼️ Add photos and videos only when necessary

Images and videos are useful **only if** they make the explanation easier. Avoid overwhelming guests with unnecessary media.

Use dedicated fields like **photo**, **video**, or **instructions**. Don’t paste links inside the description.

## 🗣️ Tone of voice

</br>

### 📌 Use a friendly, neutral tone

Write as if you're explaining something to a guest in person. Be clear, but don’t overthink it. Avoid using all caps, abbreviations, or internal jargon.

> **Example** ❌ “Private parking: yes at corner”  
> ✅ “Private parking is available just around the corner from the building”

### 📌 Avoid vague words

Be direct. Don’t use words like “available”, “present”, or “see photo” — they don’t actually tell the guest where to look or what to do. Instead, give clear and specific details.

> **Example** ❌ “A hairdryer is available in the bathroom”  
> ✅ “You’ll find the hairdryer in the cabinet under the sink”


## 🪡 Writing custom items

</br>

### 💡 Think in placeholders

Write your items so they work seamlessly inside guest messages.

> **Example** 
> - **Garbage collection times**: “from 6:30 PM to 10:30 PM”  
> - **Guest message**: “Please remember that trash can be taken out {garbage_collection_times}.”

### 🥵 Don’t overload one item

Each library item should focus on **one clear piece of information**. Standard items are meant to hold just one piece of content. When creating custom items, make sure to separate different types of information into separate entries.

> **Example**  ❌ **Hot water information**: “Boiler above the bidet. Button below. If no hot water, open valve under kitchen sink.”  
>  </br>
> ✅ Split into multiple items:  
> - **Hot water system location**: “Above the bidet in the bathroom”  
> - **Hot water ON/OFF button location**: “Below the boiler in the bathroom”  
> - **Main water valve location**: “Under the kitchen sink”

### ✍️ Use step-by-step instructions when needed

For procedures like opening a lockbox or resetting the boiler, use short, numbered steps in a logical order.

> **Example** ✅ **Keybox instructions**:  
> 1. Turn the dials to match the code.  
> 2. Pull down the black lever.  
> 3. After use, scramble the code to keep it private.



## 📜 Writing internal policies

Policies are a special type of library item used to control Alfred’s behavior in specific situations. They are **never shown directly to guests**. Instead, they define what Alfred should do or say when certain conditions are met — such as when a guest reports a problem, asks for extra services, or tries to check in outside of working hours.

We’ve already defined core policies for Alfred. If you need to create custom ones, these tips will help you do it right.

### 🧠 What a good policy needs

A well-written policy should:
- Be **specific** about the scenario it applies to  
- Clearly define **what Alfred should do** (pass to a human? send a message? take no action?)  
- Include **what Alfred should say**, if a guest message is needed  
- Be written in **natural, human-readable language** (no placeholders, no technical shorthand)


### ✅ Structure to follow

Before writing a policy item, take a moment to think about the exact scope:  
- What situation does it cover?  
- When does it start?  
- When does it end?

Then use this structure:

1. **Trigger**  
   Describe the condition that activates the policy.  
   _Example: “If the guest reports that they lost the keys…”_

2. **Action**  
   Describe what Alfred should do.  
   _Example: “Pass the chat to a human agent.”_

3. **Message (if needed)**  
   Provide the exact message Alfred should send.  
   _Example: “No worries, we’ll get back to you shortly!”_

