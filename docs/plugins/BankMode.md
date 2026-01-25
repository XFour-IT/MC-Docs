---
icon: lucide/landmark
---
# BankMode

BankMode is a Minecraft server plugin that adds banking, loans, and interest with support for Vault or an internal economy.

---

## 📆 Overview

- Deposit and withdraw money
- Earn interest over time
- Request and repay loans
- Choose between Vault or internal economy
- Real-time tracking and auto-collection for loans

---

## 📦 Installation

**Requirements:**

- Paper/Spigot 1.20.1+
- Java 17+
- (Optional) Vault + EssentialsX

**Steps:**

1. Drop `bankmode-bukkit-1.0.0.jar` into `/plugins`
2. Restart your server
3. Plugin auto-detects economy system
4. Use `/bnk config` to customize settings

---

## ⚙️ Configuration

**Economy Modes:**

- `vault` – uses Vault economy
- `internal` – BankMode's internal system
- `auto` – default, auto-detects

**Default Values:**

- Interest Rate: 2.0%
- Interest Period: 1 hour
- Loan Interest: 5.0%
- Loan Term: 30 days
- Auto Default: 7 days
- Max Loan: $10,000
- Min Loan: $100
- Max Loans: 3 per player

---

## 🔢 Basic Commands

```bash
/bnk deposit <amount>       # Deposit money
/bnk withdraw <amount>      # Withdraw money
/bnk balance                # Check your balance
/bnk history                # View transactions
/bnk status [live]          # Interest countdown

```

---

## 💳 Loan Commands

```bash
/bnk loan request <amount> [reason]   # Request a loan
/bnk loan pay <loan_id> <amount>      # Make payment
/bnk loan list                        # View active loans
/bnk loan info <loan_id>             # View loan details

```

---

## ⚙️ Admin Commands

```bash
/bnk config interest <rate>            # Set interest rate
/bnk config period <seconds>           # Set interest payout period
/bnk config economy <mode>             # Set economy mode
/bnk config toggle                     # Enable/disable interest system

/bnk config loan interest <rate>       # Set loan interest rate
/bnk config loan term <seconds>        # Set loan term duration
/bnk config loan maxamount <amount>    # Max loan allowed
/bnk config loan minamount <amount>    # Min loan allowed
/bnk config loan maxloans <count>      # Max active loans per player
/bnk config loan autodefault <seconds> # Auto-default timeout
/bnk config loan toggle                # Enable/disable loan system
/bnk config loan info                  # View loan settings

/bnk internal set <player> <amount>    # Set balance (internal only)
/bnk internal add <player> <amount>    # Add balance (internal only)
/bnk internal remove <player> <amount> # Remove balance (internal only)
/bnk internal balance <player>         # Check player's balance
/bnk internal list                     # List all balances

/bnk info                               # View plugin settings
/bnk stats                              # View economy stats
/bnk test                               # Trigger overdue loan check

/bnk help                               # Help menu
/bnk help <category>                    # Help by category

```

---

## 🌐 Features

- Auto interest payouts
- Multi-loan support
- Automatic overdue collection
- Internal and Vault support
- Live countdowns

---

## 🔒 Permissions

```yaml
# Player
bankmode.use
bankmode.deposit
bankmode.withdraw
bankmode.loan
bankmode.status
bankmode.help

# Admin
bankmode.admin
bankmode.internal

```

---

## 🔧 Troubleshooting

**Interest Not Paying?**

- Check `/bnk config toggle`
- Ensure rate and period are set

**Loan Not Working?**

- Loan system enabled?
- Too many loans or overdue?

**Command Not Found?**

- Plugin loaded?
- Check permissions

---

## 📅 Changelog

**v1.0.0**

- Initial release with banking, loans, interest, and dual economy

---

## ❗ Support

1. Use `/bnk help` in-game
2. Check this doc
3. Use `/bnk test` for loan checks

---
