# Root Activity

Esta documentação se destina a como implementar o envio da atividade de conta Root para uma sala no Slack. É necessário que exista um trail multirregional criado no Cloudtrail, para que haja correta detecção de tal atividade, para implementação, seguir os passos abaixo:

1 – Subir os arquivos RootActivityLambda.zip e RootAPIMonitor.json para um bucket S3, os quais serão utilizados para a posterior criação do recursos necessários no Cloudformation. Este bucket deve estar na mesma região em que o Cloudformation e a Lambda serão provisionados posteriormente;


2 – Após, é necessário acessar o console do CloudFormation dentro da conta da AWS;

![Alt text](https://gitlab.com/mandic-labs/teams/team-delta/tutoriais/root-activity/-/raw/d007f73db0ed767ccf1009e21b379aacf9bd88be/Images/tutoimagem1.jpg)

3 – Na página do CloudFormation, escolher a opção de criar uma nova Stack e criar uma com novos recursos;
![Alt text](https://gitlab.com/mandic-labs/teams/team-delta/tutoriais/root-activity/-/raw/d007f73db0ed767ccf1009e21b379aacf9bd88be/Images/tutoimagem2.jpg)

4 – Na página a seguir, inicialmente, escolher a opção de template pronto, com a origem de um S3, e informar a URL do objeto para a criação, e após, prosseguir;
![Alt text](https://gitlab.com/mandic-labs/teams/team-delta/tutoriais/root-activity/-/raw/d007f73db0ed767ccf1009e21b379aacf9bd88be/Images/tutoimagem3.jpg)

5 – Ao prosseguir, preencher os seguintes dados:
**Stack name:** com o nome da Stack que será criada para provisionamento;
**SNSSubscriptions:** o endereço de e-mail que irá efetuar a a inscrição SNS;
**SNSTopicName:** Nome do tópico SNS que irá receber a notificação do root (e que será utilizado posteriormente para a Lambda que irá triggar a notificação do Slack);
**LambdaTimeout:** o tempo para timeout da função Lambda. Pode ser deixado o padrão de 60 segundos;
**LambdaS3bucket:** Nome do Bucket em que foram provisionados os arquivos no passo 1;

![Alt text](https://gitlab.com/mandic-labs/teams/team-delta/tutoriais/root-activity/-/raw/d007f73db0ed767ccf1009e21b379aacf9bd88be/Images/tutoimagem4.jpg)

6 – Na página seguinte, criar a Tag com o nome da Stack e adicionar outras, se for necessário;

![Alt text](https://gitlab.com/mandic-labs/teams/team-delta/tutoriais/root-activity/-/raw/d007f73db0ed767ccf1009e21b379aacf9bd88be/Images/tutoimagem5.jpg)

7 – No próximo passo, rolar até o fim da página, e marcar a opção “I acknowledge that AWS CloudFormation might create IAM resources with custom names” e criar a Stack.

![Alt text](https://gitlab.com/mandic-labs/teams/team-delta/tutoriais/root-activity/-/raw/d007f73db0ed767ccf1009e21b379aacf9bd88be/Images/tutoimagem6.jpg)







