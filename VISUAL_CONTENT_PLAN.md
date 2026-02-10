# Visual Content Plan: Videos & Screenshots

Step-by-step instructions for creating videos and taking screenshots to complete the DocsAutomator documentation.

## Current State

- **17 pages** have visual content (videos and/or screenshots)
- **50 pages** have zero visual content
- Airtable integration page is the gold standard — has a video + 6 annotated screenshots
- Quickstart guide has 6 screenshots showing the full setup flow
- Most feature pages, all use case pages, and the new PDF/eSign content have no visuals

---

## Priority 1: Videos (High Impact)

These videos will be embedded at the top of their respective pages using the `<Frame><iframe>` pattern.

### Video 1: PDF Template Editor Walkthrough

**Page:** `docsautomator-basics/pdf-template-guide.mdx`
**Duration:** 2-3 minutes
**Embed at:** Top of page, right after the intro paragraph

Record in the DocsAutomator app:

1. Open an automation and click the template section
2. Show the toggle between "Google Docs" and "Existing PDF"
3. Select "Existing PDF"
4. Drag and drop a sample PDF (use a pre-designed invoice or certificate with clear empty fields)
5. Show the "X fields auto-detected" notification if the PDF has AcroForm fields
6. Click the edit button to open the placeholder editor
7. **Pan the three-panel layout** — left sidebar (field types), center (PDF viewer), right sidebar (properties)
8. Add a **text** placeholder — drag it from the sidebar onto a name field area on the PDF
9. Name it "customer_name" in the properties panel
10. Change the font to Roboto, size to 14, color to dark blue
11. Show the **alignment** dropdown (left/center/right)
12. Show the **overflow** dropdown — briefly explain "Shrink to fit" vs "Expand vertically"
13. Add an **image** placeholder — drag it onto a logo area
14. Add a **checkbox** placeholder
15. Add an **e-signature** field — show the "Add E-Sign Field" section in the left sidebar, add a signature field
16. Show **multi-page** — scroll down to page 2 and add a field there
17. Click **Preview** to show the live preview with sample data
18. Click **Save**
19. Brief voiceover: "The PDF itself is never modified — DocsAutomator overlays your data on top at generation time"

---

### Video 2: E-Signature Setup & Signing Flow

**Page:** `features/docsautomator-esign.mdx` (replace or supplement existing video if outdated)
**Duration:** 3-4 minutes
**Embed at:** Top of page (already has a video embed — update the YouTube URL if creating a new one)

Record:

1. Open a Google Doc template that has e-sign placeholders (`{{esign.signature.1}}`, `{{esign.date.1}}`)
2. Go to the automation's output settings
3. Enable "E-Signatures"
4. **Configure Signer 1** — enter email field mapping, name field mapping
5. Add **Signer 2** — show the "Add Signer" button
6. Show **Signing Order** toggle — explain "Sequential" vs "Parallel"
7. Show **Email Configuration** — subject, body with variables (`{{signerName}}`, `{{documentName}}`), button color
8. Show **Reminder Settings** — enable reminders, set frequency
9. Show **Expiration Settings**
10. Show **Branding** — upload a custom logo
11. Click Preview or generate a test document
12. **Switch to the signer's perspective** — open the signing link in a new tab or incognito
13. Show the signing experience:
    - Review document
    - Click on signature field → draw or type signature
    - Date auto-fills
    - Fill in text field
    - Check the checkbox
    - Click "Complete Signing"
14. Show the **completion screen** with download option
15. Back in the app: show the signing session status changed to "completed"
16. Show the **audit trail** if visible

---

### Video 3: Updated Platform Overview

**Page:** `index.mdx`
**Duration:** 2 minutes
**Embed at:** Already has a video — update the YouTube URL to the new version

The current "DocsAutomator in 2 minutes" video may not cover PDF templates or eSign. Record an updated version:

