
name: GitHub-Profile-3D-Contrib

on:
  schedule:
    # Runs automatically every day at midnight (UTC)
    - cron: "0 0 * * *"
  # Allows manual execution from the Actions tab
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    name: generate-github-profile-3d-contrib
    steps:
      - uses: actions/checkout@v3
      - uses: yoshi389111/github-profile-3d-contrib@0.7.1
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          USERNAME: Ambati4422
      - name: Commit & Push changes
        run: |
          git config user.name github-actions[bot]
          git config user.email github-actions[bot]@users.noreply.github.com
          git add -A .
          git commit -m "Generated 3D Contribution Graph" || exit 0
          git push
## 📊 3D Contribution Graph

![Ambati4422's 3D Contribution Graph](./profile-3d-contrib/profile-green-animate.svg)

   
 
