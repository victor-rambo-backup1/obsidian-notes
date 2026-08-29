
## Status code

`2XX`: Sucesso na operação

`4XX`: Não consegui fazer operação

`5XX`: Tentou fazer operação e deu problema no servidor

- 200: Servidor aceitou request e processou
- 201: Servidor conseguio criar a entidade, geralmente post
- 202: Servidor aceitou request, mas não processou ainda
- 204: Servidor não tem conteudo para retornar, geralmente delete
- 301: Recurso foi movido para uma nova localização
- 400: Servidor não conseguio processar o request, geralmente formato errado
- 401: Servidor não sabe quem você é precisa autenticar
- 403: Servidor sabe quem você é mas você não tem permissão pra acessar o recurso
- 404: Servidor não achou o recurso, provalmente URL errada
- 500: Erro interno do servidor
- 503: Servidor fora do ar

## IP Address

- Endereço do dispositivo na rede

## IP público

- Acessível pela internet
- É único em toda a internet

## IP privado

- Não é acessível pela internet
- É único dentro de uma rede local

## Roteador

- A ponte entre a internet e os dispositivos de uma rede local
- Permite que dispositivos locais (com ip privados) acessem a internet por meio do ip público do roteador
- Possui um ip público e um privado
- Utiliza ip público para se comunicar na internet
- Utiliza ip privado para se comunicar na rede local

## TCP (Transmission Control Protocol)

- Protocolo de transporte.
- Comunicação na internet
- Quebra os dados em pacotes
- Envia os pacotes
- Garente que os pacotes enviados pela rede cheguem na ordem certa
- Pede pacote de novo em caso de dado perdido

## HTTP (Hypertext Transfer Protocol):

- Protocolo de aplicação
- Rege como o cliente e servidor vão se comunicar entre sí
- Não governa com vai ser transferido os dados,
- Governa como eles vão ser estruturados e interpretados
- Uma norma para padronizar requests e responses

## DNS (Domain Name System)

- Ligar o domínio da URL a um IP
- Existe o servidor DNS que dado um domínio retorna o IP
- Alguns domínios podem estar atrelados a multiplos IPs
- Database distribuida
- Passa por 3 servers:
    - Pergunta ao root name server qual servidor que trabalha com .com
    - Retorna o IP desse servidor
    - Pergunta ao .com name server qual servidor que sabe sobre o domínio que eu quero
    - Retorna o IP desse servidor
    - Esse servidor retorna o IP do site que você quer para o servidor DNS
    - O servidor DNS retornar o IP do site que você quer

## URL (Universal Resource Locator)

- É como os recursos são localizados na internet
- São compostos principalmente por 3 partes:
    - Protocolo: O protocolo de aplicação que será usado para comunicação
    - Dominio: Atráves do DNS vai virar o IP
    - Recurso: É oque eu quero, o endpoint, não necessariamente algo físico
    - Parâmetros: São informações extras que podem ser usado pelo servidor web de qualquer forma
    - Ancora: Carrega a página html direto num elemento específico, não é mandando no request, é coisa do browser
- Uma URL pode ser:
    - URL Absoluta: a ULR padrão com todos os campso obrigatórios
    - URL Relativa: o browser com base na página atual consegue inferir algumas informações que você deixou de fora da URL

## ISP (Internet Serviçe Provider)

- A compania de internet
- Por default o servidor DNS usado vai ser o da compania de internet

## Port Number

- É uma int de 16 bits que indica qual processo que vai ser usado no servidor

## DOM (Document Objet Model)

- É um representação do HTML em uma estrutura de memória
- Permite que o javascript manipule o HTML sem ter que interagir com o texto cru

HTML → DOM → APLICA CSS → RENDER TREE