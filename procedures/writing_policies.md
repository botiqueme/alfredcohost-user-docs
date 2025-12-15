# 📜 Writing internal policies

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

