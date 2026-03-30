# Incident Response KQL Query Collection

Welcome to the **Incident Response KQL Query Collection** — a community-driven list of Kusto Query Language (KQL) queries for security analysis and incident response. This project is designed to help students learn both **KQL** and **GitHub collaboration** at the same time.

---

## 📋 About This Repository

This repository contains a growing list of KQL queries contributed by students just like you. The queries are stored in [KQL-queries.md](KQL-queries.md) and cover common incident response and threat-hunting scenarios using platforms such as Microsoft Sentinel and Microsoft Defender.

Your job is to **add your own KQL query** to the list. This is a hands-on way to practise using GitHub and to share useful knowledge with your classmates.

---

## 🚀 How to Contribute — Step by Step

Don't worry if you've never used GitHub before. Follow these steps carefully and you'll have your first contribution submitted in no time!

### Step 1 — Create a GitHub Account

If you don't already have a GitHub account:

1. Go to [https://github.com](https://github.com)
2. Click **Sign up** in the top-right corner
3. Follow the prompts to create a free account

### Step 2 — Fork This Repository

"Forking" creates your own personal copy of this repository so you can make changes without affecting the original.

1. Make sure you are logged in to GitHub
2. Click the **Fork** button near the top-right of this page
3. GitHub will create a copy of the repository under your own account (e.g. `your-username/c4-inc-response-public-repo`)

### Step 3 — Edit the KQL Queries File

1. In **your forked repository**, navigate to [KQL-queries.md](KQL-queries.md)
2. Click the **pencil icon** (✏️) on the right side of the page to edit the file
3. Scroll to the bottom of the list of queries
4. Add your own KQL query using the template at the bottom of the file:

````markdown
### <number>. <Short description of what the query does>
```kql
<your KQL query here>
```
````

5. Give your query a clear, descriptive title
6. Scroll down and click **Commit changes** when you're done

### Step 4 — Open a Pull Request

A pull request (PR) is how you propose your changes be added to the original repository.

1. Go back to the main page of **your forked repository**
2. You should see a banner saying **"This branch is 1 commit ahead"** — click **Contribute** → **Open pull request**
3. Give your pull request a clear title (e.g. `Add query: detect suspicious PowerShell`)
4. In the description, briefly explain what your query does and when it would be useful
5. Click **Create pull request**

That's it! Your contribution will be reviewed and merged into the shared list. 🎉

---

## 💡 Tips for a Good Contribution

- **Test your query first** if you have access to a Microsoft Sentinel or Defender environment
- **Comment your query** — add a brief note explaining what the query detects and why it is useful
- **Check for duplicates** — have a look through the existing queries before adding a new one
- **One query per pull request** — this makes it easier to review

---

## 📖 Learning Resources

New to KQL? These free resources will help you get started:

- [Microsoft KQL documentation](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/)
- [KQL Quick Reference](https://learn.microsoft.com/en-us/azure/data-explorer/kql-quick-reference)
- [GitHub's own guide to contributing to projects](https://docs.github.com/en/get-started/exploring-projects-on-github/contributing-to-a-project)

---

## 🤝 Code of Conduct

Be kind and respectful to your fellow students. All contributions are welcome regardless of experience level. If you are unsure about something, open a pull request anyway — the review process is there to help you learn.

---

*This repository is maintained as part of a student learning activity.*
