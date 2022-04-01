<h3>Ubuntu</h3>

Use a function to quickly spin this instance up, with persistant storage.<br>

```bash
function ubuntu () {
	dirname=${PWD##*/}
	docker run -v `pwd`:/${dirname} -w /${dirname} -it --rm ubuntu
}
```
