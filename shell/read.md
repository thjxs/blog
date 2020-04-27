## read use input
```sh
read -p 'message: ' message
if [ -z "$message" ]; then
    exit    
fi
# use message as variable
somecmd $message
# if message contain whitespace
# such as "hello word"
# then in somecmd, $1 eq hello, $2 eq word
# you should avoid this, try 
somecmd "$message"
```
