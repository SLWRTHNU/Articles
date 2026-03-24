# Vanillasoft Knowledge Base Article Style Guide

## Purpose
This guide defines the standards for creating and auditing knowledge base articles for support.vanillasoft.com. All articles must be professional, uniform, easy-to-read, and ready to copy/paste directly into Zendesk.

---

## Article Structure

### Title Requirements
- **Style**: Natural and welcoming, not cold or basic
- **Format**: Action-oriented and clear about what the article covers
- **Examples**:
  - ✅ GOOD: "Setting Up Your Voicemail in the Vanillasoft VoIP Portal"
  - ✅ GOOD: "Managing Your Phone Number and Settings in the Vanillasoft VoIP Portal"
  - ❌ BAD: "Configure Voicemail"
  - ❌ BAD: "Voicemail Setup"

### Introduction Requirements
Every article MUST start with:
1. **What the feature/task is** - Brief explanation
2. **How it's beneficial** - Light touch, NOT a sales pitch
3. **Why the customer would use it** - Practical use cases

**Example**:
```html
<p>
  <strong>Call Screening</strong> allows you to manage unwanted incoming calls from specific numbers by automatically routing them to voicemail, sending a busy signal, or letting them ring without answer. This feature helps reduce interruptions from spam calls, telemarketers, or other unwanted contacts while ensuring legitimate calls reach you. Call screening rules are managed through the Vanillasoft VoIP portal and apply automatically once configured.
</p>
```

---

## Formatting Standards

### Images
- **Placeholder path**: `/guide-media/01K7J353MBJ2JD62HMTENQDPXX`
- **Always include**: `width="502" height="202"`
- User will replace placeholder with actual screenshot IDs after article creation

**Example**:
```html
<img src="/guide-media/01K7J353MBJ2JD62HMTENQDPXX" width="502" height="202">
```

### Links to Other Articles
- **Always open in new tab**: `target="_blank" rel="noopener noreferrer"`
- **Full sentence format**: Article title is the hyperlinked portion
- **Never use**: "click here" or "this article"

**Examples**:
```html
✅ GOOD: For more details, refer to the <a href="URL" target="_blank" rel="noopener noreferrer">How To Create an Email Template</a> article.

❌ BAD: Click <a href="URL">here</a> for more information.
```

### Accordions
**Use accordions for**:
- Multiple methods/configuration options
- "What You Need Before You Start"
- "Best Practices"
- "What to Do Next"
- Any 2+ distinct information sections
- Troubleshooting sections

**Don't overuse** - Goal is to keep articles clean and scannable, not overwhelming

**Format**:
```html
<div class="accordion">
  <p>
    <strong>Section Title</strong>
  </p>
</div>
<div class="panel">
  <!-- Content here -->
  <hr style="height: 1px; visibility: hidden;">
</div>
```

### Lists
- **Include** `data-list-item-id` attributes on all list items
- **Format**: `data-list-item-id="e93d64914f6c7df3e53476a13e314ee7f"` (random alphanumeric)

**Example**:
```html
<ul>
  <li data-list-item-id="ec7bf51dc02b7958671f86061f88514f8">
    <p>
      List item content here.
    </p>
    <hr style="height: 1px; visibility: hidden;">
  </li>
</ul>
```

### Spacing
- **Small gaps between list items**: `<hr style="height: 1px; visibility: hidden;">`
- **Major section breaks**: `<hr style="height: 15px; visibility: hidden;">`
- **Last item in a list**: No trailing `<hr>` tag

### Tables
- **Wrapper**: Use `<figure class="wysiwyg-table">` around tables
- **Styling**: Use `border-color` instead of `border: 1px solid`

**Example**:
```html
<figure class="wysiwyg-table" style="margin: 20px 0; width: 100%;">
  <table style="border-collapse: collapse;">
    <thead>
      <tr style="background-color: #f5f5f5;">
        <th style="border-color: #ddd; padding: 12px; text-align: left;">Header</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="border-color: #ddd; padding: 10px;">Content</td>
      </tr>
    </tbody>
  </table>
</figure>
```

### Headers (H3)
- **Include ID attributes** for anchor linking
- **Format**: `id="h_01KHKE60G811708W9FTC855Z1X"` (alphanumeric)

