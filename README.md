# cheatsheet

* collection of personal cheatsheets
* using this function to print cheatsheet

```bash
cheatsheet () {
    [[ -z "${1}" ]] && echo cheatsheet \<name of cheatsheet\> && return
    pandoc ~/cheatsheets/${1} | lynx -dump -stdin || could find cheatsheet
}
```

* also using this simple completion function 

`compdef '_files -W  ~/cheatsheets/' cheatsheet`