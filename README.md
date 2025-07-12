# 🔧 action-repo

This repository is used to simulate GitHub Actions such as `push`, `pull request`, and `merge` events. These events trigger a webhook that sends data to the `webhook-repo` server, which processes and stores the event information in a MongoDB database.

---

## 🎯 Purpose

The `action-repo` is part of a two-repo system for a developer assessment. It demonstrates how GitHub events can be captured and consumed by an external backend through webhooks.

---

## 🚀 How It Works

1. GitHub Actions like:
   - `Push`
   - `Pull Request`
   - `Merge` (Bonus)
   
   will trigger a webhook attached to this repository.

2. The webhook sends payload data to the **webhook endpoint** implemented in a separate Flask-based project (`webhook-repo`).

3. The Flask server parses the webhook, formats the data, and stores it into MongoDB.

4. A UI polls MongoDB every 15 seconds to fetch and display the latest updates in a clean and minimal interface.

---

## 🔗 Related Repository

➡️ [webhook-repo](https://github.com/YOUR_USERNAME/webhook-repo)

---

## 🛠️ Setup Instructions

To get started with triggering webhooks from this repository:

1. **Clone the Repo**
   ```bash
   git clone https://github.com/YOUR_USERNAME/action-repo.git
   cd action-repo