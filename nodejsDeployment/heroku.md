### Buildpacks
`heroku buildpacks:add`
`heroku buildpacks:remove`

### Heroku Buildpack for git lfs
[buildpack](https://elements.heroku.com/buildpacks/bureauxlocaux/heroku-buildpack-git-lfs)

### Heroku and Cloudflare
To add custom domain name to Heroku, use `heroku domains:add example.com`
With Clouflare, will need to add three:
  root domain: `example.com`
  sub domain: `www.example.com`
  wildcard domain: `*.example.com`
The DNS targets that are linked to these three domains need to be independently added to the DNS records on Cloudflare, or the other hosts I might be using. 