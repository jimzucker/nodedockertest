# nodedockertest
Example using official node docker image

##Build
=======
#Build
docker build . -t nodedockertest

#run
docker run nodedockertest

#The secret sauce Package.json
##Take a look at the packge.json, the docker image will run 'npm install' and then 'node start'
##The install will pull all of the code and then start will run the script specified in the scripts configuraiton
```json
{
  "name": "github-webhook-handler",
  "version": "0.6.0",
  "description": "Web handler / middleware for processing GitHub Webhooks",
  "main": "github-webhook-handler.js",
  "scripts": {
    "start": "node test.js"
  },
  "keywords": [
    "github",
    "webhooks"
  ],
  "author": "Rod Vagg <r@va.gg> (http://r.va.gg)",
  "license": "MIT",
  "dependencies": {
    "github-webhook-handler": "git://github.com/rvagg/github-webhook-handler.git",
    "bl": "~1.1.2",
    "buffer-equal-constant-time": "~1.0.1"
  },
  "devDependencies": {
    "run-series": "~1.1.4",
    "tape": "~4.6.0",
    "through2": "~2.0.1"
  }
}
```
