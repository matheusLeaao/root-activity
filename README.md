# Root Activity

Esta documentação se destina a como implementar o envio da atividade de conta Root para uma sala no Slack. É necessário que exista um trail multirregional criado no Cloudtrail, para que haja correta detecção de tal atividade, para implementação, seguir os passos abaixo:

1 – Subir os arquivos RootActivityLambda.zip e RootAPIMonitor.json para um bucket S3, os quais serão utilizados para a posterior criação do recursos necessários no Cloudformation. Este bucket deve estar na mesma região em que o Cloudformation e a Lambda serão provisionados posteriormente;
![Alt text](root-activity/Images/tutoimagem1.jpg?raw=true "Title")


2 – Após, é necessário acessar o console do CloudFormation dentro da conta da AWS;




