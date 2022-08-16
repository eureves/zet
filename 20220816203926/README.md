# Unit tests in nodejs

Unit test can be made with `Jest` library.

```javascript
it("name of the test", () => {
	expect(() => "returned value").toBe("returned value") # => pass
}
```

Async
```javascript
it("name of the test", () => {
	expect.assertion(1)
	return new Promise(...args).then(data => expect(data).toBe(data))
}
```

#testing #development
