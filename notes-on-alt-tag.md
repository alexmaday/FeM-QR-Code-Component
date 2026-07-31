# Thoughts and ideas while building the QR Code Component

## 2026-07-29 15:42 - Alt text for QR code image Wednesday

**tl;dr**

> "Silktide Warnings vs. Errors:
> A yellow icon (!) means a manual review check/warning (e.g., automated tools flagging long alt text for human review), not a broken WCAG rule

Using the [Silktide Accessibility Checker](https://silktide.com/toolbar/) in chrome, I got a warning on my alt text for the single QR code image. It pointed me to "Understanding Success Criterion for Non-text Content" v1.1.1 (which is no longer maintained incidentally). There's conveniently a section on the page called Examples. Unfortunately, there's no specific mention for a QR code use case. What about on the updated page for v2.2? Maybe QR codes weren't a thing when v1.1.1 was written.

Nope. Within v2.2, there's no mention of what makes a successful alt text for a QR code.

So I google, "alt text for QR code" and go through several iterations including:

- "Scan QR code to visit Frontend Mentor"
- "Scan QR code to visit www.FrontendMentor.com"
- "Scan QR code to visit www.FrontendMentor.com - Improve your front-end skills by building projects"

Do you see how each iteration, I kept adding more detail and was still getting a warning. At this point, I turn to have a chat with AI. Of course, I first present it with AGENTS.md so it won't give me any answers outright.

As a sighted user, I don't have lived experience of navigating the web using assistive technology and one thing AI pointed out was that it was redundant to include the heading text verbatim. It does nothing. And most importantly, alt text should describe what the image is (content), not what the user should do (action). That is all.

Turns out `alt="QR code to Frontend Mentor"` passes muster with google gemini. Turns out, this text is still worthy of a warning. Turns out that