1. Quick intro: "DocsAutomator turns your data into documents — PDFs, Google Docs, with optional e-signatures"
2. Show **template choice**: Google Docs (show a template with `{{placeholders}}`) AND PDF templates (show the visual editor briefly)
3. Show **data source connection** — pick Airtable, show base/table selection
4. Show **field mapping** — map a few fields
5. Show **preview** — generate a preview PDF
6. Show **output settings** — email, Drive, e-signatures
7. Show a **generated document** — the final PDF
8. Show the **e-signing flow** — 10 seconds showing a signer signing
9. End card: "Get started free at docsautomator.co"

---

### Video 4: Quickstart — Full Setup in 5 Minutes

**Page:** `docsautomator-basics/quickstart-guide.mdx`
**Duration:** 4-5 minutes
**Embed at:** Top of page (currently has no video)

Record the entire quickstart flow:

1. Log into the DocsAutomator dashboard
2. Click "New Automation"
3. Choose a data source (Airtable or Google Sheets)
4. Connect your account (show OAuth flow)
5. **Google Doc path**: Paste a template link, show Template Check
6. **Brief PDF path**: Show the toggle, upload a PDF, position 1-2 fields (keep this under 30 seconds — link to Video 1 for full details)
7. Select base/table
8. Map fields — show the field mapping interface
9. Generate a preview
10. Configure output settings (save PDF, send email)
11. Mention e-signatures as an option
12. Show the final generated document

---

## Priority 2: Screenshots (Essential Pages)

Save all screenshots to `/docs/images/{section}/` with descriptive filenames. Use `<Frame>` wrapper for consistent styling.

### Screenshots for: PDF Template Guide

**Directory:** `/docs/images/pdf-template/`

Take these screenshots in the DocsAutomator app:

| # | Filename | What to capture | Where in the doc |
|---|----------|----------------|-----------------|
| 1 | `template-type-toggle.png` | The template section showing "Google Docs" and "Existing PDF" toggle buttons | After "Select PDF template" step |
| 2 | `upload-area.png` | The drag-and-drop upload area (empty state) | After "Upload your PDF" step |
| 3 | `uploaded-pdf-info.png` | After upload — showing filename, page count, placeholder count, Edit/Delete buttons | After "Review detected fields" step |
| 4 | `editor-full-view.png` | Full-screen editor with a PDF loaded, showing all 3 panels (left sidebar, center PDF, right properties) with a few placeholders placed | Top of "The Visual Placeholder Editor" section |
| 5 | `editor-left-sidebar.png` | Close-up of left sidebar showing field type buttons (Text, Image, Checkbox) and e-sign fields section | "Adding Placeholders" section |
| 6 | `editor-placeholder-selected.png` | A text placeholder selected on the PDF, showing the blue selection handles and the properties panel populated on the right | "Positioning and Resizing" section |
| 7 | `properties-text.png` | Right panel showing text properties: font family dropdown, font size, color picker, alignment, overflow mode | "Text Properties" section |
| 8 | `properties-overflow.png` | The overflow mode dropdown expanded showing all 4 options | "Text Overflow Modes" section |
| 9 | `preview-mode.png` | The editor in preview mode — showing the PDF with sample data filled into placeholders | "Preview Mode" section |
| 10 | `esign-fields.png` | Left sidebar showing the "Add E-Sign Field" section with signature, date, text, checkbox options | "E-Signature Fields on PDFs" section |

---

### Screenshots for: Google Doc Template Guide

**Directory:** `/docs/images/google-doc-template/`

