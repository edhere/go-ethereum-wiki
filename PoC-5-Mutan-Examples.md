## Currency

```go
init {
	store[this.Origin()] = 10^20
}

main {
	big to = this.Data(0)
	big from = this.Origin()
	big value = this.Data(1)

	if store[from] > value {
		store[from] = store[from] - value
		store[to] = store[to] + value
	}
}
```