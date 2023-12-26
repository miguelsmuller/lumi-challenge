# Teste Desenvolvedor Full Stack - Lumi

O objetivo deste repositório é organizar e gerenciar os projetos relacionados em um único local, facilitando o desenvolvimento, teste e implantação de ambos os projetos.

Este monorepo contém dois projetos relacionados: 

- **[Monorepo Lumi Challenge](https://github.com/miguelsmuller/lumi-challenge)**
  
- **[Lumi Extraction](https://github.com/miguelsmuller/lumi-extraction)**

- **[Lumi Back](https://github.com/miguelsmuller/lumi-back)**

- **[Lumi Front](https://github.com/miguelsmuller/lumi-front)**


## **Estrutura de Submódulos**

Para manter a organização e o versionamento centralizados, este monorepo usa submódulos para incluir os projetos relacionados. Isso permite que você mantenha um histórico de controle de versão compartilhado e mantenha as dependências entre os componentes de maneira consistente.


### **Clonando o Monorepo com Submódulos**

Ao clonar este monorepo, certifique-se de incluir os submódulos para garantir que todos os componentes sejam baixados corretamente:

```shell
git clone --recurse-submodules <monorepo_URL>
```


### **Atualização de Submódulos**

Para atualizar um submódulo específico a partir deste repositório principal, você pode usar os seguintes comandos:

```shell
git submodule update --remote <submodule_name>
ou
git submodule update --remote --recursive
```

Isso trará as últimas mudanças do repositório _<submodule_name>_ e as incorporará no repositório principal.


### **Envio de Alterações nos Submódulos para o Servidor Remoto**

Lembre-se de que ao fazer `git add ...` e `git commit` no monorepo, você está apenas registrando as alterações nos submódulos no histórico do repositório principal. Para enviar as alterações dos submódulos aos seus respectivos repositórios remotos, é necessário executar o comando git push diretamente dentro do diretório do submódulo.


## **Docker Compose**

O arquivo `docker-compose.yml` incluído neste repositório descreve a configuração de um ambiente Docker para executar os projetos. Ele define dois serviços:


### **Serviço Invoice Back**

Este serviço é o `Invoice Back`, que se conecta à Invoice API e fornece uma interface do usuário para listar e gerenciar transações.

- Nome do contêiner: lumi-invoice-back
- Porta exposta: ???
- Variáveis de ambiente:
  - ???: ???


### **Serviço Invoice Front**

Este serviço é o `Invoice Front`, que se conecta à Invoice API e fornece uma interface do usuário para listar e gerenciar transações.

- Nome do contêiner: lumi-invoice-front
- Porta exposta: ???
- Variáveis de ambiente:
  - ???: ???


## **Makefile**

Esse projeto possui um Makefile associado para simplificar tarefas comuns de desenvolvimento e inclui as seguinte metas :

- `run`: Inicia o ambiente especificado no docker-compose.yml subindo os container `Invoice Back` e `Invoice Front`
