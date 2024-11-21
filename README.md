# expense-helm

This repos hosts all the needed helmCharts for expense project's frontend and backend

# How to install argocd cli 
```
    curl -sSL -o argocd-linux-amd64 https://github.com/argoproj/argo-cd/releases/latest/download/argocd-linux-amd64
    sudo install -m 555 argocd-linux-amd64 /usr/local/bin/argocd
    rm argocd-linux-amd64

    Ref: https://argo-cd.readthedocs.io/en/stable/cli_installation/
```


> What we achieved so far ?
1) I will just run the tf script 
    a) creates network
    b) creates rds 
    c) creates eks 
    d) installs argocd server
    e) installs metrics-server

2) Run the init.sh 
    a) Dynamically fetches the password for argo 
    b) Using that password, authenticates to argocd 
    c) Does the creaation fo argocd jobs ( Continuous Reconissance : whenever there is a change, deployment will happen automatically.)