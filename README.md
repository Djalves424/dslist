# Intensivão Java com Spring

(Efetuado curso aconhando as aulas com Prof. Nelio Alves)

 API Rest:

Padrão Rest

•	Cliente/servidor com HTTP

•	Comunicação stateless (*)

•	Interface uniforme, formato padronizado (*)

•	Cache

•	Sistema em camadas

•	Código sob demanda (opcional) 

https://www.redhat.com/pt-br/topics/api/what-is-a-rest-api

#######################################################################################

Padronização

GET https://meusistema.com/buscar-produto/5

                                                  ➝ INCORRETO      

GET https://meusistema.com/deletar-produto/5

#######################################################################################

Padronização

GET https://meusistema.com/produtos 

GET https://meusistema.com/produtos/5

POST https://meusistema.com/produtos

                                                ➝ CORRETO                            

{ ... }
                                      
PUT https://meusistema.com/produtos/5

{ ... }

DELETE https://meusistema.com/produtos/5

#######################################################################################

# Padrão de camadas

![image](https://github.com/Djalves424/dslist/assets/108296040/d9f60976-3604-4fb2-95f8-079d6e942cb2)

#######################################################################################

# Relacionamentos

![image](https://github.com/Djalves424/dslist/assets/108296040/20169642-9897-4128-bbf3-cdb68022ee16)

# MODELO DE OBJETOS

![image](https://github.com/Djalves424/dslist/assets/108296040/0ba31301-49b8-4d2b-b94c-c7792aa7db3c)

# MODELO RELACIONAL

![image](https://github.com/Djalves424/dslist/assets/108296040/84ad40ca-907a-42cf-b527-cc60260e798a) ### ![image](https://github.com/Djalves424/dslist/assets/108296040/501f8e8b-bd75-4d96-a741-406bd0feaf0f)

![image](https://github.com/Djalves424/dslist/assets/108296040/dbd8bbd8-5bb9-43c4-91fc-01fad910cd36)

#######################################################################################

# Perfis de projeto

1.	Perfil de desenvolvimento e testes:

-	test
-	
-	Banco de dados H2

2.	Perfil de homologação / staging:

-	dev

-	Banco de dados Postgres de homologação

3.	Perfil de produção:

-	prod

-	Banco de dados Postgres de produção

#######################################################################################

# Passos para homologação

OPCIONAL NO TREINAMENTO!!

Preparação do ambiente

Docker ou

Postgresql + pgAdmin ou DBeaver

Homologação local

1.	Criar perfis de projeto
   
*	system.properties

2.	Gerar script da base de dados

*	apagar arquivo gerado

3.	Criar base de dados de homologação

4.	Rodar app no modo dev e validar

#######################################################################################

# Passos deploy CI/CD

OPCIONAL NO TREINAMENTO!!

Pré-requisitos

-	Conta no Railway

-	Conta no Github com mais de 90 dias

-	Projeto Spring Boot salvo no seu Github

-	Script SQL para criação e seed da base de dados

-	Aplicativo de gestão de banco instalado (pgAdmin ou DBeaver)

# Passos Railway

1.	Prover um servidor de banco de dados

2.	Criar a base de dados e seed

3.	Criar uma aplicação Railway vinculada a um repositório Github

4.	Configurar variáveis de ambiente

```

APP_PROFILE

DB_URL (Formato:

jdbc:postgresql://host:porta/nomedabase)

DB_USERNAME

DB_PASSWORD CORS_ORIGINS

```

5.	Configurar o domínio público para a aplicação

6.	Testar app no Postman

7.	Testar a esteira de CI/CD


  









