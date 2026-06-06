# Abandoned Ideas

This is a place for collecting software ideas that were abandoned, paused, stuck after launch, or waiting for someone else to take over.

Building has become easier than ever. With vibe coding, a random late-night idea can quickly turn into a product conversation with AI. The more you talk, the more real it feels: requirements appear, pages take shape, APIs get wired, and at 2 AM you start feeling like this might be the one.

Then the real world returns. Nobody visits. Promotion is harder than expected. Technical debt grows. Interest shifts. A competitor appears. Work gets busy. Or the excitement simply fades.

That is normal.

Every developer has projects that did not continue: launched products with no growth, half-built tools, apps that never found users, failed experiments, paused open-source plans, or side projects that quietly disappeared. They are not always worthless. Sometimes they simply missed the right timing, audience, context, or next maintainer.

**Abandoned Ideas** aims to preserve those ideas publicly, so developers can learn from each other, find inspiration, and discover new opportunities from launched products, unfinished work, failed attempts, and real-world blockers.

## Who This Is For

- Makers who launched something but could not find users or growth
- Makers who have paused or abandoned a project
- Developers who want to document a failed attempt for others to learn from
- Indie hackers looking for new product or open-source ideas
- Builders who may want to take over an abandoned idea
- People interested in product validation, user acquisition, and early-stage launches

## What You Can Find Here

- Abandoned product ideas
- Launched products that are stuck with growth or promotion
- Short descriptions of what each idea was about
- The main blocker the author is facing
- Work that had already been done
- Tech stacks, live URLs, open-source URLs, and handoff notes
- Real problems other developers encountered

Not everything here is a success story. That is the point. The current state of a project is useful raw material. It can help others avoid repeated mistakes, rethink a market, or revive an idea in a new form.

## Browse Online

GitHub Pages: [Open website](https://ipwangxin.github.io/AbandonedIdeas/)

```text
https://ipwangxin.github.io/AbandonedIdeas/
```

Traffic Alliance: [Open page](https://ipwangxin.github.io/AbandonedIdeas/lianmeng.html)

```text
https://ipwangxin.github.io/AbandonedIdeas/lianmeng.html
```

If your product was not blocked by development but by “promotion is hard, cannot find users,” the Traffic Alliance may help. It is a lightweight mutual-support network where early-stage products exchange links and share exposure to reach their first real users.

## What You Can Submit

You do not need to wait until a project is completely abandoned. These are all welcome:

- Launched, but no users or growth
- Launched, but no longer maintained
- Not launched, but there is a prototype, demo, or screenshot
- Not launched, but there are notes, requirements, or AI chat summaries
- Open-source, but lacking contributors, maintainers, or a new owner
- Fully abandoned, but the process and lessons are worth sharing

## How to Submit a New Idea

1. Open the repository [Issues page](https://github.com/ipwangxin/AbandonedIdeas/issues).

   ```text
   https://github.com/ipwangxin/AbandonedIdeas/issues
   ```

2. Click [New issue](https://github.com/ipwangxin/AbandonedIdeas/issues/new/choose).

   ```text
   https://github.com/ipwangxin/AbandonedIdeas/issues/new/choose
   ```

3. Choose the **提交遗缺点子** form.
4. Fill in:
   - Idea name
   - One-line description
   - Current status
   - Live URL, optional
   - Open-source URL, optional
   - Blocker or reason for abandonment
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
- If the project is live, add the product, demo, landing page, or documentation URL
- If the project is open-source, add the GitHub, GitLab, Gitee, or other repository URL
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
