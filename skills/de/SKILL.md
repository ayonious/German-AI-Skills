---
name: de
description: correct and translate german, english, or mixed text. use when a user pastes text that may contain grammar, spelling, punctuation, vocabulary, or phrasing mistakes. automatically detect the language. always output a german version first and an english version second. if the input is german, provide corrections and a corrected german version followed by an english translation. if the input is english, provide a natural german translation followed by a corrected english version. preserve meaning, tone, emojis, names, dates, and level of formality.
---

# Task

Take any user-provided text and improve it.

The text may be:

- German
- English
- Mixed German and English
- Informal chat messages
- Emails
- Social media posts
- Notes
- Voice-to-text transcripts

Always detect the language automatically.

Always return:

1. German version first
2. English version second

# Core Rules

- Correct grammar.
- Correct spelling.
- Correct punctuation.
- Improve unnatural wording.
- Preserve the original meaning.
- Preserve emojis.
- Preserve names, dates, locations, URLs, and factual details.
- Preserve the user's intended level of formality unless instructed otherwise.
- Do not explain grammar unless explicitly asked.
- Do not add information that was not present in the original text.
- Make the result sound natural and native.

# German Error Highlighting

When the original input contains German, include a correction section.

Show only words or short phrases that were changed.

Format:

### Corrections

- incorrect → correct
- incorrect → correct

Do not explain the correction.

If no corrections were needed, omit the Corrections section entirely.

# Output Format

For German input:

## German 🇩🇪

### Corrections

(optional)

### Corrected Text

<corrected german>

## English 🇬🇧

<english translation>

---

For English input:

## German 🇩🇪

<natural german translation>

## English 🇬🇧

<corrected english>

---

For mixed-language input:

## German 🇩🇪

### Corrections

(optional)

### Corrected Text

<fully natural german version>

## English 🇬🇧

<fully natural english version>

# Examples

## Example 1

User:

Ich habe es vergesn

Output:

## German 🇩🇪

### Corrections

- vergesn → vergessen

### Corrected Text

Ich habe es vergessen.

## English 🇬🇧

I forgot it.

---

## Example 2

User:

Das ist ein Cafe Neben meine Wohung

Output:

## German 🇩🇪

### Corrections

- Cafe → Café
- Neben → neben
- meine → meiner
- Wohung → Wohnung

### Corrected Text

Das ist ein Café neben meiner Wohnung.

## English 🇬🇧

That is a café next to my apartment.

---

## Example 3

User:

ahhh soo schön. Gratuliere euch.

Output:

## German 🇩🇪

### Corrections

- soo → so

### Corrected Text

Ahhh, so schön! 😊 Gratuliere euch! 🎉

## English 🇬🇧

Ahhh, so beautiful! 😊 Congratulations to you both! 🎉

---

## Example 4

User:

Hi Jerek! Mir geht es ziemlich gut aber auch sehr busy.

Output:

## German 🇩🇪

### Corrections

- aber auch sehr busy → aber ich bin auch sehr beschäftigt

### Corrected Text

Hi Jerek! Mir geht es ziemlich gut, aber ich bin auch sehr beschäftigt.

## English 🇬🇧

Hi Jerek! I'm doing quite well, but I'm also very busy.

---

## Example 5

User:

This is a cafe next to my apartment

Output:

## German 🇩🇪

Das ist ein Café neben meiner Wohnung.

## English 🇬🇧

This is a café next to my apartment.

---

## Example 6

User:

I forgot to send the email yesterday sorry

Output:

## German 🇩🇪

Ich habe gestern vergessen, die E-Mail zu senden. Entschuldigung.

## English 🇬🇧

I forgot to send the email yesterday. Sorry.

---

## Example 7

User:

Und ja someone contacted me aber ich brauche mehr time.

Output:

## German 🇩🇪

### Corrections

- someone contacted me → jemand hat sich gemeldet
- time → Zeit

### Corrected Text

Und ja, jemand hat sich gemeldet, aber ich brauche mehr Zeit.

## English 🇬🇧

And yes, someone contacted me, but I need more time.

# Special Cases

## Single Word Input

User:

Wohung

Output:

## German 🇩🇪

### Corrections

- Wohung → Wohnung

### Corrected Text

Wohnung

## English 🇬🇧

Apartment

## Short Chat Messages

Keep the output concise.

Do not rewrite the message into a long paragraph.

## Emojis

Keep emojis whenever possible.

Example:

User:

Wie schön!!

Output:

## German 🇩🇪

### Corrections

- !! → !

### Corrected Text

Wie schön! 😊

## English 🇬🇧

How lovely! 😊

# Priority Order

1. Preserve meaning.
2. Correct mistakes.
3. Maintain natural native phrasing.
4. Preserve tone and emojis.