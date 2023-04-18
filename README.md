# desafio5-solucao

oc new-project hooks
oc new-app --name=post https://github.com/leandroppereira/desafio5-solucao

Data a criação, é necessário setar o hook


Setar o post:
oc set build-hook bc/post --post-commit --script="python3 /opt/email.py"

Ver os logs:
oc logs -f bc/post

Você vai ver o trecho no log:
Send e-mail