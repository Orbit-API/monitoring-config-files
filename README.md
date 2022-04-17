# Monitoramento e Alerta

Repositório para os arquivos de configuração do Prometheus e Alert Manager necessários para o monitoramento da aplicação alvo.

## Instalando Prometheus e Alert Manager

### Windows
#### Prometheus

- Para instalar o Prometheus no Windows, vá até a página do [Prometheus](https://prometheus.io/download/) e baixe a versão *2.34.0*.
- Extraia a pasta no local desejado e inicie o arquivo executável.

#### Alert Manager
- Para instalar o Alert Manager no Windows, vá até a página do [Prometheus](https://prometheus.io/download/) e baixe a versão *0.24.0*.
- Extraia a pasta no local desejado e inicie o arquivo executável.


### Linux
#### Prometheus

- Para instalar o Prometheus no Linux, vá até a página do [Prometheus](https://prometheus.io/download/) e baixe a versão *2.34.0*.
- Extraia a pasta no local desejado e inicie o arquivo executável através da interface gráfica ou terminal.
- Para iniciar através do terminal, é preciso entrar na pasta *prometheus-2.34.0.linux-amd64* e executar o arquivo **prometheus**.

```bash
cd prometheus-2.34.0.linux-amd64

./phometheus
```

#### Alert Manager
- Para instalar o Alert Manager no Linux, vá até a página do [Prometheus](https://prometheus.io/download/) e baixe a versão *0.24.0*.
- Extraia a pasta no local desejado e inicie o arquivo executável através da interface gráfica ou terminal.
- Para iniciar através do terminal, é preciso entrar na pasta *alertmanager-0.24.0.linux-amd64* e executar o arquivo **alertmanager**.

```bash
cd alertmanager-0.24.0.linux-amd64

./alertmanager
```

## Configuração dos arquivos

Antes de iniciar o Prometheus e o Alert Manager, é necessário realizar a configuração no arquivo **prometheus.yml** localizado na pasta *prometheus-2.34.0.linux-amd64*.

#### Prometheus
- [Neste repositório](https://github.com/Orbit-API/monitoring-config-files/blob/master/prometheus/prometheus.yml) disponibilizamos o conteúdo que deve ser adicionado dentro deste arquivo.
- Salve as alterações.

#### Alert Manager
- Crie o arquivo **alert.rules.yml** dentro da pasta *prometheus-2.34.0.linux-amd64* e cole o conteúdo disponibilizado [aqui](https://github.com/Orbit-API/monitoring-config-files/blob/master/prometheus/alert.rules.yml).
- Salve aso arquivo.

- Optamos pelo envio da notificação do alerta para o Canal Orbit no Slack. Também é necessário realizar essa configuração e, para isso, deve-se criar um novo arquivo **alertmanager.yml** dentro da pasta *alertmanager-0.24.0.linux-amd64* e adicionar o conteúdo disponibilizado [aqui](https://github.com/Orbit-API/monitoring-config-files/blob/master/alert-manager/alertmanager.yml).
- Salve o arquivo.

- Após a realização das alterações, pode-se iniciar os arquivos executáveis **prometheus** e **alertmanager**, como mencionado anteriormente.

**Obs: caso deseje entrar para o grupo do Slack para o qual as notificações estão sendo enviadas, entre em contato conosco através do Canal [6ads_po1](https://app.slack.com/client/T037C9B3UJ2/C0388PYU8C8).**
