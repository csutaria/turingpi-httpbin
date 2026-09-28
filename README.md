# httpbin

Test service for the Traefik error-pages middleware, using
[go-httpbin](https://github.com/mccutchen/go-httpbin). Its `/status/{code}`
endpoint returns any HTTP status on demand.

Routed at `httpbin.traefik.lan` with `error-pages-middleware` from the
`error-pages` namespace attached. The cross-namespace reference requires
Traefik's `providers.kubernetesCRD.allowCrossNamespace: true`.

Register with Argo CD: `kubectl apply -f argocd/application.yaml`
