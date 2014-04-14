# heroku-buildpack-tessera

I am a Heroku buildpack that installs
[tessera](https://github.com/mojodna/tessera) and its dependencies to serve up
[tilelive](https://github.com/mapbox/tilelive.js)-compatible maps and data.

## Using

When deploying a map to Heroku for the first time, run the following inside
a `tessera`-compatible map project (currently just TileMill 2 styles):

```bash
heroku apps:create -b https://github.com/mojodna/heroku-buildpack-tessera.git

git push heroku master
```

This may take up to 5 minutes. Accompanying
[TileJSON](https://www.mapbox.com/developers/tilejson/) will be available at
`/index.json`.
