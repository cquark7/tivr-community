<h1 align="center">
  <img src="assets/tivr-logo.svg" alt="tivr" width="320">
</h1>

<p align="center"><strong>From my workbench to yours.</strong></p>

<p align="center">
  <a href="https://tivr.dev"><strong>Open the workbench →</strong></a>
  · <a href="#find-your-next-tool">Explore the tools</a>
  · <a href="#privacy-by-design">How privacy works</a>
  · <a href="https://github.com/cquark7/tivr-community/issues/new?template=feature_request.yml">Suggest what comes next</a>
</p>

---

**[tivr](https://tivr.dev) is a growing collection of browser-based tools for code, data, images, and documents.** Format JSON, compare text, preview Markdown, inspect Parquet files, or clean up an image. Your tool inputs are processed in your browser and never uploaded.

**Free to use · No signup · No ads · No installation**

This is the community home for tivr: find a tool, read its guide, report a problem, or help shape what comes next.

## Privacy by design

You should know what happens to your work before you open it in a tool.

- **Inputs stay on your device.** Files, text, and passwords are processed locally; tools have no upload path or server-side processing service for them.
- **No application tracking.** No tracking cookies, browser analytics scripts, or visitor identifiers are added by tivr.
- **You control saved drafts.** Supported editors save drafts in this browser by default. [Privacy settings](https://tivr.dev/settings) let you stop new saves and delete existing drafts. Turning saving off does not delete drafts already stored. Preferences also stay in your browser.
- **External images need permission.** Images hosted elsewhere are blocked until you load one or allow external content in settings. Loading an image shares your IP address and the image URL with its host; that URL can itself contain private information.
- **Sharing is an explicit choice.** A tool's share link can contain its document text. Anyone with the link can read it, and browser history may retain it. Feedback and support services handle what you submit under their own policies; tool content is not attached automatically.

**Local processing does not mean no network traffic.** Pages, fonts, code, engines, and models download from tivr.dev. The hosting provider handles request information such as IP addresses, requested URLs, and timestamps.

**[Read the full privacy explanation →](https://tivr.dev/privacy)** · **[Manage privacy settings →](https://tivr.dev/settings)**

## Technical safeguards

| Safeguard                        | What it does                                                                                                                                                         |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **HTTPS and transport security** | Encrypt delivery of the site and tell supporting browsers to use HTTPS on later visits.                                                                              |
| **Self-hosted assets**           | Fonts, scripts, processing engines, and models come from tivr.dev, with no third-party runtime CDNs.                                                                 |
| **Browser security policies**    | Restrict script sources and network connections, block form submissions, prevent other sites from framing tivr, and disable camera, microphone, and location access. |
| **Sanitized previews**           | Filter scripts, event handlers, and unsafe URLs out of user-provided HTML before rendering.                                                                          |
| **Automated release checks**     | Flag common upload-capable APIs and unreviewed external URLs in application source.                                                                                  |

These safeguards support the no-upload design, but headers alone cannot prove that a network request carries no content.

<details>
<summary><strong>Verify a workflow yourself</strong></summary>

1. **Watch the network.** Open your browser's developer tools, choose Network, and try a tool with invented data. Inspect request URLs, query parameters, and payloads for that data. Page and engine downloads, approved external images, and hosting diagnostics are described above.
2. **Inspect the response headers.** Select the page request and look for `Content-Security-Policy`, `Strict-Transport-Security`, and `Permissions-Policy`. You can also inspect them from a terminal:

   ```bash
   curl -I https://tivr.dev/privacy
   ```

3. **Check local storage.** Open Application → Storage, or your browser's site-data settings. Compare saved drafts before and after changing the draft setting or deleting a draft. Clearing site data removes saved drafts, preferences, and cached site assets.

Network inspection covers the workflow you test, not every possible tool interaction.

</details>

## Designed for every screen

- **Phones, tablets, and desktops.** Responsive layouts adapt from narrow mobile screens to wide desktop workspaces, with care for readable text, reachable controls, touch interaction, and keyboard-and-mouse usability.
- **Light and dark mode.** Both themes receive the same attention to contrast, legibility, and visual polish.

## Find your next tool

Browse by task; each app guide explains its features.

### Security

| Tool                                                          | Your next small task                                        | App guide                                       |
| ------------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------- |
| **[Password Generator](https://tivr.dev/password-generator)** | Generate strong passwords or memorable passphrases          | [Read guide](apps/password-generator/README.md) |
| **[PDF Password Remover](https://tivr.dev/pdf-unlocker)**     | Unlock a PDF with its password and save an unprotected copy | [Read guide](apps/pdf-unlocker/README.md)       |

### Text & Code

| Tool                                                      | Your next small task                                               | App guide                                     |
| --------------------------------------------------------- | ------------------------------------------------------------------ | --------------------------------------------- |
| **[Markdown Editor](https://tivr.dev/markdown-preview)**  | Write Markdown and see the formatted result as you type            | [Read guide](apps/markdown-preview/README.md) |
| **[Text Compare](https://tivr.dev/diff-checker)**         | Compare two texts and see exactly what changed                     | [Read guide](apps/diff-checker/README.md)     |
| **[Monty Playground](https://tivr.dev/monty-playground)** | Try Monty, Pydantic’s Rust-based Python 3.14 interpreter & sandbox | [Read guide](apps/monty-playground/README.md) |

### Images

| Tool                                                          | Your next small task                                 | App guide                                       |
| ------------------------------------------------------------- | ---------------------------------------------------- | ----------------------------------------------- |
| **[Background Remover](https://tivr.dev/background-remover)** | Remove an image background and clean up the edges    | [Read guide](apps/background-remover/README.md) |
| **[AI Image Upscaler](https://tivr.dev/image-upscaler)**      | Enlarge images up to 4× and compare before and after | [Read guide](apps/image-upscaler/README.md)     |

### Data

| Tool                                                            | Your next small task                                                 | App guide                                       |
| --------------------------------------------------------------- | -------------------------------------------------------------------- | ----------------------------------------------- |
| **[Parquet Viewer & SQL](https://tivr.dev/parquet-viewer-sql)** | Browse Parquet files up to 2 GB, with SQL available when you need it | [Read guide](apps/parquet-viewer-sql/README.md) |
| **[JSON Formatter](https://tivr.dev/json-formatter)**           | Format JSON, fix syntax errors, and explore nested data              | [Read guide](apps/json-formatter/README.md)     |

## Built out of a familiar frustration

> “I wanted tools I could trust.”

**[Read the story behind tivr →](https://tivr.dev/about)**

## Help shape the workbench

Specific, reproducible reports are easiest to act on.

- **[Report a bug](https://github.com/cquark7/tivr-community/issues/new?template=bug_report.yml)** with the tool, what happened, and a small example that reproduces the issue.
- **[Suggest a feature or a new tool](https://github.com/cquark7/tivr-community/issues/new?template=feature_request.yml)** by describing the task you're trying to finish.
- **[Browse existing requests](https://github.com/cquark7/tivr-community/issues)** and add a 👍 when someone has already described your need.
- **Include a useful workflow** in a request or report to show how you use the tool.

Use invented examples and leave sensitive information out of public posts. The [participation guide](CONTRIBUTING.md) explains how to make a useful report. For direct feedback, email **[contact@tivr.dev](mailto:contact@tivr.dev)**.

### Report a security concern privately

Email **[contact@tivr.dev](mailto:contact@tivr.dev)** with the affected tool or page, what you observed, and steps to reproduce using invented data. Keep exploitable details out of public issues and leave credentials and private documents out of the report. There is no guaranteed response time or paid bounty program.

## Keep a good tool within reach

**If tivr earns a place in your bookmarks, give this repo a ⭐.** It helps others discover the workbench.

New tools and improvements are posted on the [updates page](https://tivr.dev/updates), with an [RSS feed](https://tivr.dev/updates.xml) for your reader. If you'd like to help with the running costs, you can also [support tivr](https://tivr.dev/support).