| # | Filename | What to capture | Where in the doc |
|---|----------|----------------|-----------------|
| 1 | `template-example.png` | A Google Doc template with visible `{{placeholders}}` — use an invoice template with 5-6 placeholders highlighted | Top of "Template Syntax" section |
| 2 | `generated-output.png` | The same template after generation — showing the filled-in document | Below the template example (before/after) |
| 3 | `line-items-template.png` | A Google Doc showing line item syntax (the table with `{{#items}}` and `{{/items}}` tags) | "Line Item Variables" section |
| 4 | `line-items-output.png` | The generated document with the line item table expanded with real data | Next to the template screenshot |
| 5 | `esign-placeholders.png` | A Google Doc showing e-sign placeholders at the bottom of a contract (`{{esign.signature.1}}`, `{{esign.date.1}}`) | New "E-Signature Placeholders" section |
| 6 | `image-placeholder.png` | A Google Doc showing `{{image_logo}}` placeholder and the resulting image in the output | "Image Variables" section |

---

### Screenshots for: Quickstart Guide (supplement existing)

**Directory:** `/docs/images/quickstart/`

These screenshots may already exist but need updating for PDF template + eSign:

| # | Filename | What to capture | Where in the doc |
|---|----------|----------------|-----------------|
| 1 | `template-type-choice.png` | The template section showing both Google Doc and PDF options | Step 3 (PDF Template tab) |
| 2 | `esign-output-toggle.png` | Output settings with the e-signature toggle visible/enabled | Step 5 (near the eSign Info callout) |

---

### Screenshots for: E-Signature Pages

**Directory:** `/docs/images/esign/`

| # | Filename | What to capture | Where in the doc |
|---|----------|----------------|-----------------|
| 1 | `signer-configuration.png` | The signer setup panel — email field, name field, "Add Signer" button | `docsautomator-esign.mdx` — "Configuring Signers" section |
| 2 | `signing-order.png` | The Sequential vs Parallel toggle | "Signing Order" section |
| 3 | `email-configuration.png` | Email template editor — subject, body with variables, button color picker | "Email Configuration" section |
| 4 | `signing-experience.png` | The signer's view — document with signature field highlighted, ready to sign | "Signing Experience" section |
| 5 | `signature-drawn.png` | After signing — the signature drawn in the field | Same section |
| 6 | `completion-screen.png` | The "Signing Complete" screen with download button | Same section |
| 7 | `session-status.png` | The signing session list in the app showing status (pending, completed, etc.) | "Session Statuses" section |
| 8 | `audit-trail.png` | The audit trail showing timeline of events (sent, viewed, signed) | For the compliance page or main eSign page |

---

### Screenshots for: Use Case Pages

**Directory:** `/docs/images/use-cases/`

Each use case page should have 3-4 screenshots showing the end-to-end flow:

**Invoices from Airtable** (`use-cases/invoices-from-airtable.mdx`):

| # | Filename | What to capture |
|---|----------|----------------|
| 1 | `invoice-template.png` | The Google Doc invoice template with placeholders visible |
| 2 | `invoice-airtable-data.png` | The Airtable base with sample invoice data (customer, items, amounts) |
| 3 | `invoice-field-mapping.png` | The field mapping interface with invoice fields mapped |
| 4 | `invoice-generated.png` | The final generated invoice PDF |

**Bulk Certificates from Google Sheets** (`use-cases/bulk-certificates-from-google-sheets.mdx`):

| # | Filename | What to capture |
|---|----------|----------------|
| 1 | `certificate-template.png` | The Google Doc certificate template |
| 2 | `certificate-sheets-data.png` | The Google Sheet with participant names, course names, dates |
| 3 | `certificate-generated.png` | A generated certificate PDF |
| 4 | `certificate-batch-queue.png` | The queue/batch processing view showing multiple certificates being generated |

**Contracts with E-Sign** (`use-cases/contracts-with-esign.mdx`):

| # | Filename | What to capture |
|---|----------|----------------|
| 1 | `contract-template.png` | The contract template with e-sign placeholders at the bottom |
| 2 | `contract-esign-config.png` | The e-signature output settings configured with 2 signers |
| 3 | `contract-signing.png` | The signer's view of the contract with signature fields |
| 4 | `contract-completed.png` | The completed signed contract PDF |

---

## Priority 3: Screenshots (Feature Pages)

