name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *" # every day at midnight
  workflow_dispatch:

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - name: Generate Snake SVG
        uses: Platane/snk@v3
        with:
          github_user_name: codewithmohin
          outputs: |
            output/github-contribution-grid-snake.svg

     
