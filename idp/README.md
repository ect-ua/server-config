# Configurar o IdP ECT-UA

Este repositório contém toda a configuração necessária para replicar um servidor IdP ECT-UA com todas as funcionalidades disponíveis em https://idp.ect-ua.com.

Este repositório inclui:

- Tema ECT-UA para Keycloak (diretório `ect-ua-theme`)
- Configuração docker-compose (ficheiro `docker-compose.yml`)

Como é óbvio, não coloquem aqui as configurações do servidor de produção. Nunca. Em vez disso, usem um fork destas configurações privado e apenas acessível à equipa de desenvolvimento do ECT-UA.


## Iniciar os serviços

Para arrancar o idp, executa:

```docker-compose up```

O IdP estará disponível no endereço http://localhost:8080/. Por defeito, o nome de utilizador e palavra-passe são, respetivamente, `admin` e `Pa55w0rd`.


## Domínio idp.ect-ua.com ou idp.ectuadev

Para integrar o IdP sobre um domínio, segue as instruções disponíveis no repositório https://github.com/ect-ua/nginx-config.


## Contribuir para este repositório

Garante sempre que neste repositório está a última versão das configurações do servidor. Para isso, sugiro que cries um Pull Request sempre que pretendes sugerir alterações e que não edites diretamente os ficheiros no branch master, a menos que tal faça sentido. Se não tens permissões de escrita sobre este repositório, faz um fork do mesmo e depois submete o teu Pull Request. Sabe mais aqui: https://help.github.com/articles/creating-a-pull-request-from-a-fork/.

Fizeste as tuas alterações diretamente no servidor?

Se tudo está a funcionar corretamente, já executaste o comando para testar e as tuas alterações já estão no branch master deste repositório, convém repôr tudo outra vez de novo para evitar problemas. O procedimento é o mesmo caso tenhas feito asneira e agora nada funcione, por isso estás no bom caminho.

Para voltar a sincronizar com o git, executa estes comandos:

1. ```git reset --hard``` -> Isto vai apagar as tuas alterações
2. ```git pull``` -> Isto vai fazer download da versão mais recente

Depois disto, não te esqueças de iniciar ou reiniciar cada um dos serviços.

Se o git está todo lixado e nada funcionar, não entres em desespero. Existem formas de voltar atrás no histórico. Qualquer dúvida, pergunta a qualquer colega com mais experiência em git.


## Ajuda

Se precisares de ajuda, contacta a equipa do ECT-UA pelo email `projetoectua [arroba] gmail.com`.
