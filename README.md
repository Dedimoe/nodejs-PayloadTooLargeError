# nodejs-PayloadTooLargeError
nodejs: PayloadTooLargeError: request entity too large

Solution:
```
const express = require("express")
...
app.use(express.json({ limit: "50mb" }))
```
and
```
app.use(express.urlencoded({ limit: "50mb", extended: true, parameterLimit: 50000 }))
```
