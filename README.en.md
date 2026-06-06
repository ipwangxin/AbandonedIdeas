# Abandoned Ideas

A lightweight website built with **GitHub Issues + GitHub Pages + GitHub Actions** for collecting, displaying, and reusing abandoned software ideas.

Many indie projects stop not because they are worthless, but because the maker ran out of time, failed to find users, hit technical blockers, or could not validate a business model. This repository turns those abandoned ideas into reusable public knowledge.

## Core Features

- Collect abandoned idea reports through a structured GitHub Issue form
- Read all Issues labeled `abandoned`
- Display idea name, reason, author, and date on GitHub Pages
- Generate a clickable tag cloud based on abandonment reasons
- Guide users who select “Promotion is hard, cannot find users” toward the Traffic Alliance
- Use GitHub Actions to generate `docs/data.json`, reducing frontend API rate-limit pressure

## Website

After GitHub Pages is enabled, the website should be available at:

```text
https://ipwangxin.github.io/AbandonedIdeas/
```

Traffic Alliance page:

```text
https://ipwangxin.github.io/AbandonedIdeas/lianmeng.html
```

## How to Submit an Abandoned Idea

1. Open the repository Issues page.
2. Click **New issue**.
3. Choose the **提交遗缺点子** issue form.
4. Fill in the idea name, one-line description, abandonment reason, tech stack, and work already done.
5. Submit the issue. It will be labeled `abandoned`.
6. GitHub Actions will regenerate `docs/data.json`, and the homepage will display the new entry.

## How to Enable GitHub Pages

1. Open repository `Settings`.
2. Go to `Pages`.
3. Under `Build and deployment`, choose:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/docs`
4. Save and wait for GitHub Pages to deploy.

## Data Sync

The workflow is located at:

```text
.github/workflows/sync-issues.yml
```

It runs when:

- An Issue is opened, edited, labeled, unlabeled, reopened, or closed
- The hourly schedule triggers
- You manually run the workflow

The generated data file is:

```text
docs/data.json
```

The homepage reads this static JSON file first. If it is unavailable, it falls back to the GitHub API.

## Traffic Alliance

If a submitter chooses **“Promotion is hard, cannot find users”** as the abandonment reason, the Issue form shows a Traffic Alliance prompt.

The Traffic Alliance is designed to:

- Help early-stage products find their first users
- Let members exchange lightweight links
- Build a shared traffic pool through simple manual operations

The page is located at:

```text
docs/lianmeng.html
```

You can manually update:

- The number of joined developers
- The application link
- The Google Form embed URL
- FAQ content
- Member rules

## Operations SOP

For the first 10 users, manual operations are recommended:

1. Check newly submitted `abandoned` Issues daily.
2. Add useful labels such as `promotion`, `handoff-ready`, or `technical-blocker`.
3. For users who selected the promotion-related reason, leave a comment inviting them to the Traffic Alliance.
4. Add successful handoff or revival stories to the homepage.
5. Check alliance member links once per week.

Homepage success stories are maintained in:

```text
docs/index.html
```

Search for `成功案例` to find the section.

## Future Improvements

- Add a dedicated Issue template for Traffic Alliance applications
- Add a `members.json` file to display alliance members
- Add dedicated pages for each abandonment reason
- Match ideas by tech stack, domain, and reason
- Track handoff status and successful revivals

## 中文

中文说明见 [README.md](README.md)。
