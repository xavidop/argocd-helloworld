# argocd-helloworld


Install Kind

install argocd cli:` brew install argocd` https://argo-cd.readthedocs.io/en/stable/cli_installation/

./install.sh


argocd login localhost --insecure --grpc-web-root-path argocd


argocd app create app2 \
    --project default \
    --repo https://github.com/xavidop/argocd-helloworld/ \
    --path app \
    --dest-namespace default \
    --dest-server https://kubernetes.default.svc \
    --sync-policy auto \
    --revision main  

https://github.com/LaraPruna/DespliegueArgoCD#introduccion