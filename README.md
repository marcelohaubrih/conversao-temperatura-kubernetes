# Projeto Desenvolvido em Aula

### - Compilando a imagem ( api-conversao )
``$ docker image build -t api-conversao:v1 src/. ``

### - Rodando a imagem em um container na porta 8080 ( CONVERSAO )
``$ docker run -d -p 8080:8080 --name CONVERSAO api-conversao:v1``

## <b>BOAS PRATICAS

- Sempre criar a imagem pelo Dockerfile para versionar suas imagens
- Sempre nomear suas imagens podronizadas com versionamento marcelohaubrih/api-conversão:v1 (namespace/repositorio:tag)
- Sempre dar preferência a imagens oficiais
- Sempre utilizar imagens bases versionadas para evitar que uma atualização de imagem base quebre sua aplicação
- Sempre utilizar 1 processo por container para não perder escabilidade
- Sempre utilizar o princípio das camadas para evitar execuções desnecessárias na geração de imagens
- Sempre fazer uso do .dockerignore para evitar copida de pastas e arquivos desnecessarios
- COPY vs ADD Sempre utilizar o COPY.
- Utilizar MultiStage Build em linguagens Compiladas para gerar imagens menores

