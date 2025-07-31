# 🔐 SafeVault – Governance & Automation for Safe{Wallet}

SafeVault is a full-stack Safe App that enhances the governance and coordination of Safe{Wallet} users through GitHub-native workflows, automation, and real-time tooling.
	•	🧠 Built on Safe SDK + AppKit (Reown)
	•	⚙️ GitHub Actions-powered Safe proposal creation
	•	🧾 PWA frontend with multi-network support
	•	🔔 Telegram preview bots for signer updates
	•	🛂 Reown login + Safe connection
	•	🌐 Hosted on GitHub Pages / Safe Apps iframe

⸻

📦 Features
	•	✅ GitHub → Safe Transaction: Issue comment → Proposal command
	•	✅ Reown wallet login & Safe signer mapping
	•	✅ Safe App SDK integration for direct multisig execution
	•	✅ Owner threshold management + status tracking
	•	✅ Telegram + Email notification support (via bot/webhooks)
	•	✅ Supports: Ethereum, Arbitrum, Optimism, Polygon, Gnosis, Base, zkSync, Sepolia

⸻

🚀 Live Demo

🧪 SafeVault App

🧠 Reown AppKit

⸻

🧩 Safe App Configuration

Required to list your app on Safe{Wallet} and run it inside the Safe App browser.
{
  "name": "SafeVault",
  "description": "Governance and automation platform for Safe{Wallet}",
  "iconUrl": "https://your-safevault-url.com/icon.png",
  "url": "https://your-safevault-url.com",
  "chainIds": [1, 10, 137, 42161, 100, 8453, 1101],
  "provider": "Reown",
  "accessControl": {
    "type": "no_restriction"
  }
}

⚙️ Environment Configuration

Create a .env.local file in the root:
NEXT_PUBLIC_SAFE_ADDRESS=<default 0xAfD5f60aA8eb4F488eAA0eF98c1C5B0645D9A0A0>
NEXT_PUBLIC_REOWN_PROJECT_ID=< 0e86b980-2298-4978-8dd5-0b9e7af95016>
NEXT_PUBLIC_TELEGRAM_BOT_URL= https://t.me/mysafenotifier_bot
NEXT_PUBLIC_SUPPORTED_CHAINS=1,10,137,42161,100
NEXT_PUBLIC_SITE_URL=https://your-safevault-url.com


🛠️ Development Setup
git clone https://github.com/your-org/SafeVault.git
cd SafeVault
npm install
npm run dev
Local app will run at: http://localhost:3000


🧪 GitHub Actions Integration

Use proposal commands in issues to trigger Safe transactions.

	•	GitHub Workflow: .github/workflows/trigger-safe-proposal.yml
	•	Available Commands:
	•	/transfer
	•	/change-threshold
	•	/add-owner
	•	/remove-owner

See /backend/commands/ for full logic.

⸻

🛡️ Safe SDK & AppKit
	•	Safe SDK Docs
	•	@safe-global/safe-apps-react-sdk
	•	Reown AppKit

⸻

🚢 Deployment

🔁 GitHub Pages (Static Export)
npm run export
Then push the /out directory to the gh-pages branch. You can automate this with:
# .github/workflows/deploy.yml
uses: peaceiris/actions-gh-pages@v4


🛂 Permissions & Security
	•	Uses official Safe contracts only
	•	No private key management
	•	Reown handles auth and wallet mapping
	•	GitHub Actions scoped to repo-level automation

⸻

🧾 License

MIT License © 2025 TheGoodEth

⸻

📬 Contact / Support
	•	🔗 Telegram Support: @SafeVaultBot
	•	✉️ Email: support@safevault.xyz
