<h3>Discovery</h3>

```bash
function discovery(){
  dirname=${PWD##*/}
  docker run -v `pwd`:/${dirname} -w /${dirname} -it --rm discovery
}
```

## Tools

| Tool | Repository |
|---|---|
|arjun|https://github.com/s0md3v/Arjun|
|dirsearch|https://github.com/maurosoria/dirsearch|
|gau|https://github.com/lc/gau|
|kiterunner|https://github.com/assetnote/kiterunner|
|linkfinder|https://github.com/GerbenJavado/LinkFinder|
|paramspider|https://github.com/devanshbatham/ParamSpider|
|subjs|https://github.com/lc/subjs|
|unfurl|https://github.com/tomnomnom/unfurl|
