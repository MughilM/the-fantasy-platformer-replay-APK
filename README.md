# The Fantasy Platformer: replay timelines

Per-week NFL player stat timelines used by The Fantasy Platformer's replay feature. The files are generated and
published automatically by the `timelines.yml` workflow in the app's repository. Don't edit them by hand: each run
overwrites them.

## Layout

`{season}/{week}.json.gz` is one gzipped JSON file per NFL week (weeks 19–22 are the postseason). For example:
`https://mughilm.github.io/the-fantasy-platformer-replay-APK/2025/15.json.gz`.

Each file lists the week's games (kickoff and end times in UTC), every play's per-player stat changes in time order,
and a map from nflverse GSIS player IDs to Sleeper player IDs. The format is defined by `timeline.schema.json` in the
app's repository (`schemaVersion` 1).

## Data and attribution

Built from [nflverse](https://github.com/nflverse) play-by-play, schedule, and player ID data, licensed
[CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/). The player ID mapping also uses Sleeper's public players
database. Not affiliated with the NFL, nflverse, or Sleeper.
