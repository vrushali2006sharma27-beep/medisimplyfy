# MediSimplify AI

A browser-based platform that makes medical information understandable. Patients can paste any medical report, prescription, discharge summary, or lab result and receive a clear, plain-language explanation — in their own language, at a reading level that suits them.

---

## Purpose

Medical documents are written for clinicians, not patients. Terms like "acute myocardial infarction," "ejection fraction," or "HbA1c" mean nothing to most people receiving that information. MediSimplify bridges that gap by translating clinical language into plain English (or any of ten supported languages), flagging the terms that matter most, and letting patients ask follow-up questions in their own words.

The platform is designed for anyone who has ever left a clinic with a document they did not fully understand.

---

## Features

### Simplify Text

Paste any medical document — a discharge summary, a prescription, a pathology report, a blood panel — and the platform returns a plain-language explanation. Key medical terms are underlined and reveal a plain-language tooltip on hover. Color-coded boxes call out the most important actions, warnings, and safe-to-know details.

The reading level can be set to three levels:

- Very simple (approximately grade 5)
- Moderate (approximately grade 8)
- Detailed (approximately grade 12)

Built-in sample documents cover a heart attack report, a prescription for sinusitis, a blood panel with anaemia and elevated blood sugar, and a congestive heart failure discharge summary.

### Translate

Medical documents can be translated into ten languages while preserving clinical meaning. When the "also simplify" option is active, jargon is simplified in the same pass. Supported languages are English, Hindi, Spanish, French, Arabic, Chinese (Simplified), Portuguese, German, Tamil, and Bengali.

### Glossary

A searchable reference of twenty common medical terms, each explained in plain language and categorised by domain: cardiology, laboratory tests, medications, and general medicine. The glossary is designed for quick lookup, not exhaustive reference.

### Ask a Question

A conversational interface where patients can ask plain-language questions about their document. Example prompts include understanding a diagnosis, identifying side effects, clarifying dosage instructions, and interpreting whether a result is within normal range. The tool includes a clear disclaimer that it does not provide medical advice and is not a substitute for a healthcare professional.

---

## Languages

The user interface itself can be switched to any of the ten supported languages using the selector in the header. UI labels, button text, and section headings update accordingly.

Supported: English, Hindi, Spanish, French, Arabic, Chinese, Portuguese, German, Tamil, Bengali.

---

## Accessibility

- Read Aloud: a speech synthesis button reads the simplified explanation aloud in the selected language.
- Copy: all outputs include a one-click copy button.
- Keyboard navigation is fully supported, with visible focus states.
- The layout is responsive and works at phone width.
- Dark mode follows the system preference and can be overridden.
- Reduced motion is respected; animations are suppressed when the user has that preference set.

---

## Technical notes

This is a self-contained HTML file with no server-side dependencies. All logic runs in the browser. In the current demo state:

- The simplify and translate outputs are pre-authored for the four included sample documents. Free-form input returns a generic structural explanation.
- The translation engine is simulated. In a production deployment, this would connect to a translation API (such as Google Cloud Translation or Azure Cognitive Services) and a large language model endpoint for the simplification and Q&A features.
- No data is transmitted anywhere. Nothing the user pastes is sent to a server.
- Browser local storage is not used.

---

## Deployment

The platform is a single `.html` file. It can be hosted on any static file host (Netlify, Vercel, GitHub Pages, an S3 bucket with static hosting enabled, or a standard web server). No build step is required.

For a production build, the following integrations would be added:

- A translation API for real-time multilingual output
- A large language model API for open-ended text simplification and the Q&A chat
- Authentication if patient records are to be stored or retrieved
- An audit log if the platform is used in a clinical setting

---

## Medical disclaimer

MediSimplify AI explains medical language. It does not diagnose, prescribe, or advise on treatment. No output from this platform should be used as a substitute for the advice of a qualified healthcare professional. If you have questions about your health or your treatment plan, speak with your doctor, pharmacist, or clinical team.

---

## Project structure

```
index.html    Single-file application — all HTML, CSS, and JavaScript
README.md            This file
```

---

## License

This project is released for educational and demonstration purposes.
