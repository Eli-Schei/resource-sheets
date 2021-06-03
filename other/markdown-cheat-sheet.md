
# Code blocks

You create a code block by writing three back-ticks ` ``` ` on the line before and below your code. 

And you add syntax highlighting to id by adding the programminglanguage after the last back-tick on the first line: ` ```javascript `


## Below is an empty codeblock
```
```

## Below is a codeblock with javascript - without syntax highlighting
```
const myFunction = () => {
    console.log("This is my function");
}
```

## Below is a codeblock with javascript - with syntax highlighting
```javascript
const myFunction = () => {
    console.log("This is my function");
}
```

## Below is a codeblock with powershell syntax highlighting
```powershell
Connect-PnPOnline "yourtenantURL" -Interactive

Get-PnPTenantAppCatalogUrl
```
