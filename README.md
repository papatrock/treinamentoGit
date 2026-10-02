# Configuração da chave SSH

O SSH permite autenticar no Bitbucket usando um par de chaves, sem precisar informar usuário e senha a cada operação.

O par é composto por:

Chave privada: fica na sua máquina e nunca deve ser compartilhada.
Chave pública: pode ser cadastrada no Bitbucket.

## Gerar chave ssh

Abra o terminal e execute:

```bash
$ ssh-keygen
```

O comando irá fazer algumas perguntas:

`Enter file in which to save the key (/home/user.name/.ssh/id_ed25519):`

Esse é o local onde a chave será salva. Pressione Enter para utilizar o local padrão.

Depois:

`Enter passphrase for "/home/user.name/.ssh/id_ed25519" (empty for no passphrase):`

Aqui é possível definir uma senha adicional para proteger a chave privada.

Para o treinamento, caso não queira utilizar uma senha, basta pressionar Enter. Em seguida, pressione Enter novamente quando a senha for solicitada pela segunda vez.

Ao final, serão criados dois arquivos:

```
~/.ssh/id_ed25519
~/.ssh/id_ed25519.pub
```

**Atenção:** nunca envie ou compartilhe o arquivo id_ed25519. Ele é sua chave privada. O arquivo que deve ser cadastrado no Bitbucket é o id_ed25519.pub.

O primeiro é a chave privada e o segundo é a chave pública.

Para visualizar a chave pública, execute:

`$ cat ~/.ssh/id_ed25519.pub`

Será exibida uma linha semelhante a:

```
ssh-ed25519 AAAABBBBBBBBBBBBCCCCCCCCC12345AAAAILG+asdjkqwoieuwertasdlçaks user.name@sim123
```

Copie a linha inteira, desde ssh-ed25519 até o final.

## Adicionando a chave ao Github

Agora precisamos informar ao Github qual é a nossa chave pública.

No Gihub, acesse o menu de configurações, localizado no canto superior direito.

<img width="289" height="650" alt="image" src="https://github.com/user-attachments/assets/bad4e663-6b1a-4d42-a26b-beb6996feaac" />

No menu lateral, acesse SSH and GPG keys

<img width="435" height="891" alt="image" src="https://github.com/user-attachments/assets/a61ac607-e65b-4793-a933-41f809cd95c2" />

Na tela de SSH Keys, clique em New SSH key para cadastrar uma nova chave.

<img width="1305" height="220" alt="image" src="https://github.com/user-attachments/assets/ec839858-33f8-4e72-91fe-0aa14a5e5fcf" />

Preencha os campos:

* **Title:** um nome para identificar a chave. Por exemplo: Notebook Simepar.

* **Key type**: Authentication key

* **Key:** cole aqui a chave pública copiada anteriormente com o comando cat ~/.ssh/id_ed25519.pub.

Depois de preencher os campos, salve a chave em **Add SSH key**.

<img width="1057" height="550" alt="image" src="https://github.com/user-attachments/assets/b831c8b1-063c-4c51-a486-7765288945d9" />


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