These pages are text-only and would benefit from at least 1-2 screenshots each.

### Line Items

**Directory:** `/docs/images/line-items/`

| # | Filename | Page | What to capture |
|---|----------|------|----------------|
| 1 | `line-items-template.png` | `features/line-items.mdx` | Google Doc template with line item table syntax |
| 2 | `line-items-generated.png` | `features/line-items.mdx` | Generated document with expanded table rows |
| 3 | `nested-template.png` | `features/line-items/nested-line-items.mdx` | Template showing 2-level nested line items |
| 4 | `nested-generated.png` | `features/line-items/nested-line-items.mdx` | Generated document with nested rows |
| 5 | `grouping-template.png` | `features/line-items/line-items-grouping-+-calculations.mdx` | Template with grouping/calculation syntax |
| 6 | `grouping-generated.png` | `features/line-items/line-items-grouping-+-calculations.mdx` | Generated document with grouped rows and totals |

### Conditional Content

**Directory:** `/docs/images/conditional/`

| # | Filename | Page | What to capture |
|---|----------|------|----------------|
| 1 | `conditional-show-hide-config.png` | `features/advanced-placeholder-options/conditional-show-hide.mdx` | The conditional rendering configuration in the app |
| 2 | `conditional-show-result.png` | Same | Generated doc with section shown |
| 3 | `conditional-hide-result.png` | Same | Generated doc with section hidden |
| 4 | `conditional-styling-config.png` | `features/advanced-placeholder-options/conditional-styling.mdx` | The conditional styling rules configuration |
| 5 | `conditional-styling-result.png` | Same | Generated doc showing styled text |

### AI Field Mapping

**Directory:** `/docs/images/ai-field-mapping/`

| # | Filename | Page | What to capture |
|---|----------|------|----------------|
| 1 | `ai-mapping-suggestions.png` | `features/ai-field-mapping.mdx` | The field mapping interface showing AI-suggested matches (with the "AI" badge or indicator) |
| 2 | `ai-mapping-accepted.png` | Same | After accepting AI suggestions — all fields mapped |

### Output Settings

**Directory:** `/docs/images/output/`

| # | Filename | Page | What to capture |
|---|----------|------|----------------|
| 1 | `email-config.png` | `features/actions-after-document-generation/send-email.mdx` | Email configuration panel — recipient, subject, body, attachment toggle |
| 2 | `drive-folder-config.png` | `features/actions-after-document-generation/save-pdfs-in-google-drive.mdx` | Google Drive folder selection interface |
| 3 | `merge-pdfs-config.png` | `features/actions-after-document-generation/merge-existing-pdfs.mdx` | The merge PDF configuration — prepend/append toggle, file URL field |
| 4 | `webhook-config.png` | `features/actions-after-document-generation/notify-webhook.mdx` | Webhook URL configuration field |

### Other Feature Pages

| # | Filename | Page | What to capture |
|---|----------|------|----------------|
| 1 | `images/previews/preview-panel.png` | `features/document-previews.mdx` | The preview panel showing a generated PDF preview |
| 2 | `images/run-history/run-list.png` | `features/run-history.mdx` | The run history list showing recent document generations with status |
| 3 | `images/run-history/run-detail.png` | `features/run-history.mdx` | A single run detail view showing input data, output PDF, timing |
| 4 | `images/folders/folder-view.png` | `features/folder-organization.mdx` | The automation list organized in folders |
| 5 | `images/team/team-members.png` | `features/team-management.mdx` | The team management panel showing members and roles |
| 6 | `images/workspaces/workspace-switcher.png` | `features/workspaces.mdx` | The workspace switcher dropdown |

---

## Priority 4: Integration Page Videos

These integration pages currently have NO video. Consider recording short (1-2 min) setup walkthroughs:

