# Airflow: Preparação do Ambiente

[← Voltar à Trilha de Airflow](https://github.com/joycequoos/Apache_Airflow./blob/main/README.md)

<!--
  Comentário: apliquei a mesma estrutura início/meio/fim usada no README do
  Apache_Airflow. O conteúdo original era uma sequência linear de imagens
  e comandos, sem separação clara de etapas — reorganizei em 3 blocos:
  o que você precisa antes de começar, o passo a passo de instalação, e
  a verificação final de que o ambiente está pronto.
-->

Este repositório documenta o passo a passo para preparar o ambiente local do Apache Airflow utilizando **Docker**.

---

## Pré-requisitos

Antes de instalar o Airflow, você vai precisar de:

- **Docker** instalado na máquina.
- Uma **IDE** de sua preferência (Anaconda / VS Code).

### Download do Docker para Windows

[![Download Docker para Windows](https://github.com/JosiTubaroski/Airflow_Preparar_Ambiente/raw/main/img/Docker_Windows.png)](https://github.com/JosiTubaroski/Airflow_Preparar_Ambiente/blob/main/img/Docker_Windows.png)

Para instalar o Airflow com Docker:

1. Crie uma pasta chamada `airflow`.
2. Salve os seguintes arquivos dentro dela:
   - `docker-compose.yaml`
   - `.env`

---

##  Instalando e subindo o ambiente

<!--
  Comentário: agrupei aqui todo o processo de instalação e execução dos
  comandos, que no README original estava misturado com o passo de
  pré-requisitos — assim fica mais claro que essa é a etapa "mão na massa".
-->

### 1. Instalando o Docker

[![Instalando o Docker](https://github.com/JosiTubaroski/Airflow_Preparar_Ambiente/raw/main/img/Instalando_Docker.png)](https://github.com/JosiTubaroski/Airflow_Preparar_Ambiente/blob/main/img/Instalando_Docker.png)

Aguarde o término da instalação.

📖 [Para saber mais sobre Docker](https://github.com/joycequoos/Docker)

### 2. Abrindo o prompt de comando na pasta do projeto

Após a instalação do Docker, abra o prompt de comando e posicione-se na pasta `airflow`.

[![Prompt de comando na pasta airflow](https://github.com/JosiTubaroski/Airflow_Preparar_Ambiente/raw/main/img/CMD_Airflow.png)](https://github.com/JosiTubaroski/Airflow_Preparar_Ambiente/blob/main/img/CMD_Airflow.png)

Depois de localizar o caminho da pasta, digite `dir` e verifique se o resultado é apresentado corretamente (os arquivos `docker-compose.yaml` e `.env` devem aparecer).

[![Verificando o diretório com dir](https://github.com/JosiTubaroski/Airflow_Preparar_Ambiente/raw/main/img/CMD_DIR.png)](https://github.com/JosiTubaroski/Airflow_Preparar_Ambiente/blob/main/img/CMD_DIR.png)

### 3. Subindo os containers

Execute o comando abaixo para iniciar a instalação:

```bash
docker-compose up -d
```

[![Término da execução](https://github.com/JosiTubaroski/Airflow_Preparar_Ambiente/raw/main/img/Termino_Execucao.png)](https://github.com/JosiTubaroski/Airflow_Preparar_Ambiente/blob/main/img/Termino_Execucao.png)

---

## Verificando o ambiente e primeiro acesso

### 1. Verificar se o ambiente está pronto

```bash
docker-compose ps
```

[![Verificando se o ambiente está pronto](https://github.com/JosiTubaroski/Airflow_Preparar_Ambiente/raw/main/img/Verificando_Se_AmbientePronto.png)](https://github.com/JosiTubaroski/Airflow_Preparar_Ambiente/blob/main/img/Verificando_Se_AmbientePronto.png)

### 2. Acessando a interface do Airflow

Com o ambiente pronto, abra o navegador e acesse:

```
localhost:8080
```

<!--
  Comentário: a imagem de login original usava um link temporário e
  assinado do GitHub (private-user-images.githubusercontent.com com token
  JWT), que expira depois de um tempo. Recomendo re-fazer o upload dessa
  imagem direto para a pasta /img do repositório e trocar por um link
  "raw" permanente, senão ela vai quebrar sozinha no futuro.
-->

Informe, tanto para usuário quanto para senha: `airflow`

### 3. Apresentação inicial do Airflow

[![Tela inicial do Airflow](https://github.com/JosiTubaroski/Airflow_Preparar_Ambiente/raw/main/img/Tela_Airflow.png)](https://github.com/JosiTubaroski/Airflow_Preparar_Ambiente/blob/main/img/Tela_Airflow.png)

Essa apresentação já contém as DAGs de demonstração que acompanham a instalação padrão do Airflow — um bom ponto de partida para explorar a interface antes de criar suas próprias DAGs.

➡️ **Próximo passo:** [Conhecendo o Airflow](https://github.com/JosiTubaroski/Conhecendo_Airflow)
