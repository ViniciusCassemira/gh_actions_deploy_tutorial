# Github Actions Deploy Tutorial

Trago nesse repositório um exemplo de como usar o Github Actions para integração com algumas ferramentas como **Dockerhub** e **AWS**:

### Fluxo:
- Um push com mudanças é feito na branch **main**
- O GitHub Actions monitora automaticamente o repositório e, quando detecta um push na branch **main**, ativa o workflow definido no arquivo ```.github/workflows/deploy.yml```, executando a **pipeline** com  seus 2 jobs
- O 1º Job é o **Build**, sendo  responsável por criar imagem e publicar no Dockerhub
- já o 2º Job **(Deploy)** se conecta em um servidor na AWS via SSH, e executa comandos para parar o container atual da aplicação (caso exista), baixar a imagem atualizada direto do Dockerhub e a executa, atualizando assim o servidor.

## Conceitos usados:
- **Pipeline:** Um conjunto automatizado de processos sequenciais que transformam código fonte em aplicação deployada, incluindo etapas como build, teste, validação e deployment. Facilita a integração e entrega contínua (CI/CD) ao automatizar tarefas repetitivas no ciclo de desenvolvimento.
- **Docker e Dockerhub:** Docker é uma plataforma de containerização que empacota aplicações com suas dependências em containers portáteis e isolados. Dockerhub é o registro público onde desenvolvedores compartilham e distribuem imagens Docker pré-construídas.
- **AWS e Cloud:** AWS (Amazon Web Services) é uma plataforma de computação em nuvem que oferece diversos serviços, sendo computação sob demanda um exemplo. Cloud computing permite acesso remoto a recursos computacionais sem necessidade de infraestrutura física local.

## Tutorial:
Em breve farei um vídeo no Youtube recriando esse tutorial, explicando cada etapa e o porquê daquilo.