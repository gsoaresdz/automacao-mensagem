# Automação de envio de Mensagens com o WhatsApp Web

Este projeto consiste em um script Python que automatiza o envio de mensagens para contatos do WhatsApp Web. O script utiliza as seguintes bibliotecas:

- **pandas:** para importar o arquivo Excel com os contatos e mensagens a serem enviadas.
- **selenium:** para controlar o navegador Chrome e interagir com o WhatsApp Web.
- **urllib:** para codificar a mensagem a ser enviada.

**IDE e versão do Python**

O script foi desenvolvido no Visual Studio Code com a versão 3.10.4 do Python.

**Regra de negócio**

O script funciona da seguinte forma:

1. Importa o arquivo Excel com os contatos e mensagens a serem enviadas.
2. Abre o WhatsApp Web no navegador Chrome.
3. Percorre o arquivo Excel, enviando uma mensagem para cada contato.
4. A mensagem é enviada na forma "Oi [nome]! [mensagem]".
5. O script aguarda 12 segundos entre cada envio para evitar que o WhatsApp bloqueie a conta.

**Passos executados no código**

O código é dividido em duas partes principais:

- Importação de Arquivo Excel
- Automação de Envio de Mensagens

**Importação de Arquivo Excel**

A primeira parte do código importa o arquivo Excel com os contatos e mensagens a serem enviadas. O arquivo deve ter as seguintes colunas:

- **Pessoa:** nome do contato.
- **Número:** número de telefone do contato.
- **Mensagem:** mensagem a ser enviada.

O código utiliza a biblioteca pandas para importar o arquivo Excel. O código a seguir mostra como importar o arquivo:

**Python**

```python
contatos_df = pd.read_excel(r"arquivos/Enviar.xlsx")
```

**Use code with caution. [Learn more](https://bard.google.com/faq#coding)content_copy**

**Automação de Envio de Mensagens**

A segunda parte do código automatiza o envio de mensagens para os contatos do arquivo Excel. O código funciona da seguinte forma:

1. Abre o WhatsApp Web no navegador Chrome.
2. Percorre o arquivo Excel, enviando uma mensagem para cada contato.
3. A mensagem é enviada na forma "Oi [nome]! [mensagem]".
4. O script aguarda 12 segundos entre cada envio para evitar que o WhatsApp bloqueie a conta.

O código a seguir mostra como enviar uma mensagem para um contato:

**Python**

```python
pessoa = contatos_df.loc[i, "Pessoa"]
numero = contatos_df.loc[i, "Número"]
texto = urllib.parse.quote(f"Oi {pessoa}! {mensagem}")
link = f"https://web.whatsapp.com/send?phone={numero}&text={texto}&/n"
navegador.get(link)
while
len(navegador.find_elements(By.ID, "pane-side")) < 1:
    time.sleep(1)
time.sleep(1)
navegador.find_element(By.XPATH, '//*[@id="main"]/footer/div[1]/div/span[2]/div/div[2]/div[2]/button/span').click()

```

**Use code with caution. [Learn more](https://bard.google.com/faq#coding)content_copy**

**Observações**

- O script foi desenvolvido para fins educacionais. Não é recomendado o uso do script para enviar mensagens em massa para contatos que não autorizaram o envio.
- O script pode ser modificado para atender a diferentes necessidades. Por exemplo, é possível alterar o intervalo de tempo entre os envios de mensagens ou incluir novas funcionalidades.
