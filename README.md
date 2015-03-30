# resync

`sync.Once` with `Reset()`

  * See [sync.Once](http://golang.org/pkg/sync/#Once)

## Example

```
// use it just like sync.Once
var once resync.Once

func handleRequest(w http.ResponseWriter, r *http.Request) {
	once.Do(func(){
		// load templates or something
	})
	// TODO: repsond
}

func handleResetRequest(w http.ResponseWriter, r *http.Request) {
	once.Reset() // call Reset to cause initialisation to happen again above
}
```
