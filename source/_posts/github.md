---
title: "GitHub"
date: 2014-12-11 17:34:16
categories:
  - app
tags:
  - github
  - git
  - notes
toc: true
---

[Microsoft + GitHub = Empowering Developers - The Official Microsoft Blog](https://blogs.microsoft.com/blog/2018/06/04/microsoft-github-empowering-developers/)
[A bright future for GitHub | The GitHub Blog](https://blog.github.com/2018-06-04-github-microsoft/)
[GitHub Documentation](https://docs.github.com/en)
[GitHub: A cheat sheet - TechRepublic](https://www.techrepublic.com/article/github-the-smart-persons-guide/#ftag=CAD-00-10aag7f)
[tiimgreen/github-cheat-sheet: A list of cool features of Git and GitHub.](https://github.com/tiimgreen/github-cheat-sheet)
[Introduction to GitHub in Visual Studio Code - Learn | Microsoft Docs](https://docs.microsoft.com/en-us/learn/modules/introduction-to-github-visual-studio-code/)
[Introducing code owners - The GitHub Blog](https://github.blog/2017-07-06-introducing-code-owners/)

[10 Fun Things You Can Do With GitHub.dev 😎 - DEV Community](https://dev.to/lostintangent/10-awesome-things-you-can-do-with-github-dev-5fm7)

[Bountysource](https://www.bountysource.com/)

[CLAHub](https://www.clahub.com/)
[Useful Forks](https://useful-forks.github.io/)
[npmhub.org](http://npmhub.org/)

[Git Started with GitHub | Udemy](https://www.udemy.com/git-started-with-github/)
[Sane GitHub Labels – Dave Lunny – Medium](https://medium.com/@dave_lunny/sane-github-labels-c5d2e6004b63)

[GitHub Tools](https://github.com/github-tools)
[GitHub Cards](http://lab.lepture.com/github-cards/)
[GitHub Card - gh-card](https://gh-card.dev/)
[GitHub Visualizer](http://ghv.artzub.com/)
[Octobox](https://octobox.io/) Untangle your GitHub Notifications
[sourcerer-io/sourcerer-app: 🤖 Sourcerer app makes a visual profile from your GitHub and git repositories.](https://github.com/sourcerer-io/sourcerer-app)
[Issue Stats](http://issuestats.com/)
[ben174/git-draw: Allows you to draw in your github heatmap](https://github.com/ben174/git-draw)

[nlf/node-github-hook](https://github.com/nlf/node-github-hook)
[nlf/gitenforcer](https://github.com/nlf/gitenforcer)
[nlf/node-ghtoken](https://github.com/nlf/node-ghtoken)

[Johennes/gitig: Client-side git mirror replicator (Mirror of https://nosuchdomain.mooo.com/git/doc/gitig)](https://github.com/Johennes/gitig)

[The Unofficial GitHub Watch & Fork Buttons](http://ghbtns.com/)
[Fork me on GitHub CSS Ribbon](https://simonwhitaker.github.io/github-fork-ribbon-css/)
[Pure CSS responsive "Fork me on GitHub" ribbon](http://codepo8.github.io/css-fork-on-github-ribbon/)
[GitHub Ribbon Using CSS Transforms | Unindented](https://unindented.org/articles/github-ribbon-using-css-transforms/)

## Auth

[Behind GitHub's new authentication token formats | The GitHub Blog](https://github.blog/2021-04-05-behind-githubs-new-authentication-token-formats/)

## Gist

[Lepton - A Lean GitHub Gist Client](http://hackjutsu.com/Lepton/)

## GitHub CLI

[GitHub CLI | Take GitHub to the command line](https://cli.github.com/)
[cli/cli: GitHub’s official command line tool](https://github.com/cli/cli)

[Scripting with GitHub CLI - The GitHub Blog](https://github.blog/2021-03-11-scripting-with-github-cli/)
[Work with GitHub Actions in your terminal with GitHub CLI - The GitHub Blog](https://github.blog/2021-04-15-work-with-github-actions-in-your-terminal-with-github-cli/)

[donnemartin/gitsome: A supercharged Git/GitHub command line interface (CLI). An official integration for GitHub and GitHub Enterprise: https://github.com/works-with/category/desktop-tools](https://github.com/donnemartin/gitsome)

## GitHub Pages

[GitHub Pages | Websites for you and your projects, hosted directly from your GitHub repository. Just edit, push, and your changes are live.](https://pages.github.com/)
[GitHub Help](https://help.github.com/categories/20/articles)

[A Guide To Using Github Pages · Thinkful Programming Guides](https://www.thinkful.com/learn/a-guide-to-using-github-pages/)

[React Router with GitHub Pages - DEV Community 👩‍💻👨‍💻](https://dev.to/caffiendkitten/react-router-with-github-pages-en3)

You can also place static web sites on `gh-pages` branch and it can be accessed at `<user>.github.io/<repo>`. If the repo is `<user>.github.io`, the URL is `<user>.github.io`.

GitHub includes Jekyll generator by default.
[GitHub Pages](http://jekyllrb.com/docs/github-pages/)
[Instantly Beautiful Project Pages · GitHub](https://github.com/blog/1081-instantly-beautiful-project-pages)

But you can put any static generated site on any branch, enter project settings and select GitHub Pages to serve that branch.

### Custom Domain

1. Put the domain name in a file `CNAME` in the root of your `gh-pages` branch.
2. Setup A records pointing to GitHub in your domain registrar
   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153

Or do it in "Custom domain" in repo settings.

[dns - gh-pages not allowing multiple subdomains - Webmasters Stack Exchange](https://webmasters.stackexchange.com/questions/104291/gh-pages-not-allowing-multiple-subdomains)
[Setting up an apex domain - User Documentation](https://help.github.com/articles/setting-up-an-apex-domain/#configuring-a-records-with-your-dns-provider)

[Using a custom domain with GitHub Pages - User Documentation](https://help.github.com/articles/using-a-custom-domain-with-github-pages/)
[Troubleshooting custom domains - User Documentation](https://help.github.com/articles/troubleshooting-custom-domains/)

[Using GitHub Pages To Host Your Website - Treehouse Blog](http://blog.teamtreehouse.com/using-github-pages-to-host-your-website)
[rafrex/spa-github-pages: Host single page apps with GitHub Pages](https://github.com/rafrex/spa-github-pages)

### `gh-pages`

[tschaub/gh-pages: General purpose task for publishing files to a gh-pages branch on GitHub](https://github.com/tschaub/gh-pages)

```json
"scripts": {
  "deploy": "gh-pages -d dist"
}
```

[Tips](https://github.com/tschaub/gh-pages#tips)
If error "fatal: A branch named 'gh-pages' already exists." is encountered, clear `gh-pages`'s cache.

```sh
rm -rf node_modules/gh-pages/.cache
```

## GitHub Actions

[GitHub Actions](https://github.com/actions?type=source)
[actions/virtual-environments: GitHub Actions virtual environments](https://github.com/actions/virtual-environments)

[Automatic Deployment With Github Actions - YouTube](https://www.youtube.com/watch?v=X3F3El_yvFg)

[Building Your First GitHub Action | Azure DevOps Blog](https://devblogs.microsoft.com/devops/building-your-first-github-action/)
[GitHub Actions Documentation - GitHub Docs](https://docs.github.com/en/free-pro-team@latest/actions)
[Workflow syntax for GitHub Actions - GitHub Docs](https://docs.github.com/en/free-pro-team@latest/actions/reference/workflow-syntax-for-github-actions)
[Features • GitHub Actions](https://github.com/features/actions/)
[sdras/awesome-actions: A curated list of awesome actions to use on GitHub](https://github.com/sdras/awesome-actions)
[GitHub Actions for Rust · svartalf](https://svartalf.info/posts/2019-09-16-github-actions-for-rust/)
[actions-rs](https://github.com/actions-rs?type=source)

[starter-workflows/dotnet-core.yml at master · actions/starter-workflows · GitHub](https://github.com/actions/starter-workflows/blob/master/ci/dotnet-core.yml)

[How to build and push Docker image with GitHub actions? - Event-Driven.io](https://event-driven.io/en/how_to_buid_and_push_docker_image_with_github_actions/)

[Ramblings from Jessie: The Life of a GitHub Action](https://blog.jessfraz.com/post/the-life-of-a-github-action/)
[Python in GitHub Actions · Homepage of Hynek Schlawack](https://hynek.me/articles/python-github-actions/)
[How to write good quality Python code with GitHub Actions](https://medium.com/@wkrzywiec/how-to-write-good-quality-python-code-with-github-actions-2f635a2ab09a)
[How to Publish a no-code website in 10 minutes](https://www.freecodecamp.org/news/publish-a-no-code-website-in-10-minutes/amp/) Hugo with GitHub Action
[Getting Started with GitHub Actions for .NET Developers - Steve Gordon - Code with Steve](https://www.stevejgordon.co.uk/getting-started-with-github-actions-for-dotnet-developers)

Put YAML in `.github/workflows/`:  
[verona/update-snmalloc.yaml at master · microsoft/verona](https://github.com/microsoft/verona/blob/master/.github/workflows/update-snmalloc.yaml)

[The Changelog #331: GitHub Actions is the next big thing with Kyle Daigle, Director of Ecosystem Engineering at GitHub | News and podcasts for developers | Changelog](https://changelog.com/podcast/331)

## Package Registry

[GitHub Package Registry: Your packages, at home with their code](https://github.com/features/package-registry)
[Introducing GitHub Package Registry - The GitHub Blog](https://github.blog/2019-05-10-introducing-github-package-registry/)
[GitHub launches Package Registry to easily generate packages from your code | ZDNet](https://www.zdnet.com/article/github-launches-package-registry-to-easily-generate-packages-from-your-code/#ftag=CAD-00-10aag7e)

## Extensions

[sindresorhus/refined-github: Chrome extension that simplifies the GitHub interface and adds useful features](https://github.com/sindresorhus/refined-github)
[rubyerme/chrome-github-mate: Chrome extension to make single file download effortless and with more features](https://github.com/rubyerme/chrome-github-mate)
[octo-linker/chrome-extension: Octo-Linker Chrome extension](https://github.com/octo-linker/chrome-extension/)
[npm-hub - Chrome Web Store](https://chrome.google.com/webstore/detail/npm-hub/kbbbjimdjbjclaebffknlabpogocablj) add npm dependencies to GitHub repo
[buunguyen/octotree: Code tree for GitHub and GitLab](https://github.com/buunguyen/octotree)

[thecodejunkie/github.expandinizr: Chrome extension that improves the GitHub experience](https://github.com/thecodejunkie/github.expandinizr)
[NavTree for Github - Chrome Web Store](https://chrome.google.com/webstore/detail/navtree-for-github/hehmfcekejdeohjjckmalfemepbbafbe?hl=en-US)
[ZenHub - Project Management for Agile Teams in GitHub](https://www.zenhub.io/)

## Links

```
# browse tree in browser
https://github.com/<user>/<repo>/tree/<branch>/<folder>
# e.g.:
https://github.com/chancejs/chancejs/tree/master/dist

# use `y` to convert branch to commit
https://help.github.com/articles/getting-permanent-links-to-files/#press-y-to-permalink-to-a-file-in-a-specific-commit

# view file in browser
https://github.com/<user>/<repo>/blob/<branch>/<path>
# e.g.:
https://github.com/chancejs/chancejs/blob/master/dist/chance.min.js

# raw file (for download)
https://github.com/<user>/<repo>/raw/<branch>/<path>
# e.g.:
https://github.com/chancejs/chancejs/raw/master/dist/chance.min.js

# to have proper MIME type for viewing in browser

# download latest release
curl -L "https://github.com/jenkins-x/jx/releases/download/$(curl --silent "https://github.com/jenkins-x/jx/releases/latest" | sed 's#.*tag/\(.*\)\".*#\1#')/jx-linux-amd64.tar.gz" | tar xzv "jx"
```

### Serve files

[raw.githack.com](https://raw.githack.com/)
[GitCDN - A powerful CDN for Github files](https://gitcdn.xyz/)
[schme16/gitcdn.xyz: Serve your content straight from GitHub, with the correct Content-Type, consistant url and a powerful CDN](https://github.com/schme16/gitcdn.xyz)
[RawGit](http://rawgit.com/) EOLed

```sh
# - replace `githubusercontent.com` with `githack.com` in raw file link

https://raw.githubusercontent.com/servo/servo/master/dependencyci.yml
# becomes
# https://raw.githack.com/servo/servo/master/dependencyci.yml
# https://gitcdn.xyz/repo/servo/servo/master/dependencyci.yml
```

[GitHub & BitBucket HTML Preview](http://htmlpreview.github.io/)

```sh
http://htmlpreview.github.io/?https://github.com/baconjs/bacon.js/blob/master/examples/examples.html
```

## SSH keys

> see `ssh.md`

[Connecting to GitHub with SSH - User Documentation](https://help.github.com/articles/connecting-to-github-with-ssh/)
[Generating SSH keys - User Documentation](https://help.github.com/articles/generating-ssh-keys/)
[Error: Permission denied (publickey) - User Documentation](https://help.github.com/articles/error-permission-denied-publickey/)

You can get your keys via `https://github.com/username.keys`.

## Multiple accounts

If you have multiple account on GitHub, you can use HTTPS to specify the user (but you have to enter credentials every-time):

```sh
git remote set-url origin https://USERNAME@github.com/USERNAME/PROJECTNAME.git
```

You must use `git` user (not USERNAME) for git protocol; you can then use multiple SSH keys with SSH host alias to distinguish between different accounts.

> see `git-notes.md#specify-ssh-key-to-use`

`~/.git/config`:

```
# Personal GitHub
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa
  IdentitiesOnly yes

# company GitHub
Host github-COMPANY
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_COMPANY
  IdentitiesOnly yes
```

```
> ssh -T git@github.com
Hi <personal username>! You've successfully authenticated...
> ssh -T git@github-COMPANY
Hi <company username>! You've successfully authenticated...
```

```sh
# replace @github.com with host alias (@github-COMPANY)
> git remote set-url origin git@github-COMPANY:Company/testing.git
# or manually edit `.git/config`
```

[Quick Tip: How to Work with GitHub and Multiple Accounts - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/how-to-work-with-github-and-multiple-accounts--net-22574)
[Github for work and play (multiple accounts) | ricardian ambivalence](http://ricardianambivalence.com/2013/09/22/github-for-work-and-play-multiple-accounts/)
[Switch between user identities in one Git on one computer - Stack Overflow](http://stackoverflow.com/questions/9347458/switch-between-user-identities-in-one-git-on-one-computer)
[git - Multiple github accounts on the same computer? - Stack Overflow](http://stackoverflow.com/questions/3860112/multiple-github-accounts-on-the-same-computer)

## Organization

[repo-utils](https://github.com/repo-utils/)

[repo-utils/badgeboard: template for \*.github.io's](https://github.com/repo-utils/badgeboard)
[pillarjs](https://pillarjs.github.io/) (example)

[repo-utils/org-labels: A tool to help manage organization-wide GitHub issue labels.](https://github.com/repo-utils/org-labels)
[Marsup/hil - JavaScript](https://github.com/Marsup/hil)
[jshttp/style-guide - JavaScript](https://github.com/jshttp/style-guide)

## Handling PR

[Merging a pull request - User Documentation](https://help.github.com/articles/merging-a-pull-request/)
[Checking out pull requests locally - User Documentation](https://help.github.com/articles/checking-out-pull-requests-locally/)

[A Git Workflow Walkthrough - Merging Pull Requests - git, Tools & Workflows, Tutorial, Web Applications - Bocoup](https://bocoup.com/weblog/git-workflow-walkthrough-merging-pull-requests)
[Best Way To Merge A (GitHub) Pull Request](http://blog.differential.com/best-way-to-merge-a-github-pull-request/)

[Configuring a remote for a fork - User Documentation](https://help.github.com/articles/configuring-a-remote-for-a-fork/)
[Syncing a fork - User Documentation](https://help.github.com/articles/syncing-a-fork/)

Using [hub](https://hub.github.com/):

```sh
hub checkout <PR url>
git rebase -i origin/master
git checkout master
git merge --no-ff <username-branch>
git push

# OR

hub fetch <username>
git merge <username/branch>
git rebase -i origin/master
git push

# from GitHub
git checkout -b username-branch master
git pull <fork url> master
git rebase -i origin/master
git checkout master
git merge --no-ff username-branch
git push origin master
```

## Integration

[Integrations Directory](https://github.com/integrations)

[probot/probot: a trainable robot that responds to activity on GitHub](https://github.com/probot/probot)

## GitHub API

[GitHub API v3 | GitHub Developer Guide](https://developer.github.com/v3/)
[Creating an access token for command-line use - User Documentation](https://help.github.com/articles/creating-an-access-token-for-command-line-use/)

[ghapi | ghapi](https://ghapi.fast.ai/)
[Learn about ghapi, a new third-party Python client for the GitHub API - The GitHub Blog](https://github.blog/2020-12-18-learn-about-ghapi-a-new-third-party-python-client-for-the-github-api/)

[PyGithub/PyGithub: Typed interactions with the GitHub API v3](https://github.com/PyGithub/PyGithub)
[All the Things You Can Do With GitHub API and Python | by Martin Heinz | Towards Data Science](https://towardsdatascience.com/all-the-things-you-can-do-with-github-api-and-python-f01790fca131)

[michael/github: A higher-level wrapper around the Github API. Intended for the browser.](https://github.com/michael/github)

## Webhooks

[Webhooks | GitHub Developer Guide](https://developer.github.com/webhooks/)
[rvagg/github-webhook: A flexible web server for reacting GitHub Webhooks](https://github.com/rvagg/github-webhook)
[rvagg/github-webhook-handler: Node.js web handler / middleware for processing GitHub Webhooks](https://github.com/rvagg/github-webhook-handler)

## GitHub Archive

[GitHub Archive](https://www.githubarchive.org/)

[GitHub Data Challenge Winners](https://github.com/blog/1162-github-data-challenge-winners)
[Data Challenge II Results](https://github.com/blog/1544-data-challenge-ii-results)
[Third Annual GitHub Data Challenge](https://github.com/blog/1864-third-annual-github-data-challenge)
[Third Annual Data Challenge Winners](https://github.com/blog/1892-third-annual-data-challenge-winners)

[GitHut - Programming Languages and GitHub](http://githut.info/)
[donnemartin/viz: Interactive visualizations and stats of GitHub's newest, most popular repos.](https://github.com/donnemartin/viz)
[GeoBases](http://opentraveldata.github.io/geobases/)
[GitHub ArchiveRoom - Explore your GitHub archive data in 3D!](http://archiveroom.vf.io/)
