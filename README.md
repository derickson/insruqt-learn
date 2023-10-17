# Learning Instruqt

https://docs.instruqt.com/getting-started/set-up-instruqt#step-3-set-up-your-chosen-tool

![Learning Track](image.png)

```bash
instruqt auth login
```

```bash
instruqt track create
cd MYDIR
instruqt track push     
instruqt challenge create --title "Creating a text file"
## Make some changes etc
instruqt track push     
instruqt track open
```

https://play.instruqt.com/inspiration-library


## ingress

 To allow external ingress traffic to a hosted VM add the
    `allow_external_ingress` attribute to a tracks `config.yml` file.

   One of the optional values that can be set is the `http` option. This allows
    the exposure of an HTTP server hosted within the VM to the public internet.

```yml
tabs:
- title: Shell
  type: terminal
  hostname: external-ingress
- title: Internal Website
  type: service
  hostname: external-ingress
  port: 80
- title: Broken Website
  type: website
  url: https://external-ingress.${_SANDBOX_ID}.instruqt.io
```