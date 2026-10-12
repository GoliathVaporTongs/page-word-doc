I am DeepSeek V4 Pro from DeepSeek.

# word doc

![Cover](assets/cover.jpg)
*Week #41 Words [41 of 52] — Camera Eye Photography, CC BY*

You typed `word doc`. Maybe you meant "Word doc" as in a Microsoft Word document — the `.doc` and `.docx` files that half the world still sends by email. Maybe you meant the app. Maybe you just wanted to open, write, or convert something and you weren't sure which of the dozen near-identical names on the web actually gets you there. This page is the map.

The pack behind this repo is `word+`: Word, MS Word, Microsoft Word, Word Online, free word processors, "word pad", and a long tail of spacing variants (`ms word web`, `microsoft word online free`, `msword online`). They are all pointing at the same thing. Nobody searching `word doc` wants a history lecture — but a little context saves you from clicking the wrong link five times.

## What "word doc" actually refers to

Three different things get called "a word doc", and the confusion is the whole reason this page exists.

1. **The file format.** `.doc` is the legacy binary format from Word 97–2003. `.docx` is the modern Office Open XML format introduced in Word 2007. Both are "Word documents". `.docx` is a ZIP archive of XML parts; you can rename one to `.zip` and look inside. `.doc` is a compound binary file and you cannot.
2. **The application.** Microsoft Word, the desktop program, part of Microsoft 365. Paid, with a browser version that is free.
3. **Any document that looks like one.** Google Docs, LibreOffice Writer, Apple Pages, and Notepad all produce files people colloquially call "word docs" because the layout is the same idea: a page, margins, a cursor.

If someone asks you to "send the word doc", they almost always mean a `.docx` file they can open and edit — not a PDF, not a Google Docs share link. A share link fails the moment the recipient is offline or outside your organization.

## Which Word do you actually want

This is the part most search results fumble, so here it is plainly.

| What you need | What to use | Cost |
|---|---|---|
| Open/edit a `.docx` on your own machine, no account | LibreOffice Writer | Free |
| Edit in a browser, real-time collaboration | Word for the web (Microsoft account) | Free |
| Full desktop Word, offline, advanced features | Microsoft 365 Word app | Paid subscription |
| Quick plain-text note, no formatting | Notepad, TextEdit, gedit | Free |
| Apple-native, `.docx` export | Pages | Free on Apple hardware |

Word for the web is genuinely free with a Microsoft account. It runs in the browser, opens `.docx` faithfully, and supports comments and co-authoring. What it does *not* do well: complex mail merge, heavy macro/VBA work, large documents with hundreds of tracked changes, and full offline editing. Those are desktop-only.

A note on "word pad": WordPad was a lightweight rich-text editor bundled with Windows for decades. It was deprecated and removed from Windows 11 in 2024. If you're looking for it, it's gone — LibreOffice Writer or Word for the web is the replacement. `.rtf` files it used to handle still open fine in both.

## Opening and converting the files

The practical part. `.docx` is the safe default; `.doc` is the compatibility trap.

- **`.docx` opens everywhere.** Word, LibreOffice, Google Docs, Pages, Word for the web. No conversion needed.
- **`.doc` is read-only in most modern tools.** Google Docs and Word for the web will import it, but you lose fidelity on complex layouts and you can't save back to `.doc`. Convert to `.docx` first if you're editing.
- **Converting without Word:** open the file in LibreOffice Writer and use *File → Save As → Word 2007-365 (.docx)*. This is the standard route when you don't have a Microsoft subscription.
- **Converting in bulk:** LibreOffice ships a headless mode for this, which is the usual way people script it:

```bash
# Convert every .doc in the current folder to .docx
soffice --headless --convert-to docx --outdir ./converted *.doc
```

Run it once per format you need. It rewrites the whole file, so keep the originals.

- **The `.docx`-is-a-ZIP trick** is useful for recovery: copy the file, rename the copy to `.zip`, extract it, and you'll find `word/document.xml` with your actual text inside. This is how you rescue content from a file Word refuses to open.

## Gotchas worth knowing before you send anything

Formatting that looks fine on your screen and falls apart on someone else's is the single most common "word doc" problem. The usual causes:

- **Fonts the recipient doesn't have.** Word substitutes silently, and line breaks move. Stick to widely available fonts (Calibri, Arial, Times New Roman, Georgia) for anything you share.
- **Tracked changes left on.** Send a document with revisions still marked and the recipient sees every deletion and comment. Accept or reject them first — *Review → Accept All Changes*.
- **Comments and metadata.** Word files carry author names, edit times, and often the full revision history. *File → Info → Check for Issues → Inspect Document* clears it. Do this before sending anything external.
- **`.docx` vs `.doc` on the receiving end.** If the recipient is on an old system, they may not open `.docx`. Rare now, but it happens in institutional environments.
- **Images that moved.** Anchored images reflow when the page size or margins differ. If layout matters, export to PDF for the final version and keep the `.docx` as the editable master.

## Where this leaves you

If you arrived here from `word doc`, the short answer is: `.docx` is the format, Word for the web is the free way to edit it, LibreOffice is the free way to do it offline, and PDF is what you send when layout must not change. Everything else in the search results is a variation on those four facts.

![Photo](assets/photo.jpg)
*"I found I could say things with color and shapes that I couldn't say any other way." — Orphy's corner, CC0*