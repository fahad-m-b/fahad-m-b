name: Metrics
on:
  schedule: [{cron: "0 0 * * *"}]
  workflow_dispatch:
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
          user: fahad-m-b
          template: classic
          base: header, activity
          config_timezone: Asia/Muscat
          
          # Compact top languages bar
          plugin_languages: yes
          plugin_languages_colors: github
          plugin_languages_limit: 6
          plugin_languages_sections: most-used
          plugin_languages_details: percentage
