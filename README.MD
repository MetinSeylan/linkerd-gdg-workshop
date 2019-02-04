### Pre-Check
`linkerd check --pre`

### Basic Install LinkerD
`linkerd install | kubectl apply -f -`

### Check Deployments
`kubectl get deploy -n linkerd`

### Dashboard
`linkerd dashboard`

### Install Demo App
`linkerd inject booksapp.yaml | kubectl apply -f -`

### CRD for routes
```bash
linkerd profile --open-api swagger/webapp.swagger webapp | kubectl apply -f -
linkerd profile --open-api swagger/books.swagger books | kubectl apply -f -
linkerd profile --open-api swagger/authors.swagger authors | kubectl apply -f -
```