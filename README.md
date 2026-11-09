# DevBAI for VS Code

Practice game development in your editor: open a challenge, improve the game code, run visible tests and explain your decisions. DevBAI connects your local work to the website's challenge library and progress tracking.

[Download the extension](https://github.com/siiinbad/DevBAI-Extension/releases/latest) · [Installation guide](https://dev-bai.vercel.app/get-extension) · [Open DevBAI](https://dev-bai.vercel.app) · [Report an issue](https://github.com/siiinbad/DevBAI-Extension/issues)

## Install

1. Open the latest release and download the **.vsix installer** and its **.vsix.sha256 checksum** from Assets. The `.files.txt` file is an inventory, not a checksum. GitHub's Source code archives do not install the extension.
2. Check that the installer's SHA-256 matches the checksum. The installation guide includes Windows, macOS and Linux commands.
3. In desktop VS Code, open **Extensions → … → Install from VSIX**, select the installer and reload if prompted.
4. Click the DevBAI icon in the Activity Bar and sign in with the same GitHub account used on the website. Complete website onboarding and consent if requested.
5. Choose a challenge in **Challenges**, or use **Start in VS Code** on the website. Review the downloaded workspace before granting trust.

DevBAI is currently distributed through GitHub Releases. It is not published to the VS Code Marketplace. Students do not need the private application repository, pnpm, database access or a local Spring Boot server. Sign-in, downloads and progress synchronization use the hosted DevBAI service.

## What you can do

- Practice Java, Python, JavaScript, HTML and CSS through game-development activities.
- Read instructions, open supplied source files and run the challenge's visible tests locally.
- Complete code-reading and written-reasoning activities without a compiler.
- Submit your work and explanation explicitly for assessment using your own GitHub Copilot account in VS Code.
- Review provisional feedback and practice levels, with local drafts preserved across editor sessions.
- Use Health diagnostics and pause/resume controls when checking setup or synchronization.

Version 0.2.4 adds **Prepare tools / repair setup**, clearer diagnostics and improved language-runtime discovery. Version 0.2.5 adds a dedicated **Evaluation complete** display, automatic Feedback opening, submission-state checks and **Retake challenge**, preserving local source and drafts. Check the release version before expecting those newer controls; downloading 0.2.4 does not include the 0.2.5 update.

## Requirements

- **Desktop VS Code 1.91.0 or later.** Use a current supported release for live Copilot access; GitHub's provider may impose newer requirements.
- **Java:** a complete JDK 17+ with both `java` and `javac`. The challenge includes Maven wrappers. Red Hat Java support is optional editor assistance in corrected builds.
- **Python:** Python 3.10+. Supported commands include `python3`, `python` and the Windows `py -3` launcher in version 0.2.4 and later.
- **JavaScript, HTML and CSS:** Node.js 22+ for the supplied local tests.
- **Reading and written activities:** no language compiler is required.

The same VSIX is intended for Windows, macOS and Linux. Language tools must be installed on the computer running the challenge. Check each release's evidence and notes; platform support does not establish that every device or configuration has been tested.

## Copilot and your work

Website GitHub sign-in and VS Code Copilot sign-in are separate. Assessment uses your signed-in Copilot account and available allowance, after your explicit confirmation and any model-access consent requested by VS Code. DevBAI does not guarantee a free model allowance or ask students to paste a Copilot token into settings.

Editing and running tests keep source on your computer. Background synchronization sends permitted activity metadata. Explicit assessment/submission sends the allowed work, explanation or reading answers for processing. Visible tests alone do not trigger AI assessment, and Copilot feedback remains provisional.

## Results and retakes

In version 0.2.5 and later, Project distinguishes **Attempt in progress**, **Evaluation in progress**, **Evaluation complete**, **Needs review** and closed attempts. Results refresh automatically. Completed attempts require **Retake challenge** before another submission; retaking keeps local code and drafts and preserves the previous attempt record. A Needs review attempt may be revised and submitted again unless finalized.

Earlier versions may show `DEVBAI-E099 (ATTEMPT_STATE)` when submitting a completed attempt. Use Sync now to read its status, wait if evaluation is pending, or reopen a completed challenge with **Reuse existing workspace**. See the troubleshooting guide for details.

## Help

Run **DevBAI: Run Diagnostics** from the Command Palette, or open **Health** in the dashboard. A **Not checked** row means that Diagnostics did not perform that check; it does not establish a failure. Diagnostics does not execute student code or spend Copilot allowance.

When reporting an issue, include the extension version, operating system, action that failed, full error message and redacted diagnostic report. Keep tokens, passwords, private source and connection strings out of public issues.

This public repository distributes the extension and user-facing documentation. The DevBAI application source is maintained separately.