**Example**:
```html
<h3 id="h_01KHKE60G811708W9FTC855Z1X">Section Title</h3>
```

---

## Tone and Voice

### Writing Style
- **Direct and concise** - No unnecessary words
- **Professional but approachable** - Not cold or robotic
- **Use "you"** to address the reader
- **Simple language** - Clientele is non-technical
- **Bold UI elements**: **Admin**, **Save**, **Menu**, **New**, etc.

### What to Avoid
- ❌ Overly technical jargon
- ❌ Sales-heavy language
- ❌ "Click here" or vague link text
- ❌ Excessive explanations after sharing files
- ❌ Mentioning "Cloudli" or "CMV" (unless specifically instructed)

---

## Branding and Terminology

### Always Use
- **"Vanillasoft VoIP portal"** - for portal references
- **"VS Connect"** - for star codes and dialing features
- **"Vanillasoft"** - general product references

### Never Use (unless specifically instructed)
- ❌ "Cloudli" or "Cloudli Connect"
- ❌ "CMV" or "Clarity"

### Portal Branding Note
The VoIP portal displays Cloudli branding because it's hosted by Cloudli. Include this note in first login step:

```html
<ul>
  <li>
    Note: This portal may display <strong>Cloudli</strong> branding because it is hosted by Cloudli. All configuration and support are handled by <strong>Vanillasoft</strong>. For assistance, contact <a href="https://support.vanillasoft.com/hc/en-us/requests/new" target="_blank" rel="noopener noreferrer">Vanillasoft Support</a>.
  </li>
</ul>
```

---

## Common Article Patterns

### Standard Login Step (Admin)
```html
<li>
  <p>
    Log in to <strong>Vanillasoft</strong> as an <strong>Admin</strong>.<br>
    <img src="/guide-media/01K7J353MBJ2JD62HMTENQDPXX" width="502" height="202">
  </p>
  <ul>
    <li>
      If you are logged in as a Caller, switch to <strong>Admin</strong> from the top menu.
    </li>
  </ul>
  <hr style="height: 1px; visibility: hidden;">
</li>
```

### Standard Login Step (VoIP Portal)
```html
<li>
  <p>
    Log in to the <a href="https://connect.cloudli.com" target="_blank" rel="noopener noreferrer"><strong>Vanillasoft VoIP portal</strong></a>.<br>
    <img src="/guide-media/01K7J353MBJ2JD62HMTENQDPXX" width="502" height="202">
  </p>
  <ul>
    <li>
      Note: This portal may display <strong>Cloudli</strong> branding because it is hosted by Cloudli. All configuration and support are handled by <strong>Vanillasoft</strong>. For assistance, contact <a href="https://support.vanillasoft.com/hc/en-us/requests/new" target="_blank" rel="noopener noreferrer">Vanillasoft Support</a>.
    </li>
  </ul>
  <hr style="height: 1px; visibility: hidden;">
</li>
```

### Standard "Save" Step (Single Option)
```html
<li>
  <p>
    Click <strong>Save</strong> to apply your changes.<br>
    <img src="/guide-media/01K7J353MBJ2JD62HMTENQDPXX" width="502" height="202">
  </p>
  <hr style="height: 1px; visibility: hidden;">
</li>
```

### Standard "Save" Step (Multiple Options)
```html
<li>
  <p>
    When finished, click <strong>Save</strong> to apply your changes, or click <strong>Save and Continue</strong> to save your changes and configure another [item].<br>
    <img src="/guide-media/01K7J353MBJ2JD62HMTENQDPXX" width="502" height="202">
  </p>
  <hr style="height: 1px; visibility: hidden;">
</li>
```

### List with Options/Explanations
```html
<li>
  <p>
    Open the <strong>Action</strong> drop-down and select the desired action.<br>
    <img src="/guide-media/01K7J353MBJ2JD62HMTENQDPXX" width="502" height="202">
  </p>
  <ul>
    <li>
      <strong>Option 1</strong> – Brief explanation of what this does.
      <hr style="height: 1px; visibility: hidden;">
    </li>
    <li>
      <strong>Option 2</strong> – Brief explanation of what this does.
      <hr style="height: 1px; visibility: hidden;">
    </li>
    <li>
      <strong>Option 3</strong> – Brief explanation of what this does.
    </li>
  </ul>
  <hr style="height: 1px; visibility: hidden;">
</li>
```

