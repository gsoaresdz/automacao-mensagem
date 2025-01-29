<h1 align="center">Automated Message Sending with WhatsApp Web</h1>

<p align="center">
  <img alt="Github top language" src="https://img.shields.io/github/languages/top/gsoaresdz/automated-message?color=56BEB8">

  <img alt="Github language count" src="https://img.shields.io/github/languages/count/gsoaresdz/automated-message?color=56BEB8">

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/gsoaresdz/automated-message?color=56BEB8">

  <!--<img alt="License" src="https://img.shields.io/github/license/gsoaresdz/automacao-mensagem?color=56BEB8">-->

</p>

<p align="center">
  <a href="#dart-about">About</a> &#xa0; | &#xa0; 
  <a href="#sparkles-features">Features</a> &#xa0; | &#xa0;
  <a href="#rocket-technologies">Technologies</a> &#xa0; | &#xa0;
  <a href="#white_check_mark-requirements">Requirements</a> &#xa0; | &#xa0;
  <a href="#checkered_flag-execution">Execution</a> &#xa0; | &#xa0;
  <a href="#memo-license">License</a> &#xa0; | &#xa0;
  <a href="https://github.com/gsoaresdz" target="_blank">Author</a>
</p>

<br>

## :dart: About

This project consists of a Python script that automates sending messages to contacts on WhatsApp Web. The script uses the following libraries:

- **pandas:** to import the Excel file containing contacts and messages to be sent.
- **selenium:** to control the Chrome browser and interact with WhatsApp Web.
- **urllib:** to encode the message before sending.

## :memo: IDE and Python Version

The script was developed using Visual Studio Code with Python version 3.10.4.

## :memo: Business Logic

The script works as follows:

1. Imports an Excel file containing contacts and messages to be sent.
2. Opens WhatsApp Web in the Chrome browser.
3. Iterates through the Excel file, sending a message to each contact.
4. The message is sent in the format: "Hi [name]! [message]".
5. The script waits 12 seconds between each message to prevent WhatsApp from blocking the account.

## :memo: Steps Executed in the Code

The code is divided into two main parts:

- Importing an Excel File
- Automating Message Sending

## :memo: Importing an Excel File

The first part of the code imports an Excel file containing the contacts and messages to be sent. The file should have the following columns:

- **Person:** contact's name.
- **Number:** contact's phone number.
- **Message:** message to be sent.

The code uses the pandas library to import the Excel file. The following snippet demonstrates how to import the file:

```python
contatos_df = pd.read_excel(r"arquivos/Enviar.xlsx")
```

## :sparkles: Features

The second part of the code automates the sending of messages to the contacts listed in the Excel file. The code functions as follows:

:heavy_check_mark: **Feature 1**: Opens WhatsApp Web in the Chrome browser.

:heavy_check_mark: **Feature 2**: Iterates through the Excel file, sending a message to each contact.

:heavy_check_mark: **Feature 3**: Sends the message in the format: "Hi [name]! [message]".\

The following snippet demonstrates how a message is sent to a contact:

```python
pessoa = contatos_df.loc[i, "Pessoa"]
numero = contatos_df.loc[i, "Número"]
texto = urllib.parse.quote(f"Hi {pessoa}! {mensagem}")
link = f"https://web.whatsapp.com/send?phone={numero}&text={texto}&/n"
navegador.get(link)
while len(navegador.find_elements(By.ID, "pane-side")) < 1:
    time.sleep(1)
time.sleep(1)
navegador.find_element(By.XPATH, '//*[@id="main"]/footer/div[1]/div/span[2]/div/div[2]/div[2]/button/span').click()
```

## :rocket: Technologies

The following tools were used in this project:

- [Python](https://www.python.org/)
- [Jupyter](https://jupyter.org/)
- [Anaconda](https://www.anaconda.com/)

## :white_check_mark: Requirements

Before starting :checkered_flag:, you need to have [Git](https://git-scm.com/) and [Python](https://www.python.org/) installed.

## :checkered_flag: Execution

```bash
# Clone the project

$ git clone https://github.com/gsoaresdz/automacao-mensagem.git
```

## :memo: Notes

- This script was developed for educational purposes. It is not recommended to use the script for mass messaging to contacts who have not authorized receiving messages.
- The script can be modified to meet different needs. For example, you can change the time interval between message sending or add new functionalities.

## :memo: License

This project is licensed under the MIT License. For more details, check the [LICENSE](LICENSE file.

Made with :heart: by <a href="https://github.com/gsoaresdz" target="_blank">gsoaresdz</a>

<a href="#top">Back to top</a>
