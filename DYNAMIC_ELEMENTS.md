# Dynamic Elements Guide

This document explains all the dynamic/live elements in your GitHub profile and how they work.

## 🔄 How Dynamic Elements Work

GitHub README.md files are **pure Markdown** - you cannot use React or JavaScript. However, you can embed **dynamic images** from external services that generate visuals on-the-fly:

```markdown
![Description](https://service.com/api?username=Aryan01101&params)
```

Every time someone views your profile, GitHub fetches the image URL, and the service generates a fresh image with your latest data.

---

## 📦 1. Repository Statistics Badges

**What it shows:**
- Total repositories count
- Total stars across all repos
- Total commits (all time)
- Years active on GitHub

**Service:** pufler.dev badges
**Updates:** Real-time (every page load)
**Setup required:** None - works automatically with your username

**Example:**
```markdown
![Total Repos](https://badges.pufler.dev/repos/Aryan01101?style=for-the-badge&color=00D9FF)
```

---

## 🎯 2. Pinned Repository Cards

**What it shows:**
- Repository name and description
- Primary language
- Star and fork counts
- Links directly to the repo

**Service:** github-readme-stats (Vercel)
**Updates:** Cached for ~4 hours, then refreshes
**Setup required:** None - just specify repo name

**Example:**
```markdown
[![YAAKE](https://github-readme-stats.vercel.app/api/pin/?username=Aryan01101&repo=YAAKE&theme=dark)](https://github.com/Aryan01101/YAAKE)
```

**To add more repos:** Add more card links with different `repo=` parameters

---

## 📈 3. Activity Graph

**What it shows:**
- Visual graph of your contribution activity over the last year
- Peaks and valleys show when you're most active
- Hover shows exact commit counts per day

**Service:** github-readme-activity-graph (Vercel)
**Updates:** Real-time (every page load)
**Setup required:** None

**Customization options:**
- `bg_color` - Background color
- `color` - Line/text color
- `line` - Graph line color
- `point` - Data point color
- `area=true` - Filled area under graph

---

## 🗓️ 4. Commit Pattern Heatmap

**What it shows:**
- Year-long heatmap of your contributions
- Darker colors = more commits that day
- Similar to GitHub's contribution graph but styled

**Service:** ghchart.rshah.org
**Updates:** Daily
**Setup required:** None

**Example:**
```markdown
![Commit Heatmap](https://ghchart.rshah.org/00D9FF/Aryan01101)
```

The color after the domain (`00D9FF`) is your accent color.

---

## ⏱️ 5. WakaTime Coding Stats

**What it shows:**
- Languages you've coded in this week
- Hours spent on each language
- Percentage breakdown

**Service:** github-readme-stats + WakaTime API
**Updates:** Every hour (based on WakaTime data)
**Setup required:** YES - see setup section below

### WakaTime Setup Instructions

1. **Install WakaTime Plugin**
   - VS Code: Install "WakaTime" extension
   - Other IDEs: https://wakatime.com/plugins

2. **Create WakaTime Account**
   - Sign up at https://wakatime.com/
   - Get your API key from https://wakatime.com/settings/account

3. **Configure Plugin**
   - Enter your API key when prompted
   - WakaTime will now track your coding time automatically

4. **Make Stats Public**
   - Go to https://wakatime.com/settings/profile
   - Scroll to "Public Profile"
   - Enable "Display coding activity publicly"
   - Enable "Display languages publicly"

5. **Get Your WakaTime Username**
   - Your username is in the URL: `wakatime.com/@YourUsername`
   - Update the README if it's different from "Aryan01101"

**If WakaTime shows errors:**
- Make sure your profile is public
- Verify you've coded at least 1 hour in the past week
- Check that your username is correct

---

## 🗂️ 6. Profile Summary Cards

**What it shows:**
- **Profile Details:** Complete contribution timeline graph
- **Repos per Language:** How many repos use each language
- **Most Commit Language:** Which language you commit to most
- **Stats:** Total stars, commits, PRs, issues
- **Productive Time:** What time of day you code most (UTC)

**Service:** github-profile-summary-cards (Vercel)
**Updates:** Cached for ~4 hours
**Setup required:** None

**Cards available:**
- `profile-details` - Timeline of contributions
- `repos-per-language` - Pie chart of repos
- `most-commit-language` - Bar chart of commits
- `stats` - Key statistics
- `productive-time` - Time-of-day heatmap

---

