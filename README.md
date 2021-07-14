# Teste para candidatos à vaga de DevOps

> Candidatos para vaga de DevOps na Viva Decora devem responder este teste como parte do processo seletivo. A solução do teste deve estar disponível em um repositório online (Github, Bitbucket, etc) e o link deve ser encaminhado por **mensagem ou email**. Pode ser um repositório público ou um repositório privado com acesso para o avaliador. **Será desclassificado quem entregar a solução fazendo fork deste projeto ou criando uma issue no mesmo.**

## Desafio DevOps

Este teste tem como objetivo avaliar as capacidades do candidato em entregar uma aplicação web simples aplicando boas práticas de provisionamento. 

O desafio é dividido em 2 partes:
* Provisionamento da aplicação web thumbor na AWS (ec2, beanstalk, lambda, etc)
* Deploy

## Sobre o thumbor

O Thumbor é um serviço de imagens descrito e documentado no seguinte repositório https://github.com/thumbor/thumbor
Uma vez que o serviço do thumbor esteja disponível em uma url ele pode receber requisições para manipulação de imagens

Esse provisionamento do Thumbor de levar em consideração apenas o modo unsafe do Thumbor para efeitos de simplificação da análise

### Provisionamento da infraestrutura
 
A solução do teste deve ser capaz de criar de forma automatizada toda infraestrutura necessária para o Thumbor

Para servir essa aplicação, pode-se utilizar serviços da AWS mais básicos como o EC2 ou mais instrumentados como o Beanstalk ou o Lambda. O desenvolvedor deve definir quais serviços da AWS serão utilizados.


#### Requisitos não funcionais

1. A infraestrutura onde irá rodar a aplicação web deverá ser provisionada em uma das seguintes formas:
1.1 Ferramentas de automação como ansible, puppet, terraform, etc.
1.2 Usando ferramentas de script como awscli.

2. A aplicação web deve rodar na porta `8000`.

**A documentação do projeto deve explicar como provisionar o servidor.**


### Deploy

Deverá ser possível fazer deploy da aplicação web na infraestrutura.
O deploy pode usar alguma ferramenta simples como rsync, scp ou outra ferramenta que você preferir.

**A documentação do projeto deverá mostrar como fazer o deploy da aplicação.**

## Critérios de avaliação

A solução do teste será avaliada segundo os requisitos funcionais e não funcionais propostos.

Em uma conta nossa da AWS, iremos:
* Indepotência na criação do servidor.
* Criar os serviços e fazer deploy da aplicação web seguindo a documentação entregue junto com o projeto.
* Validar se a API fornecida fornece os resultados esperados.
* Alterar a API e fazer um novo deploy.
* Remover os serviços provisionados seguindo a documentação entregue junto com o projeto.

Além disso, analisaremos o código do projeto entregue segundo algumas boas práticas de desenvolvimento, como:
* Facilidade para servir a aplicação, fazer deploy, criar e destruir serviços da AWS.
* Facilidade para dar manutenção nos serviços da AWS
* Legibilidade do código
