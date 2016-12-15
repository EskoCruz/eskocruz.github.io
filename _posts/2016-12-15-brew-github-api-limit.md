---
published: false
title: Brew\'s GitHub API Limit Error
---
## Brew's GitHub API Limit

    Error: GitHub API Error: API rate limit exceeded for 74.10.26.50. (But here's the good news:
    Authenticated requests get a higher rate limit. Check out the documentation for more details.)
    Try again in 28 minutes 46 seconds, or create a personal access token:
      https://github.com/settings/tokens/new?scopes=gist,public_repo&description=Homebrew
      and then set the token as: export HOMEBREW_GITHUB_API_TOKEN="your_new_token"
    Enter text in [Markdown](http://daringfireball.net/projects/markdown/). Use the toolbar above, or click the **?** button for formatting help.
    
![GitHub Personal Access Token]({{site.baseurl}}/images/brew-github-api.png)

`$ export HOMEBREW_GITHUB_API_TOKEN="[your_new_token]"`
