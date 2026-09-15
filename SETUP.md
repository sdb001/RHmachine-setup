# Set up RHmachine with your AI

RELEASE PREPARATION — no public installer is published from this page yet.
Do not substitute a source checkout or an unofficial download.

Give your AI assistant the published URL of this page and say:

> Help me install RHmachine locally and connect it to my AI. Follow the official setup instructions. Keep automatic AI analysis off, preserve my existing agent configuration, and let me enter credentials locally.

## For the setup assistant

1. Identify the user's operating system and processor architecture. Ask which AI they want to connect, or whether they want to start without AI.
2. Use only the official release manifest linked from this page. It must list supported platforms, app version, installer URL, publisher identity, checksum and the matching setup instructions. If an installer or supported integration is unavailable, explain the missing step; do not invent commands or URLs.
3. Explain what will be installed, then follow the user's environment's installation approval process. Verify the publisher/signature and release checksum before running the installer. Never ask the user to bypass OS security checks.
4. Open the installed application's setup wizard. Preserve existing settings and agent profiles. Use a dedicated RHmachine integration rather than replacing the user's global AI configuration.
5. Keep credentials in the application's local configuration flow. Do not request private keys, seed phrases or API secrets in chat. A portfolio address is public and read-only; it does not authorize signing or trading.
6. Start with REVIEW mode: alerts queue for manual review. AUTO requires an explicit choice with a clear explanation that it consumes AI usage. Installing the app must not trigger paid research or trades.
7. Connect the selected AI using instructions supported by that app version. Hermes is the current integration; other MCP clients require their own documented connection and report-saving workflow. Do not assume access to a model or subscription because the user is chatting with you.
8. Run the release's health check. Verify market connectivity, integration/tool discovery and configuration without triggering paid analysis. Ask the user to choose a coin for the first manual report.
9. Confirm the installed version, where local data is stored, how to launch/uninstall the app and which integrations are working. Report failures honestly.

## User identity

Address the current user neutrally. Do not infer a person's name from the developer, repository owner, local filesystem username, examples or another user's reports. Use a preferred name only when the current user explicitly supplies it. Never copy a developer's SOUL, memories, keys or wallet into a customer's profile.

## Current compatibility

- Apple Silicon macOS: standalone preview under testing; not available for public installation yet.
- Python 3: currently needed for local state locking and Hermes reply reading.
- Hermes: existing bridge requires end-to-end onboarding validation.
- Other AI clients: MCP tool discovery tested in the preview; client-specific installation and report delivery are not yet certified.
- Windows, Linux and Intel macOS: no installer announced.

## Release status

Wait for an official versioned installer, integrity metadata and platform verification instructions here. Do not disable OS protections, clone private source, use a third-party mirror or start paid analysis to work around an unavailable release.