### Standard Closing Paragraph
```html
<p>
  Your [feature] is now configured and ready to use. For additional support, contact <a href="https://support.vanillasoft.com/hc/en-us/requests/new" target="_blank" rel="noopener noreferrer">Vanillasoft Support</a>.
</p>
```

---

## Article Types and Special Considerations

### Overview Articles (No Screenshots Needed)
- Focus on features and functions described in prose
- No numbered step-by-step instructions
- Include all key features in organized sections
- Example: HUD overview, Star Codes reference

### Step-by-Step Articles
- Clear numbered steps with screenshots
- Each step should have an image placeholder
- Use nested lists for options or notes under steps
- Keep steps focused and concise

### Mixed Articles
- Start with step-by-step for initial setup/access
- Switch to prose for additional information that doesn't require screenshots
- Example: Password reset (steps 1-4, then prose for remaining info)

---

## Quality Checklist

Before submitting an article, verify:

- ✅ Title is natural and welcoming
- ✅ Introduction explains what, why, and benefits
- ✅ All image paths use placeholder: `/guide-media/01K7J353MBJ2JD62HMTENQDPXX`
- ✅ All images include `width="502" height="202"`
- ✅ Links open in new tab with full sentence format
- ✅ UI elements are bolded (**Admin**, **Save**, etc.)
- ✅ Lists include `data-list-item-id` attributes
- ✅ Proper spacing with `<hr>` tags (1px for small gaps, 15px for major breaks)
- ✅ No mention of "Cloudli" or "CMV" (unless instructed)
- ✅ Tables use `<figure class="wysiwyg-table">` wrapper
- ✅ H3 headers include `id` attributes
- ✅ Accordions used appropriately (not overused)
- ✅ Closing paragraph includes support link
- ✅ Tone is professional, direct, and concise
- ✅ Language is simple and non-technical
- ✅ Article is ready to copy/paste into Zendesk

---

## Examples of Good vs. Bad

### Introduction
✅ **GOOD**:
```html
<p>
  <strong>Call Screening</strong> allows you to manage unwanted incoming calls from specific numbers by automatically routing them to voicemail, sending a busy signal, or letting them ring without answer. This feature helps reduce interruptions from spam calls, telemarketers, or other unwanted contacts while ensuring legitimate calls reach you.
</p>
```

❌ **BAD**:
```html
<p>
  This article explains call screening.
</p>
```

### List Item Formatting
✅ **GOOD**:
```html
<li data-list-item-id="e93d64914f6c7df3e53476a13e314ee7f">
  <p>
    Click <strong>New</strong> to create a new rule.<br>
    <img src="/guide-media/01K7J353MBJ2JD62HMTENQDPXX" width="502" height="202">
  </p>
  <hr style="height: 1px; visibility: hidden;">
</li>
```

❌ **BAD**:
```html
<li>
  Click New to create a new rule.
  <img src="/guide-media/screenshot.png">
</li>
```

### Link Format
✅ **GOOD**:
```html
For more information, see the <a href="URL" target="_blank" rel="noopener noreferrer">How to Create an Email Template</a> article.
```

❌ **BAD**:
```html
Click <a href="URL">here</a> for more information.
```

---

## Usage Instructions

### For Creating New Articles:
1. Share raw content (point-form notes, existing articles, documents, etc.)
2. Specify the article type (step-by-step, overview, mixed)
3. Receive a complete, formatted HTML article ready for Zendesk

### For Auditing Articles:
1. Share the employee-written article
2. Request: "Audit this article against the Vanillasoft knowledge base style guide"
3. Receive a detailed review with specific corrections needed

---

## Notes
- This style guide was developed through iterative article creation
- All patterns have been tested and approved for support.vanillasoft.com
- When in doubt, prioritize clarity and simplicity over technical completeness
- The goal is uniform, professional, easy-to-follow documentation for non-technical users

---

**Document Version**: 1.0  
**Last Updated**: February 16, 2026  
**Maintained By**: Vanillasoft Support Documentation Team
