# Abandoned Ideas

This is a place for collecting abandoned software ideas.

Every developer has projects that did not continue: half-built tools, products that never found users, failed experiments, paused open-source plans, or side projects that quietly disappeared. They are not always worthless. Sometimes they simply missed the right timing, audience, context, or next maintainer.

**Abandoned Ideas** aims to preserve those ideas publicly, so developers can learn from each other, find inspiration, and discover new opportunities from unfinished work, failed attempts, and real-world blockers.

## Who This Is For

- Makers who have paused or abandoned a project
- Developers who want to document a failed attempt for others to learn from
- Indie hackers looking for new product or open-source ideas
- Builders who may want to take over an abandoned idea
- People interested in product validation, user acquisition, and early-stage launches

## What You Can Find Here

- Abandoned product ideas
- Short descriptions of what each idea was about
- The main reason why the author stopped
- Work that had already been done
- Tech stacks, links, and handoff notes
- Real problems other developers encountered

Not everything here is a success story. That is the point. Failure reasons are useful raw material. They can help others avoid repeated mistakes, rethink a market, or revive an idea in a new form.

## Browse Online

GitHub Pages:

```text
https://ipwangxin.github.io/AbandonedIdeas/
```

Traffic Alliance:

```text
https://ipwangxin.github.io/AbandonedIdeas/lianmeng.html
```

If your product was not blocked by development but by “promotion is hard, cannot find users,” the Traffic Alliance may help. It is a lightweight mutual-support network where early-stage products exchange links and share exposure to reach their first real users.

## How to Submit a New Idea

1. Open the repository Issues page:

   ```text
   https://github.com/ipwangxin/AbandonedIdeas/issues
   ```

2. Click **New issue**.
3. Choose the **提交遗缺点子** form.
4. Fill in:
   - Idea name
   - One-line description
   - Reason for abandonment
   - Tech stack
   - Work already done
   - Handoff notes
   - Contact or project links
5. After submission, the Issue will be labeled `abandoned`.
6. GitHub Actions will sync the data and display it on the homepage.

## Submission Tips

To make your idea easier to understand or take over:

- Do not only write “no time”; explain what had already been done
- Do not only write “failed promotion”; mention which channels you tried
- Attach code, demos, screenshots, or docs if available
- If you welcome others to continue the work, clarify permission and contact details
- If the idea should not be continued, explain why so others can avoid the same trap

## How It Works

This project intentionally keeps the infrastructure simple and mostly free:

- GitHub Issues for collecting ideas
- GitHub Issue Template for structured submissions
- GitHub Pages for the website
- GitHub Actions for syncing Issue data into `docs/data.json`

There is no backend server and no external database. The goal is to let the content flow first, then expand only when real usage demands it.

## Maintainer Notes

If you maintain this repository:

- Homepage: `docs/index.html`
- Traffic Alliance page: `docs/lianmeng.html`
- Issue form: `.github/ISSUE_TEMPLATE/abandon_idea.yml`
- Sync workflow: `.github/workflows/sync-issues.yml`
- Static data file: `docs/data.json`

For the first 10 submissions, manual operation is recommended: add useful labels, ask follow-up questions, collect success stories, and invite developers who stopped because of promotion problems to check out the Traffic Alliance.

## 中文

中文说明见 [README.md](README.md)。
