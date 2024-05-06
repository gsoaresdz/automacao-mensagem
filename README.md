&#xa0;

<h1 align="center">Automação de envio de Mensagens com o WhatsApp Web</h1>

<p align="center">
  <img alt="Github top language" src="https://img.shields.io/github/languages/top/gsoaresdz/automacao-mensagem?color=56BEB8">

  <img alt="Github language count" src="https://img.shields.io/github/languages/count/gsoaresdz/automacao-mensagem?color=56BEB8">

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/gsoaresdz/automacao-mensagem?color=56BEB8">

  <img alt="License" src="https://img.shields.io/github/license/gsoaresdz/automacao-mensagem?color=56BEB8">

</p>


<p align="center">
  <a href="#dart-sobre">Sobre</a> &#xa0; | &#xa0; 
  <a href="#sparkles-features">Features</a> &#xa0; | &#xa0;
  <a href="#rocket-tecnologias">Tecnologias</a> &#xa0; | &#xa0;
  <a href="#white_check_mark-requerimentos">Requerimentos</a> &#xa0; | &#xa0;
  <a href="#checkered_flag-execução">Execução</a> &#xa0; | &#xa0;
  <a href="https://github.com/gsoaresdz" target="_blank">Autor</a>
</p>

<br>

## :dart: Sobre

Este projeto consiste em um script Python que automatiza o envio de mensagens para contatos do WhatsApp Web. O script utiliza as seguintes bibliotecas:

- **pandas:** para importar o arquivo Excel com os contatos e mensagens a serem enviadas.
- **selenium:** para controlar o navegador Chrome e interagir com o WhatsApp Web.
- **urllib:** para codificar a mensagem a ser enviada.

## :memo: IDE e versão do Python

O script foi desenvolvido no Visual Studio Code com a versão 3.10.4 do Python.

## :memo: Regra de negócio

O script funciona da seguinte forma:

1. Importa o arquivo Excel com os contatos e mensagens a serem enviadas.
2. Abre o WhatsApp Web no navegador Chrome.
3. Percorre o arquivo Excel, enviando uma mensagem para cada contato.
4. A mensagem é enviada na forma "Oi [nome]! [mensagem]".
5. O script aguarda 12 segundos entre cada envio para evitar que o WhatsApp bloqueie a conta.

## :memo: Passos executados no código

O código é dividido em duas partes principais:

- Importação de Arquivo Excel
- Automação de Envio de Mensagens

## :memo: Importação de Arquivo Excel

A primeira parte do código importa o arquivo Excel com os contatos e mensagens a serem enviadas. O arquivo deve ter as seguintes colunas:

- **Pessoa:** nome do contato.
- **Número:** número de telefone do contato.
- **Mensagem:** mensagem a ser enviada.

O código utiliza a biblioteca pandas para importar o arquivo Excel. O código a seguir mostra como importar o arquivo:

```python
contatos_df = pd.read_excel(r"arquivos/Enviar.xlsx")
```

## :sparkles: Features

A segunda parte do código automatiza o envio de mensagens para os contatos do arquivo Excel. O código funciona da seguinte forma:

:heavy_check_mark: **Feature 1**: Abre o WhatsApp Web no navegador Chrome.\
:heavy_check_mark: **Feature 2**: Percorre o arquivo Excel, enviando uma mensagem para cada contato.\
:heavy_check_mark: **Feature 3**: A mensagem é enviada na forma "Oi [nome]! [mensagem]".\

O código a seguir mostra como enviar uma mensagem para um contato:

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

## :rocket: Tecnologias

As seguintes ferramentas foram usadas neste projeto:

- [Python](https://www.python.org/)
- [Jupyter](https://jupyter.org/)
- [Anaconda](https://www.anaconda.com/)

## :white_check_mark: Requerimentos

Antes de iniciar :checkered_flag:, você precisa ter [Git](https://git-scm.com) e [Python](https://www.python.org/) instalado.

## :checkered_flag: Execução

```bash
# Clone do projeto

$ git clone https://github.com/gsoaresdz/automacao-mensagem.git
```

## :memo: Observações

- O script foi desenvolvido para fins educacionais. Não é recomendado o uso do script para enviar mensagens em massa para contatos que não autorizaram o envio.
- O script pode ser modificado para atender a diferentes necessidades. Por exemplo, é possível alterar o intervalo de tempo entre os envios de mensagens ou incluir novas funcionalidades.

## :memo: Licença

Este projeto está sob licença do MIT. Para obter mais detalhes, consulte o arquivo [LICENSE](LICENSE).

Feito com :heart: by <a href="https://github.com/gsoaresdz" target="_blank">gsoaresdz</a>

&#xa0;

<a href="#top">De volta ao topo</a>
