# TreinamentoGit

## Clonar o projeto

Para começar o treinamento, primeiro faça uma cópia local do repositório utilizando o comando git clone.

No Github, acesse o repositório do treinamento e clique no botão <> Code:

<img width="963" height="233" alt="image" src="https://github.com/user-attachments/assets/954278c4-9b01-4a44-8504-cc2ee8482e96" />


O Github permite clonar o repositório utilizando SSH ou HTTPS. Neste treinamento utilizaremos SSH, por exigir menos configuração inicial.

Caso a opção exibida seja HTTPS, altere para SSH:

<img width="465" height="376" alt="image" src="https://github.com/user-attachments/assets/10d6857f-d89f-4206-909b-770d9292b932" />


O Github exibirá o comando git clone já pronto para ser copiado:

<img width="480" height="375" alt="image" src="https://github.com/user-attachments/assets/5f731cc2-a756-4ef3-b5da-9a6a813a4ea9" />


O comando terá um formato semelhante a:

```
git clone https://<seu-usuario>@github.org/treinamentogit.git
```

Abra o Git Bash ou outro terminal com Git disponível, navegue até a pasta onde deseja salvar o projeto e execute o comando copiado.

O git clone irá baixar o repositório e todo o seu histórico para sua máquina, criando uma pasta chamada treinamentogit.

Após finalizar o clone, entre na pasta do projeto:

```bash
cd treinamentogit
```


Você pode confirmar que está dentro do repositório executando:

```
git status
```

Se o clone foi realizado corretamente, o Git mostrará o estado atual do repositório e a branch em que você está.
