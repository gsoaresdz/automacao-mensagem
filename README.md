# **Automação de Envio de Mensagens com o WhatsApp Web**

Este projeto é uma aplicação Python que utiliza a biblioteca Selenium para automatizar o envio de mensagens através do WhatsApp Web. Ele lê informações de contato e mensagens de um arquivo Excel e envia mensagens para os contatos especificados.

## **Requisitos**

- Python 3.x
- Bibliotecas: pandas, selenium
- Google Chrome
- WebDriver do Chrome (de acordo com a versão do navegador)

## **Instalação**

1. Clone o repositório:

```
git clone https://github.com/yourusername/whatsapp-web-automation.git
```

2. Instale as bibliotecas necessárias:

```
pip install pandas selenium
```

3. Baixe o WebDriver do Chrome aqui e coloque-o no diretório do projeto ou em um diretório listado no PATH do sistema.

```
pip install pandas selenium
```

## **Uso**

1. Crie um arquivo Excel chamado **`Enviar.xlsx`** no formato abaixo:

```
| Pessoa | Número          | Mensagem       |
|--------|-----------------|----------------|
| Maria  | 5511xxxxxxxxx   | Olá, tudo bem? |
| João   | 5511xxxxxxxxx   | Bom dia!       |
```