| Page | Video content |
|------|--------------|
| `integrations-api/make.mdx` | Setting up a Make scenario that triggers DocsAutomator document generation |
| `integrations-api/noloco.mdx` | Connecting Noloco to DocsAutomator and triggering a document |
| `integrations-api/docsautomator-mcp.mdx` | Using the MCP server with Claude or another AI tool to generate documents |

(Airtable, Google Sheets, SmartSuite, ClickUp, Glide, Zapier, n8n, and Softr already have videos.)

---

## Screenshot Guidelines

### Technical specs
- **Resolution:** Take at 2x (Retina) for crisp rendering, save at original size
- **Format:** PNG for UI screenshots, JPG for full-page captures (smaller file size)
- **Browser:** Use Chrome with a clean profile (no extensions in the toolbar)
- **Window size:** 1280px wide for full-page screenshots, crop for focused UI elements
- **Dark mode:** Use light mode for all screenshots (matches the docs theme)

### Composition tips
- **Crop tightly** around the relevant UI — don't include browser chrome or unrelated sidebar
- **Highlight important elements** with a subtle red/orange rectangle or arrow annotation (use Cleanshot X or similar)
- **Use realistic data** — "Acme Corp", "INV-2025-001", real-looking names and amounts. Avoid "test", "asdf", "foo"
- **Consistent sample data** across related screenshots — same invoice, same customer throughout a tutorial
- **Show the happy path** — all fields filled, no errors, clean state

### Annotation style
- Red/orange rectangles for callouts (2px border, no fill)
- Numbered circles for step-by-step sequences
- Keep annotations minimal — the screenshot should mostly speak for itself

---

## Video Guidelines

### Technical specs
- **Resolution:** 1920x1080 minimum, 4K preferred
- **Frame rate:** 30fps
- **Format:** Upload to YouTube, embed with `<Frame><iframe>` in the docs
- **Audio:** Clear voiceover with no background music (or very subtle music)

### Recording tips
- **Clean browser** — hide bookmarks bar, use a clean Chrome profile
- **Zoom the UI** to 125-150% so elements are clearly visible in the video
- **Slow, deliberate mouse movements** — don't rush, viewers need to follow
- **Pause briefly** on important screens (2-3 seconds) before moving on
- **Use realistic data** — same guidelines as screenshots
- **Record in one take** if possible — cuts are fine but keep them smooth
- **Add captions/subtitles** on YouTube for accessibility

### Voiceover script tips
- Narrate what you're doing and WHY, not just clicking through
- Mention keyboard shortcuts when relevant ("I'll press Cmd+Z to undo")
- End with a clear call-to-action ("Check out the template guide for more details")

---

## File Structure

After creating all visual content, the images directory should look like:

```
docs/images/
├── airtable/              (existing - 6 screenshots)
├── quickstart/            (existing - 7 screenshots, add 2 more)
├── pdf-template/          (new - 10 screenshots)
├── google-doc-template/   (new - 6 screenshots)
├── esign/                 (new - 8 screenshots)
├── use-cases/             (new - 12 screenshots)
├── line-items/            (new - 6 screenshots)
├── conditional/           (new - 5 screenshots)
├── ai-field-mapping/      (new - 2 screenshots)
├── output/                (new - 4 screenshots)
├── previews/              (new - 1 screenshot)
├── run-history/           (new - 2 screenshots)
├── folders/               (new - 1 screenshot)
├── team/                  (new - 1 screenshot)
└── workspaces/            (new - 1 screenshot)
```

**Total new screenshots needed: ~60**
**Total new videos needed: 4 (Priority 1) + 3 (Priority 4) = 7**

---

## Embedding Reference

### Screenshot embed pattern
```mdx
<Frame>
  <img src="/images/{section}/{filename}.png" alt="Descriptive alt text for accessibility" />
</Frame>
```

### Video embed pattern
```mdx
<Frame>
  <iframe
    width="100%"
    height="400"
    src="https://www.youtube.com/embed/{VIDEO_ID}"
    title="Video title"
    frameBorder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowFullScreen
  />
</Frame>
```
