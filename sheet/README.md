# export Excel file

## install 
`yarn add xlsx`

## export file with json
```js
let aoo = []
for(let i = 0; i < 100; i += 1) {
    aoo.push({
        x: i,
        y: 2 * i + Math.random()
    })
}
// worksheet
let ws = XLSX.utils.json_to_sheet(aoo)
// workbook
let wb = XLSX.utils.book_new()
// append worksheet
XLSX.utils.book_append_sheet(wb, ws, 'Sheet1')
// XLSX.utils.book_append_sheet(wb, another_ws, 'another_Sheet')
XLSX.writeFile(wb, 'filename.xlsx')
```
