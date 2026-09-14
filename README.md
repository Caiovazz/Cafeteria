# Cafeteria
Landing page estática de uma cafeteria desenvolvida para praticar conceitos e ferramentas de DevOps, incluindo Git, GitHub, Docker e CI/CD.
## Funcionalidade 
O projeto Caferia foi desenvolvido  com foco na apresentacão e organizacão do layout do Café.

Entre as principais funcionalidae estão:

-Organização das imformações na Cafeteria;
-Estrutura preparadas para futuras melhoras;
-Integração Continua em prática.



🎯 Objetivo

A empresa CodeFactory Solutions foi contratada para desenvolver e manter a página web da "Cafeteria CodeFactory".  

Problema: A equipe da CodeFactory não tinha padronização de ambiente, gerava conflitos de código e demorava para publicar atualizações no site do cliente.  

Solução DevOps: Como consultoria, você implementou o repositório organizado no GitHub, o empacotamento da página em container Docker com servidor Nginx e a automação de testes com GitHub Actions.

O objetivo do projeto é desenvolver uma aplicação web simples utilizando HTML e CSS e utilizar esse projeto como laboratório para praticar conceitos e ferramentas de DevOps, como:

Controle de versão com Git;
Organização de um repositório no GitHub;
Branches e Pull Requests;
Integração contínua (CI);
Containerização com Docker;
Servidor web Nginx;
Automação de processos;
Deploy da aplicação.

🛠️ Tecnologias utilizadas
HTML5 — estrutura da página;
CSS3 — estilização e layout;
Git — controle de versão;
GitHub — hospedagem do código e colaboração;
Docker — containerização da aplicação;
Nginx — servidor web;
GitHub Actions — automação do pipeline de CI/CD.

## 📁 Estrutura do Projeto

