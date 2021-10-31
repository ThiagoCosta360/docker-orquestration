# Setup linux

## Clonagem dos repositórios

> **OBS** Para a clonagem recursiva funcionar é necessário salvar a chave ssh pública no git lab

```
git clone --recursive https://gitlab.com/plataforma_cognitiva/computer-vision/sidi/security-chat-camera/services/scc-services-orchestrator.git
```

## Instalação das dependencias

```
sudo ./scc-services-orchestrator/linux-setup.sh
```

## Run containers

- Flags

  > - **CREATE_DB** Inicializa o banca de dados pela ORM.
  > - **POPULATE_DB** Insere os dados default do banco de dados. Deve ser utilizada somente se o banco estiver vazio.

- Primeira execução

```
CREATE_DB=1 POPULATE_DB=1 docker-compose up --build
```

- Execução com o banco criado

```
docker-compose up
```
