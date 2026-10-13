# adobe acrobat professional

If you searched for *adobe acrobat professional* rather than *adobe acrobat pro*, you probably ran into the older, formal product name. Adobe sold desktop Acrobat under the name "Adobe Acrobat Professional" for several release cycles — 6.0 Professional, 7 Professional, 8 Professional — before shortening it to "Pro" with Acrobat 9 and later. Same program, different label on the box. This page is a plain-language note on what that program is, what separates it from the free Reader, and the parts that trip people up in daily use.

![Two acrobats balancing on a bicycle](assets/cover.jpg)
*The name is a pun that got out of hand: Acrobat the PDF tool, acrobats the performers. Photo: sasastro, CC BY.*

## What the name refers to today

Adobe's PDF software comes in three tiers that are easy to confuse:

- **Acrobat Reader** — free, reads and prints PDFs, fills in existing form fields, adds a basic signature. It cannot create forms, edit text, or run preflight.
- **Acrobat Standard** — Windows only. Editing, combining, exporting, basic e-signatures. No Preflight, no Action Wizard, no PDF comparison.
- **Acrobat Pro** — Windows and macOS. Everything in Standard plus the print-production and document-engineering tools: Preflight, Actions, Redaction, Compare Files, OCR, accessibility tagging, PDF/A and PDF/X conversion, and JavaScript-based automation.

When someone types "adobe acrobat professional," nine times out of ten they mean the top tier — the one that edits, not just reads. That is Acrobat Pro. The word "DC" you will see attached to it stands for Document Cloud, Adobe's subscription service. Adobe has since dropped the "DC" suffix from the product name in most places, so "Adobe Acrobat Pro DC" and "Adobe Acrobat Pro" point at the same application, just from different years of branding.

There is also a perpetual-license edition, **Acrobat Pro 2020**, sold as a one-time purchase. It is frozen at that release — no continuous updates — which matters if you depend on newer PDF 2.0 handling or recent accessibility tooling.

## What you actually do in Acrobat Pro

The free Reader is a viewer. Pro is a workshop. Concretely, here is the work that only shows up in the Pro tier:

**Preflight.** You load a PDF/X-4 or PDF/A-2b profile and Acrobat reports every deviation: fonts not embedded, RGB images in a CMYK job, transparency that will not flatten, overprint settings that will surprise a press operator. Fixups can be applied in bulk. This is the single feature that keeps Acrobat in print shops decades after cheaper viewers appeared.

**Redaction.** You mark text or areas, then *apply* the redaction. The distinction matters: until you apply it, the marks are annotations and the underlying text is still in the file, extractable by anyone. Applied redaction removes the content and can also strip hidden metadata, embedded thumbnails, and attachments — all places where "deleted" text likes to hide.

**OCR.** Scan & OCR turns a page image into selectable, searchable text. Accuracy depends on scan resolution and deskewing; 300 dpi straight scans do well, phone photos of curled pages do not. You can choose the output language, and you can OCR a whole folder through an Action.

**Compare Files.** Two versions of a contract, side by side, with insertions and deletions highlighted. Useful for reviewing redlines without trusting a word processor's change tracking.

**Actions.** Recorded sequences — "optimize for web, add page numbers, flatten to PDF/A-1b, save with a Bates prefix" — run across hundreds of files unattended. This is the closest thing Acrobat has to a scripting environment for non-programmers.

**Accessibility.** The Accessibility Checker flags missing alt text, untagged content, tables without headers, and reading order problems. Passing the checker is not the same as being usable with a screen reader, but it catches the mechanical failures.

**Forms.** You can author a fillable form from scratch or let Acrobat detect field positions on an existing flat form. Field naming, tab order, and calculation scripts are all editable, and JavaScript is available for validation logic.

**Signatures.** Two different things share the word. *Fill & Sign* draws a picture of your signature on the page — fine for internal paperwork, trivial to copy. *Certificate signatures* use a digital ID to cryptographically seal the document and reveal any later modification. If the signature needs to hold up, you want the second kind.

![Acrobats mid-routine](assets/photo.jpg)
*Balance acts and PDFs have one thing in common: the whole thing falls over if one element is slightly out of place. Photo: sasastro, CC BY.*

## Formats and standards worth knowing

Acrobat is where most people first meet the ISO 32000 family, so a short glossary saves confusion:

- **PDF 1.7** — the long-standing baseline, still the safest target for general distribution.
- **PDF 2.0** (ISO 32000-2) — the current specification. Better support for modern color, but not every consumer viewer handles every feature.
- **PDF/A** — archival. No audio, video, or external dependencies; fonts must be embedded. Subparts matter: PDF/A-1 is based on PDF 1.4, PDF/A-2 and PDF/A-3 on PDF 1.7, and PDF/A-3 additionally allows arbitrary embedded files.
- **PDF/X** — print exchange. PDF/X-1a is the conservative CMYK-only workhorse; PDF/X-4 permits live transparency and ICC-based color.
- **PDF/UA** — accessibility. Tagged structure, alt text, correct reading order.
- **PDF/E** and **PDF/VT** — engineering documents and variable-data printing, both narrow but real.

A frequent mistake: exporting a document to PDF/A for archiving, then discovering the file fails validation because a single font was substituted rather than embedded. Acrobat's Preflight will tell you which one.

## Gotchas that cost people time

**Feature parity is not guaranteed across platforms.** Acrobat Pro on macOS and Windows are close but not identical. Certain plug-ins, some Office integration, and a handful of automation hooks have historically been Windows-first or Windows-only. If your workflow depends on a specific tool, verify it exists on your platform before committing.

**Optimize and Save As are different operations.** "Reduce File Size" can downsample images and strip structure in ways that break accessibility tags or flatten layers you wanted. "Save As Other → Optimized PDF" gives you a dialog where you can see exactly what will be discarded. Read it.

**JavaScript in PDFs is restricted.** Modern Acrobat disables most document-level JavaScript by default, and for good reason — it is a well-worn attack surface. If a form's calculations stop working, that setting is usually why.

**Editing text is not word processing.** Acrobat reflows a paragraph as best it can, but it is patching a fixed-layout format. Heavy rewrites belong in the source document, with a fresh export afterward.

**Password protection and permissions are separate.** An open password controls who can view the file. A permissions password controls printing, copying, and editing. Setting only permissions, with no open password, is a weak barrier — and no PDF permission setting is a substitute for not sending the file to someone you do not trust.

## If you are starting from scratch

Open the PDF, look at the right-hand tool pane, and ignore most of it. The tools that earn their place in ordinary work are Edit PDF, Combine Files, Scan & OCR, Compare Files, and Preflight if you touch print. Everything else is situational.

If you are evaluating whether you need Pro at all: Reader covers viewing, printing, and signing. If your task is "read this PDF," you are done. Pro starts paying for itself the moment you need to change what is *inside* the file — reorder pages, fix a scan, redact a name, produce a print-ready PDF/X, or make a fillable form. That is the whole boundary, and it has not moved much in twenty years, whatever the product was called on the box that year.

---
Photos: sasastro · CC BY by; sasastro · CC BY by