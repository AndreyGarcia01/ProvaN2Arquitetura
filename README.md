Feito por Andrey e Eliel 
Entregue dia 27/05/2023

Perguntas:

1) Quais benefícios podem ser obtidos com NGINX?

A) Alta performance e escalabilidade: O NGINX é conhecido por sua capacidade de lidar com um grande número de conexões simultâneas e alta carga de tráfego. Ele usa uma arquitetura assíncrona e eficiente em termos de recursos, permitindo um melhor desempenho e escalabilidade.

B) Balanceamento de carga: O NGINX oferece recursos integrados de balanceamento de carga, permitindo distribuir o tráfego entre vários servidores backend. Isso ajuda a melhorar a disponibilidade, a escalabilidade e o desempenho do sistema.

C) Proxy reverso: O NGINX pode ser configurado como um proxy reverso, permitindo redirecionar as solicitações dos clientes para servidores backend. Ele ajuda a otimizar o desempenho e a segurança, permitindo a implementação de recursos como cache, compressão, SSL/TLS offloading e gerenciamento de conexões.

D) Servir conteúdo estático: O NGINX é altamente eficiente na entrega de conteúdo estático, como arquivos HTML, CSS, JavaScript e imagens. Ele pode atuar como um servidor de arquivos estáticos dedicado, liberando recursos do servidor de aplicativos para processar solicitações dinâmicas.

E) SSL/TLS e HTTP/2: O NGINX suporta SSL/TLS para criptografar as comunicações entre clientes e servidores. Além disso, ele oferece suporte ao protocolo HTTP/2, que oferece melhorias significativas de desempenho em relação ao HTTP/1.1.

2) O que acontece se tentar subir dois servidores diferentes na mesma porta da mesma máquina?

Quando se tenta subir dois servidores diferentes na mesma porta da mesma máquina, ocorre um conflito porque cada porta pode ser usada apenas por um programa ou serviço em um determinado momento. O sistema operacional não permite que dois programas escutem na mesma porta simultaneamente.
Para resolver esse problema, é possível utilizar portas diferentes para cada servidor ou interromper o servidor em execução na porta desejada antes de iniciar o novo servidor. Isso garante que cada servidor tenha sua própria porta exclusiva e evita conflitos de portas. 

3) Quando pode ocorrer um erro de Cross-Domain (CORS - Cross-Origin Resource Sharing) e como você pode resolver isso?
Um erro de Cross-Domain (CORS) ocorre quando uma solicitação feita por um aplicativo web é bloqueada pelo navegador devido às políticas de segurança de mesma origem. Isso acontece quando um aplicativo web em um domínio (origem) tenta acessar recursos em outro domínio.
Para resolver um erro de CORS, você pode seguir estas medidas:
Configurar os cabeçalhos CORS adequados no servidor: Isso envolve incluir os cabeçalhos CORS corretos nas respostas do servidor, como Access-Control-Allow-Origin, Access-Control-Allow-Methods, Access-Control-Allow-Headers e Access-Control-Allow-Credentials. Esses cabeçalhos informam ao navegador que ele pode acessar os recursos de outro domínio.
Usar um proxy reverso, como o NGINX: Configurar um proxy reverso entre o aplicativo web e o servidor de recursos pode ajudar a resolver o erro de CORS. O proxy age como intermediário, enviando a solicitação ao servidor de recursos em nome do aplicativo web e adicionando os cabeçalhos CORS necessários na resposta antes de enviá-la de volta ao navegador.
Utilizar técnicas alternativas, como JSONP ou CORS com credenciais: Em certos casos, pode ser necessário recorrer a técnicas alternativas. O JSONP permite contornar as restrições de CORS, mas requer cooperação do servidor de recursos. O CORS com credenciais permite o envio e recebimento de cookies de autenticação, mas exige configurações adequadas tanto no servidor de recursos quanto no aplicativo web.
É importante ter em mente que a resolução do erro de CORS depende das configurações e requisitos específicos do servidor e do aplicativo web envolvidos. É recomendável consultar a documentação relevante e as diretrizes específicas do servidor e do navegador que está sendo usado para garantir uma configuração adequada do CORS.
