transform binary data to string

can be use on img, like this `src="data:image/png;base64...`

## example
![example](example.png)

* 将 'M', 'a', 'n', 3 * 8 bit 分成一组

* 将 24 bit 分成 6 bit 一组，每组前面补0，得到4个base64编码表的索引

* 在 base64 编码表查询，得到 'T', 'W', 'F', 'u'

## btoa 

encode
```js
// btoa
s = 'hello'
s = btoa(s) // aGVsbG8=
u8 = stb(s) // [97, 71, 86, 115, 98, 71, 56, 61]

// custom
s = 'hello'
u8 = stb(s) //  [104, 101, 108, 108, 111]
u8 = encode(u8) // [97, 71, 86, 115, 98, 71, 56, 61]
```

decode
```js
// custom
s = 'aGVsbG8='
u8 = stb(s) // [97, 71, 86, 115, 98, 71, 56, 61]
u8 = decode(u8) // [104, 101, 108, 108, 111]

// atob
s = 'aGVsbG8='
s = atob(s) // hello
u8 = stb(s) // [104, 101, 108, 108, 111]
```
