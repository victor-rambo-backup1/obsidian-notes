
## Características:

- Aplicações que rodam em um modelo cliente-servidor;
- Permitem que múltiplas aplicações se comuniquem com ele por meio de protocolos;
- Evita ter que abrir uma aplicação toda vez pra requisitar o serviço;
- Muito usado para serviços essenciais como internet, bluetooth, audio.

## Como Funciona:

Aplicação invoca sistema, sistema invoca daemon, se comunica por algum protocolo, daemon devolve resposta pro sistema, sistema devolve resposta pra aplicação.

## Instalando Daemons:

No linux, podemos instalar um daemons da mesma forma que qualquer outro pacote.

Para utilizalo devemos ativa-lo usando systemctl:

```bash
sudo systemctl enable -now <daemon>
```

-enable: ativa depois de reiniciar, configura como default para todo boot.

-now: obriga a ativar agora.

Para verificar o status do sistema rodar:

```bash
sudo systemctl status <daemon>
```