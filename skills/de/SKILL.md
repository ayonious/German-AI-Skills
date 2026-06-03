---
name: de
description: correct and translate german, english, or mixed text. use when a user pastes text and wants grammar, spelling, wording, or phrasing fixed. automatically detect the language. always output corrected german first and corrected english second. if input is german, provide corrected german and english translation. if input is english, provide german translation first and corrected english second. preserve meaning, tone, emojis, and formality.
---

# Task

Take any text provided by the user and:

1. Detect whether it is German, English, or mixed.
2. Correct grammar, spelling, punctuation, and wording.
3. Preserve the user's intended meaning.
4. Preserve emojis unless they are clearly inappropriate.
5. Keep the same level of formality unless instructed otherwise.
6. Always produce both German and English versions.

# Output Format

## German 🇩🇪

<corrected german version>

## English 🇬🇧

<corrected english version>

# Rules

- Do not explain corrections unless the user explicitly asks.
- Do not comment on mistakes.
- Do not add information that was not present in the original text.
- Make the text sound natural and native.
- For mixed-language input, normalize both outputs into fluent German and fluent English.
- Preserve names, dates, places, URLs, and factual details.
- Keep messages concise when the original message is concise.

# Examples

User:

Ah wie schön!! Ich kenne die! Geht es ihnen alles gut?

Output:

## German 🇩🇪

Ah, wie schön! 😊 Ich kenne sie! Geht es ihnen allen gut?

## English 🇬🇧

Ah, how nice! 😊 I know them! Are they all doing well?

---

User:

This is a cafe next to my apartment

Output:

## German 🇩🇪

Das ist ein Café neben meiner Wohnung.

## English 🇬🇧

This is a café next to my apartment.

---

User:

Und ja jemand hat doch gemeldet aber ich muss ein bisschen platz finden damit ich die alles wieder anfangen kann.

Output:

## German 🇩🇪

Und ja, jemand hat sich tatsächlich gemeldet, aber ich muss erst etwas Zeit und Platz finden, damit ich das alles wieder anfangen kann.

## English 🇬🇧

And yes, someone actually got in touch, but I first need to find some time and space so that I can start doing all of that again.