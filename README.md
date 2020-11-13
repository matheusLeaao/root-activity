# Root Activity

Esta documentação se destina a como implementar o envio da atividade de conta Root para uma sala no Slack. É necessário que exista um trail multirregional criado no Cloudtrail, para que haja correta detecção de tal atividade, para implementação, seguir os passos abaixo:

1 – Subir os arquivos RootActivityLambda.zip e RootAPIMonitor.json para um bucket S3, os quais serão utilizados para a posterior criação do recursos necessários no Cloudformation. Este bucket deve estar na mesma região em que o Cloudformation e a Lambda serão provisionados posteriormente;
![Alt text](https://gitlab.com/mandic-labs/teams/team-delta/tutoriais/root-activity/-/raw/d007f73db0ed767ccf1009e21b379aacf9bd88be/Images/tutoimagem1.jpg)



2 – Após, é necessário acessar o console do CloudFormation dentro da conta da AWS;




