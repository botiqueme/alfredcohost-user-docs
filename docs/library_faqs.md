# Library FAQs

Common questions about writing and managing library content for your properties.

## General questions

<details>
<summary><strong>Do I need to fill in all the standard items?</strong></summary>

No. Fill in only what's relevant to your property. Leave blank any items that don't apply. Alfred will only use the information you provide.

Learn more: [About libraries](concepts/libraries_c.md)

</details>

<details>
<summary><strong>Can I edit library items after I've created them?</strong></summary>

Yes. You can edit any library item at any time. Changes take effect immediately, and Alfred will use the updated information in future guest conversations.

Learn more: [Add content to libraries](procedures/libraries_p.md)

</details>

<details>
<summary><strong>How do I know if my writing is good enough?</strong></summary>

Alfred is very good at understanding your input, even if it's not perfect. For best results, follow our [writing tips](procedures/writing_tips.md). The key is to be clear and specific — think about what a guest needs to know to solve their problem or find what they're looking for.

</details>

<details>
<summary><strong>Can I copy library items between properties?</strong></summary>

Currently, each property has its own library. You'll need to add items to each property separately. This ensures that each property's information stays accurate and specific to that unit.

Learn more: [About libraries](concepts/libraries_c.md)

</details>

## Writing content

<details>
<summary><strong>How long should library items be?</strong></summary>

Keep items short and focused. Each item should cover **one clear piece of information**. For simple items like WiFi passwords, a few words are enough. For instructions, use short, numbered steps when needed.

Learn more: [Writing custom items](procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>Can I use abbreviations or technical terms?</strong></summary>

Avoid abbreviations and internal jargon. Write as if you're explaining something to a guest in person. Use clear, everyday language that anyone can understand.

Learn more: [Writing tips](procedures/writing_tips.md)

</details>

<details>
<summary><strong>What if my property has special features not covered by standard items?</strong></summary>

Use custom items to add any information that's not covered by the standard fields. See our guide on [writing custom items](procedures/writing_custom_items.md) for tips.

</details>

<details>
<summary><strong>Should I include photos or videos?</strong></summary>

Only if they make the explanation easier. For example, a video showing how to operate a washing machine can be helpful. Avoid adding media just because you have it — focus on what actually helps guests.

Learn more: [Writing tips](procedures/writing_tips.md)

</details>

<details>
<summary><strong>How specific should I be about locations?</strong></summary>

Be as specific as possible. Instead of "in the kitchen," write "inside the cabinet under the kitchen sink." The more precise you are, the less guests will need to ask follow-up questions.

Learn more: [Writing tips](procedures/writing_tips.md)

</details>

<details>
<summary><strong>What if I'm not sure how to write something?</strong></summary>

Start by thinking: what is the guest trying to do? When will they need this information? Then write a clear, direct answer. If you're still unsure, check our [writing tips](procedures/writing_tips.md) for examples and guidance.

</details>

## Custom items

<details>
<summary><strong>When should I create a custom item?</strong></summary>

Create custom items when you need to add information that isn't covered by the standard fields. For example, if you have specific parking instructions, garbage collection times, or unique property features.

Learn more: [Writing custom items](procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>How do placeholders work in custom items?</strong></summary>

When you write custom items, think about how they might be used in guest messages. For example, if you create a "Garbage collection times" item with the value "from 6:30 PM to 10:30 PM," Alfred can insert it into messages like: "Please remember that trash can be taken out {garbage_collection_times}."

Learn more: [Writing custom items](procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>Can I put multiple pieces of information in one custom item?</strong></summary>

No. Each library item should focus on **one clear piece of information**. If you have multiple related details, create separate items for each one. This helps Alfred find and use the right information more accurately.

Learn more: [Writing custom items](procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>What's the difference between standard and custom items?</strong></summary>

Standard items are predefined fields we've created for common information (like WiFi password, check-in time, etc.). Custom items let you add any other information specific to your property. Both work the same way — Alfred uses them to answer guest questions.

Learn more: [About libraries](concepts/libraries_c.md), [Writing custom items](procedures/writing_custom_items.md)

</details>

## Policies

<details>
<summary><strong>What are policies, and how are they different from regular library items?</strong></summary>

Policies are special library items that control Alfred's behavior in specific situations. They're never shown directly to guests. Instead, they tell Alfred what to do or say when certain conditions are met — like when a guest reports a problem or asks for extra services.

Learn more: [Writing policies](procedures/writing_policies.md)

</details>

<details>
<summary><strong>Do I need to create custom policies?</strong></summary>

We've already defined core policies for Alfred. You only need to create custom policies if you have specific situations that require special handling. See our guide on [writing policies](procedures/writing_policies.md) for more details.

</details>

## Troubleshooting

<details>
<summary><strong>What if Alfred isn't using my library items correctly?</strong></summary>

Make sure your items are:
- Clear and specific
- Focused on one piece of information each
- Written from the guest's perspective
- Free of vague words like "available" or "present"

If you're still having issues, check that you've filled in the relevant standard items and that custom items have clear, descriptive labels.

Learn more: [Writing tips](procedures/writing_tips.md), [Writing custom items](procedures/writing_custom_items.md)

</details>

<details>
<summary><strong>Can I test how Alfred will use my library content?</strong></summary>

Yes. You can test how Alfred responds to guest questions using the test assistant feature. This helps you see how your library content works in practice before going live.

Learn more: [Test assistant](procedures/test_assistant.md)

</details>

<details>
<summary><strong>What happens if I leave an item blank?</strong></summary>

Nothing. Alfred simply won't use that information. Guests won't see empty fields or error messages. Only the information you provide will be used.

Learn more: [About libraries](concepts/libraries_c.md)

</details>

<style>
/* FAQ Page Styling */
.markdown-section details {
  margin-bottom: 0;
  border-bottom: 1px solid #e0e0e0;
  padding-bottom: 0.75rem;
  margin-bottom: 0.75rem;
}

.markdown-section details:last-child {
  border-bottom: none;
  margin-bottom: 0;
}

.markdown-section details summary {
  font-size: 1.25rem;
  font-weight: 600;
  color: #FF3B3C;
  cursor: pointer;
  list-style: none;
  padding: 0.75rem 0;
  position: relative;
  padding-left: 1.5rem;
}

.markdown-section details summary::-webkit-details-marker {
  display: none;
}

.markdown-section details summary::before {
  content: '';
  position: absolute;
  left: 0;
  top: 50%;
  transform: translateY(-50%) rotate(-45deg);
  width: 8px;
  height: 8px;
  border-right: 2px solid #000;
  border-bottom: 2px solid #000;
  transition: transform 0.2s ease;
}

.markdown-section details[open] summary::before {
  transform: translateY(-50%) rotate(45deg);
}

.markdown-section details summary strong {
  color: #FF3B3C;
}

.markdown-section details[open] summary {
  margin-bottom: 1rem;
}
</style>
