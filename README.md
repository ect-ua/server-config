# Configurar um servidor ECT-UA

Este repositório contém toda a configuração necessária para replicar um servidor ECT-UA com todas as funcionalidades disponíveis em https://www.ect-ua.com.

Este repositório inclui:

- Chat ECT-UA (diretório `chat`)
- IdP ECT-UA (diretório `idp`)
- Antigo fórum myNEECT (diretório `myneect`)

Não façam modificações diretamente no servidor! Testem-nas localmente primeiro e garantam que o servidor, sempre que possível apenas faz pull deste repositório com o git.

## Iniciar os serviços

O ECT UA não é um software apenas, mas sim um conjunto de aplicações individuais que partilham sessões usando um IdP e que se interligam com um servidor Nginx.

Dentro de cada um dos diretórios deste repositório encontras as aplicações individuais que deves executar. Para as executares, precisas ter instalados o [Docker](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04) e o [Docker Compose](https://www.digitalocean.com/community/tutorials/how-to-install-docker-compose-on-ubuntu-18-04) no teu computador (links para Ubuntu 18.04).


## Ligar os serviços com o Nginx

Para integrar todos os serviços sob o mesmo domínio, segue as instruções disponíveis no repositório https://github.com/ect-ua/nginx-config.


## Uso no sistema de produção


Garante sempre que neste repositório está a última versão das configurações do NGINX do servidor. Para isso, sugiro que cries um Pull Request sempre que pretendes sugerir alterações e que não edites diretamente os ficheiros no branch master, a menos que tal faça sentido. Se não tens permissões de escrita sobre este repositório, faz um fork do mesmo e depois submete o teu Pull Request. Sabe mais aqui: https://help.github.com/articles/creating-a-pull-request-from-a-fork/.

Fizeste as tuas alterações diretamente no servidor?

Se tudo está a funcionar corretamente, já executaste o comando para testar e as tuas alterações já estão no branch master deste repositório, convém repôr tudo outra vez de novo para evitar problemas. O procedimento é o mesmo caso tenhas feito asneira e agora nada funcione, por isso estás no bom caminho.

Para voltar a sincronizar com o git, executa estes comandos:

1. ```git reset --hard``` -> Isto vai apagar as tuas alterações
2. ```git pull``` -> Isto vai fazer download da versão mais recente

Depois disto, não te esqueças de iniciar ou reiniciar cada um dos serviços.

Se o git está todo lixado e nada funcionar, não entres em desespero. Existem formas de voltar atrás no histórico. Qualquer dúvida, pergunta a qualquer colega com mais experiência em git.


## Ajuda

Se precisares de ajuda, contacta a equipa do ECT-UA pelo email `projetoectua [arroba] gmail.com`.
