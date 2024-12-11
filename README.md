# Publicação de Aplicação Angular no GitHub Pages

## Configuração no angular.json
Certifique-se de que a configuração do outputPath no arquivo angular.json esteja apontando para o diretório docs:

` "outputPath": "docs" `

## Passo 1: Instalar o angular-cli-ghpages
Primeiro, instale a ferramenta angular-cli-ghpages globalmente usando o npm:

` npm i -g angular-cli-ghpages `

## Passo 2: Build da Aplicação
Em seguida, gere os arquivos de build da sua aplicação Angular com a configuração de produção e configure o caminho base para o seu repositório no GitHub Pages:

` ng build --configuration production --base-href="/[your-repo-name]/" `

Substitua [your-repo-name] pelo nome do seu repositório no GitHub.

## Passo 3: Fazer o Deploy com angular-cli-ghpages
Utilize o comando abaixo para fazer o deploy dos arquivos gerados no diretório dist para o GitHub Pages:

` npx angular-cli-ghpages --dir=docs/browser `

Substitua [app-name] pelo nome da sua aplicação.

## Passo 4: Configurar o GitHub Pages
*Vá para o repositório no GitHub que deseja publicar.
Navegue até Settings > Pages.
Em Build and deployment, selecione Deploy from a branch.
Troque o caminho /root para /docs.
Clique em Save.
O projeto estará disponível no GitHub Pages em alguns minutos.*

**Configuração de Domínio Próprio**
O GitHub Pages permite que você utilize o domínio [seu-usuário].github.io de forma gratuita. Para configurar um domínio próprio

Vá para a página do repositório no GitHub e clique em Settings.
Role até a sessão GitHub Pages.
Na opção Custom Domain, informe o domínio que deseja utilizar e clique em Save.
Apontamento de DNS

Para que o domínio próprio funcione, é necessário configurar o DNS para apontar para os servidores do GitHub. Adicione os seguintes registros DNS na configuração do seu domínio:

*Nome:* @
*Valor:* 185.199.108.153
*TTL:* 3600
*Tipo:* A

*Nome:* @
*Valor:* 185.199.109.153
*TTL:* 3600
*Tipo:* A

*Nome:* @
*Valor:* 185.199.110.153
*TTL:* 3600
*Tipo:* A

*Nome:* @
*Valor:* 185.199.111.153
*TTL:* 3600
*Tipo:* A
