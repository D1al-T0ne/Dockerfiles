<h3>Discovery</h3>

```bash
function discovery(){
  dirname=${PWD##*/}
  docker run -v `pwd`:/${dirname} -w /${dirname} -it --rm discovery
}
```
