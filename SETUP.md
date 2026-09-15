# Set up RHmachine with your AI

UNSIGNED PRIVATE BETA — installers are shared privately; this page has no public download.
Do not substitute a source checkout or an unofficial download.

Give your AI assistant the published URL of this page and say:

> Help me install RHmachine locally and connect it to my AI. Follow the official setup instructions. Keep automatic AI analysis off, preserve my existing agent configuration, and let me enter credentials locally.

## For the setup assistant

1. Identify the user's operating system and processor architecture. Ask which AI they want to connect, or whether they want to start without AI.
2. Use the official public release manifest when available, or the privately supplied beta archive, build-info.json, SHA256SUMS and matching README for an invited tester. Check supported platform, version, integrity metadata and distribution status. If an installer or supported integration is unavailable, explain the missing step; do not invent commands or URLs.
3. Explain what will be installed, then follow the user's environment's installation approval process. For signed releases, verify publisher/signature and release checksum. For this unsigned beta, explain that checksums detect corruption but do not authenticate the publisher; use only the archive supplied through the trusted private beta channel. Never ask the user to bypass OS security checks.
4. Open the installed application's setup wizard. Preserve existing settings and agent profiles. Use a dedicated RHmachine integration rather than replacing the user's global AI configuration.
5. Keep credentials in the application's local configuration flow. Do not request private keys, seed phrases or API secrets in chat. A portfolio address is public and read-only; it does not authorize signing or trading.
6. Start with REVIEW mode: alerts queue for manual review. AUTO requires an explicit choice with a clear explanation that it consumes AI usage. Installing the app must not trigger paid research or trades.
7. Connect the selected AI using instructions supported by that app version. Hermes is the current integration; other MCP clients require their own documented connection and report-saving workflow. Do not assume access to a model or subscription because the user is chatting with you.
8. Run the release's health check. Verify market connectivity, integration/tool discovery and configuration without triggering paid analysis. Ask the user to choose a coin for the first manual report.
9. Confirm the installed version, where local data is stored, how to launch/uninstall the app and which integrations are working. Report failures honestly.

## User identity

Address the current user neutrally. Do not infer a person's name from the developer, repository owner, local filesystem username, examples or another user's reports. Use a preferred name only when the current user explicitly supplies it. Never copy a developer's SOUL, memories, keys or wallet into a customer's profile.

## Current compatibility

- Apple Silicon macOS: unsigned private beta 2.1.0-beta.1; shared privately, not a public stable release.
- Python 3: currently needed for local state locking and Hermes reply reading.
- Hermes: isolated profile connector tested for configuration preservation; authenticated provider/report acceptance testing remains.
- Other AI clients: MCP configuration export and tool discovery tested. The dashboard i key uses Hermes; other clients can research and save reviews through MCP. Client-specific acceptance testing remains.
- Windows, Linux and Intel macOS: no installer announced.

## Release status

For an invited beta tester, use the privately supplied versioned archive, SHA256SUMS and included README. Confirm that the user understands it is unsigned and may be blocked by macOS. Do not bypass OS security protections. For everyone else, wait for a public download here. Do not disable OS protections, clone private source, use a third-party mirror or start paid analysis to work around an unavailable release.

## API onboarding

Public Robinhood RPC, DexScreener and GeckoTerminal endpoints are built in; no shared private keys are distributed. Provider limits and coverage still apply. The setup wizard offers optional private HTTPS RPC, Nansen, HyperSync, X and Bubblemaps credentials. Tell the user to enter these locally in the hidden-input prompt, never in AI chat. Blank preserves an existing value.

Nansen snapshots are disabled in fresh configuration until a key is added. Adding one enables scheduled snapshots within the configured daily cap (50 credits by default). Research services can consume the customer's provider credits when used. Setup makes no validation requests; SAVED is not VALIDATED. Start with public feeds if credentials are unavailable.
