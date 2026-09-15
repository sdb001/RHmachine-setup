# Set up RHmachine with your AI

UNSIGNED BETA — publicly downloadable for Apple Silicon macOS. Application source remains private.
Do not substitute a source checkout or an unofficial download.

Give your AI assistant the published URL of this page and say:

> Help me install RHmachine locally and connect it to my AI. Follow the official setup instructions. Keep automatic AI analysis off, preserve my existing agent configuration, and let me enter credentials locally.

## For the setup assistant

1. Identify the user's operating system and processor architecture. Ask which AI they want to connect, or whether they want to start without AI.
2. Use the official release links below: the beta archive, SHA256SUMS and matching README. The extracted archive contains build-info.json with per-file hashes. Check supported platform, version, integrity metadata and distribution status. If an installer or supported integration is unavailable, explain the missing step; do not invent commands or URLs.
3. Explain what will be installed, then follow the user's environment's installation approval process. For signed releases, verify publisher/signature and release checksum. For this unsigned beta, explain that checksums detect corruption but do not authenticate the publisher; download only from the official release linked below. Never ask the user to bypass OS security checks.
4. Open the installed application's setup wizard. Preserve existing settings and agent profiles. Use a dedicated RHmachine integration rather than replacing the user's global AI configuration.
5. Keep credentials in the application's local configuration flow. Do not request private keys, seed phrases or API secrets in chat. A portfolio address is public and read-only; it does not authorize signing or trading.
6. Start with REVIEW mode: alerts queue for manual review. AUTO requires an explicit choice with a clear explanation that it consumes AI usage. Installing the app must not trigger paid research or trades.
7. Connect the selected AI using instructions supported by that app version. Hermes is the current integration; other MCP clients require their own documented connection and report-saving workflow. Do not assume access to a model or subscription because the user is chatting with you.
8. Run the release's health check. Verify market connectivity, integration/tool discovery and configuration without triggering paid analysis. Ask the user to choose a coin for the first manual report.
9. Confirm the installed version, where local data is stored, how to launch/uninstall the app and which integrations are working. Report failures honestly.

## User identity

Address the current user neutrally. Do not infer a person's name from the developer, repository owner, local filesystem username, examples or another user's reports. Use a preferred name only when the current user explicitly supplies it. Never copy a developer's SOUL, memories, keys or wallet into a customer's profile.

## Current compatibility

- Apple Silicon macOS: unsigned beta 2.1.0-beta.1; public download, not a stable release.
- Python 3: currently needed for local state locking and Hermes reply reading.
- Hermes: isolated profile connector tested for configuration preservation; authenticated provider/report acceptance testing remains.
- Other AI clients: MCP configuration export and tool discovery tested. The dashboard i key uses Hermes; other clients can research and save reviews through MCP. Client-specific acceptance testing remains.
- Windows, Linux and Intel macOS: no installer announced.

## Download and install

[Release page](https://github.com/sdb001/RHmachine-beta/releases/tag/v2.1.0-beta.1) — download these assets, not GitHub's generated “Source code” archives:

- [RHmachine-2.1.0-beta.1-macos-arm64.tar.gz](https://github.com/sdb001/RHmachine-beta/releases/download/v2.1.0-beta.1/RHmachine-2.1.0-beta.1-macos-arm64.tar.gz)
- [SHA256SUMS](https://github.com/sdb001/RHmachine-beta/releases/download/v2.1.0-beta.1/SHA256SUMS)
- [README.md](https://github.com/sdb001/RHmachine-beta/releases/download/v2.1.0-beta.1/README.md)

No repository access invitation or source checkout is needed. Put the archive and SHA256SUMS in the same directory, then:

```sh
shasum -a 256 -c SHA256SUMS
tar -xzf RHmachine-2.1.0-beta.1-macos-arm64.tar.gz
cd RHmachine
sh install.sh
~/.local/bin/rhmachine setup
```

Stop if checksum verification fails. The installer refuses to replace an existing command or installation. Confirm this is an unsigned beta; macOS may block it. Do not disable OS protections or remove quarantine protections. Report the exact blocking message instead.

Follow CONNECT.md in the extracted archive to connect Hermes or another MCP client. Start with `~/.local/bin/rhmachine terminal`. Use full command paths if ~/.local/bin is not on PATH. Read the included README for local data and removal instructions.

## API onboarding

After launch, use the [keyboard guide](KEYBOARD.md) for navigation, coin actions, Split Radar, Hermes chat and saved charts. Press `?` for in-app help.

Public Robinhood RPC, DexScreener and GeckoTerminal endpoints are built in; no shared private keys are distributed. Provider limits and coverage still apply. The setup wizard offers optional private HTTPS RPC, Nansen, HyperSync, X and Bubblemaps credentials. Tell the user to enter these locally in the hidden-input prompt, never in AI chat. Blank preserves an existing value.

Nansen snapshots are disabled in fresh configuration until a key is added. Adding one enables scheduled snapshots within the configured daily cap (50 credits by default). Research services can consume the customer's provider credits when used. Setup makes no validation requests; SAVED is not VALIDATED. Start with public feeds if credentials are unavailable.