## 📊 7. GitHub Analytics (Existing)

**GitHub Stats Card:**
- Total stars, commits, PRs, issues
- Contribution streak
- Ranking (S, A, B, etc.)

**Top Languages Card:**
- Languages used across all repos
- Percentage breakdown

**Streak Stats:**
- Current streak (days)
- Longest streak
- Total contributions

**Contribution Snake:**
- Animated snake eating your contributions
- Generated daily via GitHub Actions

---

## 🎨 Customization Guide

### Color Theme
All elements use your cyan accent color: `#00D9FF`

To change colors, update the hex codes in:
- `color=00D9FF` - Accent color
- `bg_color=0D1117` - Background (dark)
- `text_color=FFFFFF` - Text (white)
- `title_color=00D9FF` - Titles (cyan)

### Themes
Most services support themes:
- `theme=dark` or `theme=github_dark`
- `theme=radical` (pink/purple)
- `theme=tokyonight` (blue)
- `theme=dracula` (purple)

### Adding More Repos to Pinned Section

```markdown
[![Repo Name](https://github-readme-stats.vercel.app/api/pin/?username=Aryan01101&repo=REPO-NAME&theme=dark&bg_color=0D1117&title_color=00D9FF&text_color=FFFFFF&icon_color=00D9FF&border_color=00D9FF&border_radius=10)](https://github.com/Aryan01101/REPO-NAME)
```

Replace `REPO-NAME` with your repository name.

---

## 🚀 Services Used

1. **pufler.dev** - Badge counters
   - Docs: https://github.com/DenverCoder1/readme-badges

2. **github-readme-stats** (Vercel)
   - Docs: https://github.com/anuraghazra/github-readme-stats
   - Pinned repos, language stats, user stats

3. **github-readme-activity-graph**
   - Docs: https://github.com/Ashutosh00710/github-readme-activity-graph
   - Activity timeline graph

4. **ghchart.rshah.org**
   - Docs: https://github.com/2016rshah/githubchart-api
   - Contribution heatmap

5. **github-profile-summary-cards** (Vercel)
   - Docs: https://github.com/vn7n24fzkq/github-profile-summary-cards
   - Detailed profile analytics

6. **github-readme-streak-stats**
   - Docs: https://github.com/DenverCoder1/github-readme-streak-stats
   - Contribution streaks

7. **Platane/snk** (GitHub Action)
   - Docs: https://github.com/Platane/snk
   - Contribution snake animation

---

## 🔧 Troubleshooting

**Stats not showing?**
- Wait a few minutes - some services cache data
- Check if your repos are public
- Verify your username is correct

**WakaTime blank/error?**
- Ensure profile is public
- Code for at least 1 hour
- Wait for data to sync (up to 1 hour)

**Cards showing 404?**
- Repository might be private
- Repository name might be incorrect
- Service might be temporarily down

**Colors not matching?**
- Check hex color codes (no # symbol in URLs)
- Ensure `&` separates parameters
- Use URL encoding if needed

---

## 📝 Additional Elements You Can Add

**GitHub Trophies:**
```markdown
![Trophies](https://github-profile-trophy.vercel.app/?username=Aryan01101&theme=darkhub&column=7&color=00D9FF)
```

**Visitor Map:**
```markdown
![Visitor Map](https://profile-counter.glitch.me/Aryan01101/count.svg)
```

**Latest Blog Posts (if you have a blog):**
Requires GitHub Action - fetches from RSS feed

**Spotify Currently Playing:**
Requires Vercel deployment and Spotify API

---

## 🎯 Best Practices

1. **Don't overload** - Too many dynamic elements slow page loads
2. **Test regularly** - Services can go down or change APIs
3. **Keep it relevant** - Only show stats that tell your story
4. **Mobile friendly** - Some complex visualizations don't work well on mobile
5. **Cache awareness** - Most services cache for 2-24 hours

---

## 📊 Your Current Dynamic Elements

✅ Profile view counter
✅ Repository stats (repos, stars, commits, years)
✅ Pinned repository cards (YAAKE, Over-save)
✅ Activity graph (contribution timeline)
✅ Commit heatmap (year-long pattern)
✅ WakaTime stats (coding time by language)
✅ Profile summary cards (6 different metrics)
✅ GitHub stats (stars, commits, PRs)
✅ Top languages breakdown
✅ Streak counter
✅ Contribution snake animation

**Total: 11 unique dynamic visualizations** showing different aspects of your GitHub activity!