```text
Cafeteria/
│
├── .github/
│   └── workflows/
│       └── pipeline.yml
│
├── CSS/
│   └── style.css
│
├── .dockerignore
├── .gitignore
├── .stylelintrc.json
├── Dockerfile
├── index.html
├── LICENSE
└── README.md

Descrição dos principais arquivos
Arquivo/Pasta	Descrição
.github/workflows/	Contém a configuração da pipeline de Integração Contínua
CSS/style.css	Arquivo responsável pela estilização da página
index.html	Página principal da aplicação
Dockerfile	Define a configuração utilizada para criar a imagem Docker
.dockerignore	Define arquivos que não devem ser enviados para o contexto de build do Docker
.gitignore	Define arquivos que não devem ser versionados pelo Git
.stylelintrc.json	Configuração das regras de validação do CSS
LICENSE	Arquivo contendo os termos da licença do projeto
README.md	Documentação principal do projeto

🔀 Pull Requests
Os Pull Requests são utilizados para organizar a integração das alterações entre as branches.
Antes de uma alteração ser incorporada à branch principal, ela pode ser revisada e validada por meio do processo de Pull Request.
Esse processo contribui para:
- Revisão do código;
- Redução de erros;
- Organização do desenvolvimento;
- Registro das alterações;
- Integração controlada entre branches.
🐳 Docker
Por que utilizar Docker?
A containerização foi utilizada para padronizar o ambiente de execução da aplicação.
Como o projeto é uma aplicação web estática, o Docker permite executar os arquivos HTML e CSS dentro de um container contendo o servidor web Nginx.
Dessa forma, não é necessário configurar manualmente um servidor web no computador para executar a aplicação.
A utilização de containers também reduz problemas relacionados a diferenças entre ambientes de desenvolvimento e execução.
📦 Construindo a imagem Docker
Para criar a imagem da aplicação, execute na pasta raiz do projeto:
docker build -t cafeteria .
O comando cria uma imagem chamada cafeteria utilizando as instruções definidas no Dockerfile.

▶️ Executando o container
Depois de criar a imagem, execute:
docker run -d -p 8080:80 --name cafeteria-container cafeteria
O container ficará disponível na porta 8080 do computador.
A aplicação pode ser acessada pelo navegador através de:
http://localhost:8080

🔎 Verificando o container
Para verificar os containers em execução:
docker ps
Para visualizar também containers que foram encerrados:
docker ps -a

⏹️ Encerrando o container
Para parar o container:
docker stop cafeteria-container
Para iniciar novamente:
docker start cafeteria-container
Caso seja necessário remover o container:
docker rm cafeteria-container

⚙️ Integração Contínua
O projeto utiliza GitHub Actions para automatizar a validação do código.
A configuração da pipeline está localizada em:
.github/workflows/pipeline.yml
A pipeline realiza verificações automáticas nos arquivos do projeto.
Entre as ferramentas utilizadas estão:
- HTML-Validate, para validação dos arquivos HTML;
- Stylelint, para validação dos arquivos CSS.

🔄 Funcionamento da Pipeline
O fluxo de Integração Contínua pode ser representado da seguinte forma:
Alteração no código
       ↓
     Git
       ↓
     Push
       ↓
   GitHub
       ↓
GitHub Actions
       ↓
Validação HTML
       ↓
Validação CSS
       ↓
Validação Do container
  Resultado da Pipeline
Dessa forma, alterações enviadas ao repositório podem ser verificadas automaticamente, ajudando a identificar problemas antes da integração do código.
💻 Instalação e Execução Local
Pré-requisitos
Para executar o projeto diretamente no computador, é necessário possuir:
- Git;
- Um navegador web.
Para executar utilizando Docker:
- Docker Desktop ou Docker Engine.
Clonando o repositório
Clone o projeto utilizando:
git clone URL_DO_REPOSITORIO
Entre na pasta do projeto:
cd Cafeteria
Execução sem Docker
Como a aplicação é baseada em HTML e CSS, também é possível executá-la diretamente pelo navegador.
Basta abrir o arquivo:
index.html
Execução utilizando Docker
Na pasta raiz do projeto:
docker build -t cafeteria .
Depois:
docker run -d -p 8080:80 --name cafeteria-container cafeteria
Acesse:
http://localhost:8080

📌 Controle de Versão
O projeto utiliza Git para controle de versão.
Entre os principais comandos utilizados durante o desenvolvimento estão:
git init
Inicialização do repositório Git.
git add .
Adição das alterações para a área de preparação.
git commit -m "mensagem do commit"
Criação de um commit com as alterações.
git push
Envio das alterações para o repositório remoto.
git pull

Atualização do repositório local com alterações do repositório remoto.
📊 Recursos do GitHub
Além do controle de versão, o projeto utiliza recursos disponibilizados pelo GitHub para organização e acompanhamento do desenvolvimento.
Entre eles:
- Issues — registro e acompanhamento de tarefas e problemas;
- Milestones — organização de tarefas por objetivos;
- Labels — categorização das Issues;
- Wiki — documentação complementar do projeto;
- Projects — organização visual das atividades;
- Insights — acompanhamento de informações e métricas do repositório.
Esses recursos contribuem para uma organização mais profissional do desenvolvimento.

🧪 Validação
A validação automática dos arquivos é realizada pela pipeline de Integração Contínua.
O HTML é analisado utilizando o:
HTML-Validate
E os arquivos CSS são analisados utilizando:
Stylelint
O objetivo é detectar problemas de estrutura e padronização automaticamente.

📸 Evidências
Durante a elaboração do projeto foram realizadas evidências das etapas de desenvolvimento, incluindo:
- Repositório no GitHub;
- Estrutura de branches;
- Commits;
- Pull Requests;
- Integração das branches;
- Pipeline do GitHub Actions;
- Container Docker em execução;
- Aplicação sendo acessada através do Nginx.
As capturas de tela dessas etapas fazem parte do relatório da atividade.

📄 Licença
Este projeto possui uma licença definida no arquivo LICENSE.
👨‍💻 Autor
Caio Vaz e Leticia Holanda
Projeto desenvolvido para fins acadêmicos na disciplina de DevOps e Integração Contínua.
