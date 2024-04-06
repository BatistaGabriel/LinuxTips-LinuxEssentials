# [Linux Essentials](https://www.linuxtips.io/course/linux-essentials)

## Descrição

O treinamento foi elaborado para ajudar estudantes e profissionais de Linux a se prepararem para atuar no mercado de trabalho de forma efetiva, fornecendo os conhecimentos necessários para lidar com as demandas e desafios do mundo profissional. Além disso, o curso visa preparar o aluno para o exame Linux Essentials, que é um importante certificado para quem deseja comprovar suas habilidades em sistemas Linux.

## Instrutores

- [Jeferson Fernando](https://nl.linkedin.com/in/jefersonfernando)
- [Gleydson Mazioli](https://br.linkedin.com/in/gleydsonmazioli)

## Carga Horária

11 horas

---

## Acesso via SSH

Para acessar alguma máquina remotamente podemos utilizar o utilitátio do open-ssh. Podemos realizar isso através do seguinte comando:

```bash
ssh user@192.168.0.22
```

Na seguinte estruruta estamos indicando ao utilitário `ssh` que vamos a conexão remota será realizada no destino `192.168.0.22` (caso tenha o DNS do destino é possível se conectar através dele também) com o usuário `user`.

Uma estrutura não muito complexa de se entender não é mesmo? Um ponto importante é o `@`, ele necessário ser informado para que o utilitário saiba o qual usuário irá se conectar em qual destino.

Ao executar este comando, sempre nas primeras vezes de qualquer destino, será perguntado se você deseja salvar o fingerprint daquele destino, basta confirmar com `y` ou `n`.

Após aceito o fingerprint, será necessário (a depender da configuração do usuário no destino)informar a senha da máquina e após isto você estará agora interagindo com o shell da máquina destino.

## Simbologia do Terminal

Vamos falar das possíveis coisas que você verá no terminal a primeira vez que acessar — tenha em mente que estaremos falando de como as coisas estão, sem terem sido customizadas.

### Identificação de Usuário

Assim como na sintaxe que utilizamos para acessar uma máquina via ssh, seu terminal terá também um indicativo de qual usuário está naquela instância do terminal e qual o destino, portanto você verá algo como:

```bash
gandalf@mordor:~$
```

### Identificação de Diretório

Ainda vendo mais detalhes sobre as informações do terminal, podemos ver que logo após do indicativo de `usuário@destino` temos logo após os `:` o nosso diretório atual.

Neste nosso caso estamos no diretório principal do usuário atual, que é representado por `~`.

### Identificação de Nível de Permissão

Continuando podemos ver que temos ainda a indicação do nosso nível de permissão dentro daquela instância do terminal, o que nos indica isso é o caracter `$`.

Quando você estiver vendo o caracter `$` isto indica a você que seu usuário não é root, por tanto algumas operações podem requerem que seja solicitada a elevação de privilégios para este usuário.

Caso você entre em um terminal e esteja vendo o caracter `#` ao invés de `$`, saiba que as coisas tendem a ser perigosas, pois, você está acessando o terminal como o usuário root.

## Comandos Úteis

Vamos ver alguns comando que podem ser úteis no seu dia a dia interagindo com o terminal de comandos do Linux.

### pwd

Vamos começar com o comando `pwd`, este comando irá te retornar qual o seu diretório atual completo.

### su -

Temos também o comando `su -`, este comando indica ao Linux que querem trocar para o usuário administrador (nosso famoso super user, sudo, admin, o bichão da montanha, etc). E o `-` indica que nós vamos também trocar para o ambiente de trabalho do usuário root.

### cd

Para navegar entre diretórios, nos podemos fazer isto atráves do comando `cd caminho`, ou seja, caso eu queria mudar do meu diretório atual para meu diretório de trabalho eu posso executar o seguinte comando:

```bash
cd /home/gandalf/workspace
```

### 
