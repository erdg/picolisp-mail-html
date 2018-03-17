# picolisp-mail-html
The built-in picolisp 'mail' function, extended to support HTML.

## documentation
See `(doc 'mail)` for details. Function signature is the same. The 'prg' argument accepts arbitrary HTML. The 'mail-html' function provides opening and closing '<html>' and '<body>' tags.

### usage
```
   (load "@lib/xhtml.l")

   (mail-html "localhost" 25                    # host, port
      "from@mail.com"                           # from
      "to@mail.com"                             # to
      "Subject Line"                            # subject
      (quote                                    # attachments
         "attachment1.pdf" "attachment2.png" )
      "Hello,"                                  # body
      NIL
      (<p> NIL "This is some " (<strong> NIL "strong") " text." )
      (prinl "<p>This works <i>too</i></p>") )
```

