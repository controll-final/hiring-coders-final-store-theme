<h1 align="center">
    Bee in Controll Store Theme 🐝
</h1>

## 🔎 Índice de conteúdos

* [Sobre o Projeto](#-sobre-o-projeto)
    * [Concepção da Bee in Controll](#-concepção-da-bee-in-controll)
    * [Construção](#-construção)
    * [Construção do Layout](#-construção-do-layout)
    * [Loja VTEX](#-loja-vtex)
    * [Controll Suggestions Block](#-controll-suggestions-block)
* [Tecnologias e Ferramentas](#-tecnologias-e-ferramentas)
* [Executando](#-executando)
* [Back-End](#-back-end)
* [Abelhudo](#-abelhudo)
* [Desenvolvido Por](#-desenvolvido-por)
* [Atribuições](#-atribuições)
* [Preview](#-preview)


#
## 📝 Sobre o Projeto

### 📌 **Concepção da Bee in Controll**

 - A concepção do nome da loja Bee In Controll surgiu a partir de um trocadinho entre o nome Controll (casa designada a nosso grupo do Hiring Coders #3) e o abelha, animal que representa casa. Dito isto, buscamos construir uma identidade visual compatível com um grupo etário de jovens adultos que vem em sua vestimenta uma forma de expressar quem são e como gostariam de ser vistos pelo ambiente que os cercam.

> A Bee In Controll nasceu inspirada no incrível poder de transformação, criatividade e união das abelhas.
>E pensando nisso, queremos te incentivar a unir-se a nós para se libertar dos padrões, usando sua criatividade como meio da transformação para assim assumir o controle do seu estilo.
>Nossa missão é trazer liberdade através de roupas divertidas e criativas, feitas especialmente para adoçar sua vida. E antes que você se pergunte, não usamos mel na fabricação de nossas peças, haha.
>Acreditamos que estilo não é seguir tendências, mas sim um poder capaz de expressar um pouco da sua personalidade e da sua essência, vestindo o que te faz sentir bem e confortável. Então, por favor, vista-se de você!!
---
### 📌 **Construção**

- Para o projeto, foi utilizada a metodologia ágil **Kanban**.
- Página construída com base no projeto da semifinal, a qual subsequentmeente foi baseada no Store Theme - VTEX. 
- Construção do front-end segundo o protótipo construído no [Figma](https://www.figma.com/file/BhAeyEwi0T6o5koquYqDQu/HC-Final-Bee-In-Control).

### **O Front-End Possui:**

- Header com Menus: todos os links habilitados.
- Home:
    * Banners com CTA;
    * Carousel com coleções exclusivas;
    * Cards com CTA;
    * Carousel com marcas com link direcionável.
- Footer: 
    - Páginas específicas do site: Sobre Nós, Política de Privacidade, Termo de Uso, Política de Troca e Fale Conosco; 
    - Links de Redes Sociais da Loja Bee In Controll: Facebook, Instagram e Youtube.
- Página Search;
- Página de Produto:
    - Com o bloco Controll Suggestions Block incluso.
- Página Sobre Nós;
- Página Fale Conosco:
    * Imagens clicáveis que redirecionam para as respectivas páginas elucidadas em seu texto;
    * App VTEX customizado construído com React e Styled Components para o bloco de formulário.
- Página Política de Privacidade;
- Página Política de Troca;
- Página Termos de Uso;
- Customizações no bloco Minicart.
---
### 📌 **Construção do Layout**

- Foram criadas duas buyer-personas a partir das informações coletadas por meio de um formulário com questionário para conhecer o público-alvo de maneira mais profunda. Esses personagens ajudaram a manter a consistência da comunicação e identidade da marca durante o desenvolvimento da loja online;
- Identidade visual construída, com criação de logo e [cartela de cores](https://www.figma.com/file/BhAeyEwi0T6o5koquYqDQu/HC-Final-Bee-In-Control?node-id=4%3A150); 
- Criação de frases e CTAs para os banners do site, buscando manter o tom característico da marca, alinhado com a identidade visual;
- Criação e alimentação com vídeos e fotos para as redes sociais Bee In Controll. [Facebook](https://www.facebook.com/beeincontrolloficial/), [Instagram](https://www.instagram.com/beeincontrolloficial/), [Youtube](https://www.youtube.com/channel/UCCE6CP2paufxjkpABhynUag).
---
### 📌 **Loja VTEX**

- Nome da Loja alterado no CMS - /admin/cms/store
- Login Social habilitado para utilização -  admin/authentication
- Catálogo de Produtos:
    - Categoria: 
    - Marcas
    - Coleções
    - Produtos:
        * Todos os mockups de produtos foram construídos pela equipe.
        * Todos os produtos foram importados de forma nativa pela plataforma VTEX utilizando as funcionalidades do Admin. Importado: Cadastro, Imagem e Preço.
        * Todas as imagens foram convertidas para .jpg para melhor performance e seguindo a recomendação de melhores práticas da VTEX.
        * As imagens foram adicionados em repositório publico, Bucket S3 da AWS, para disponibilização da importação na VTEX: https://hc-controll.s3.amazonaws.com/product/{nomedaimagem.jpg}.
        * Foi adicionado estoque para todos os produtos.
}
---
### 📌 **Controll Suggestions Block**

### 🐝 Sobre o Bloco

- Aplicação para exibição das Sugestões Ativas pelo Admin da Bee In Controll Store.
- O bloco customizado foi inspirado no bloco Buy Together da VTEX, que faz o uso da Product Summary e do Add To Cart Button.


#
### 🐝 Preview

<img alt="Preview" title="#Preview" src="https://i.ibb.co/YjtDg3c/Anima-o.gif" />

#
### 🐝 Utilizando no Projeto

**1. Adicione `controll.product-suggestion-block` nas dependências do seu tema no `manifest.json`:**

```json
  "dependencies": {
    "controll.product-suggestion-block": "0.x"
  }
```
Agora, você pode usar todos os blocos exportados pelo aplicativo. Confira a lista abaixo:

| Bloco     | Descrição | 
| -------------- | ----------- | 
| [`buy-together-suggestions`] | Renderiza o Bloco de Compre Junto obtendo as Sugestões Ativas pelo Admin na API Controll Suggestions | 
| [`buy-together-custom`] | Customização do Bloco Buy Together VTEX para uso dos dados da API e permitir customização conforme necessidade do projeto | 

**2. Adicione o bloco `buy-together-suggestions` ao seu template e declare o `buy-together-custom` na sua lista de blocos. Também é possível adicionar um cabeçalho ao bloco de Sugestões através do `children`. Por exemplo:**

```json
{
  "buy-together-suggestions": {
    "blocks": ["buy-together-custom"],
    "children": ["flex-layout.row#section-title-buy-together"]
  },
```

**3. Também é possível customizar o bloco `product-summary` e `add-to-cart-button`, conforme exemplo:**

```json
{
  "buy-together-custom": {
    "blocks": ["product-summary.shelf#buy-together"],
    "props": {
      "BuyButton": "add-to-cart-button#buy-together"
    }
  },
```

---
#### 🐝 **Customização**

Para aplicar customizações de CSS neste e em outros blocos, siga as instruções fornecidas [aqui](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-using-css-handles-for-store-customization)

| CSS Handles |
| ----------- | 
| `buyTogetherContainer` | 
| `buyTogetherContent` | 
| `buyTogetherSuggestion` | 
| `buyTogetherIconPlus` | 
| `buyTogetherIconEqual` |
| `suggestionContainer` |
| `changeSuggestionContainer` |
| `changeSuggestionButton` |


#
## 🔧 Tecnologias e Ferramentas

As seguintes tecnologias/ferramentas foram usadas na construção do projeto:

- Layout: **Figma** (consulte o Layout [aqui](https://www.figma.com/file/BhAeyEwi0T6o5koquYqDQu/HC-Final-Bee-In-Control))
- Ferramenta de Controle: **Trello** (consulte [aqui](https://trello.com/invite/b/VbvHD6lF/bfb09d3906c305da45a50b58596367a4/controll-final-hc/))
- Armazenamento de arquivos: **Google Drive** (consulte [aqui](https://drive.google.com/drive/folders/1Y9ZXOOvD85fpLGHDKMcNzSFZE4bm_ZoB))
- Comunicação: Alinhamentos no **Gather**; **Slack** e **WhatsApp**
- Foi utilizada uma ferramenta **Gerador de documentos de pessoas (Nome, RG, CPF, CEP, Endereço, etc) - 4Devs** para utilizar dados fictícios para as compras realizadas.
- **VTEX IO**
- **Java**
- **Spring Boot**
- **Jakarta Persistence API (JPA) e Hibernate**
- **Spring Data JPA**
- **Spring Security**
- **Flyway**
- **MySQL**
- **Lombok**
- **React**
- **Typescript**
- **AWS EC2**
- **AWS S3**
#
## 🔨 Executando

```
- vtex login controll
- vtex use beein 
- vtex link
```
#

## 💻 Back-End

### API para Controle de Sugestão de Produtos

### 📝 Sobre a API
 - API para Controle de Sugestões de Produtos para futuras compras dos Clientes na Loja. A API obtém os novos pedidos da loja através do Order Feed v3 da VTEX, onde registra e armazena os dados relevantes para geração de combinações, que posteriormente podem ser ativadas/desativadas como sugestões válidas para os Clientes através do Admin da Loja.

---
### 🔧 Tecnologias e Ferramentas na API

As seguintes tecnologias/ferramentas foram usadas na construção da API:

- **Java**
- **Spring Boot**
- **Jakarta Persistence API (JPA) e Hibernate**
- **Spring Data JPA**
- **Spring Security**
- **Flyway**
- **MySQL**
- **Lombok**
- **AWS EC2**
- **AWS RDS**
---
#### 📌 **Características da Aplicação**

- **Migração de Bancos de Dados - Flyway**
- **Segurança com OAuth 2 - RFC 6749**
- **2 Escopos diferentes para autorização (ADMIN e STORE)**
  - ADMIN - Realiza todas as operações na API (Consultas de Produtos, Combinações, Ativação e Inativação de Combinações)
  - STORE - Realiza consultas de Combinações Ativas (Sugestões)
- **Especificação de Erros segue a Problem Details for HTTP APIs - RFC 7807**
- **Shallow Etags para redução de tráfego**
- **Documentação Open API 3** [aqui](https://hccontroll03.app.br/swagger-ui/index.html)

---
### 🔨 Executando a API

**1. Clone a Aplicação**

```bash
https://github.com/controll-final/controll-suggestions-api.git
```

**2. Instale o MySQL ou tenha uma instância disponível**

**3. Altere as Propriedades da Aplicação**

+ Abra o arquivo `src/main/resources/application.properties`

+ Altere as Seguintes Propriedades:
```
spring.datasource.url=(String de Conexão com o Banco de Dados - ex.: jdbc:mysql://localhost/suggestionsdb?createDatabaseIfNotExist=true&serverTimezone=UTC)
spring.datasource.username=
spring.datasource.password=

security.admin-id=(ID para uso do Admin)
security.admin-secret=(Secret para uso do Admin)

security.store-id=(ID para uso da Store)
security.store-secret=(Secret para uso da Store)

security.jwt-signin-key=(Chave para assinatura dos Tokens - ex.: 89a7sd89f7as98f7dsa98fds7fd89sasd9898asdf98p)

vtex.api.vtex-account-name=(Nome da Conta VTEX)
vtex.api.vtex-environment=(Nome Environment API VTEX)
vtex.api.vtex-app-key=(App Key API VTEX)
vtex.api.vtex-app-token=(App Token API VTEX)
```

**4. Faça o build e execute a aplicação utilizando o maven**

```bash
mvn package
java -jar target/controll-suggestions-api-1.0.0.jar

```

Como alternativa, você pode executar o aplicativo sem empacotá-lo usando -

```bash
mvn spring-boot:run
```

A Aplicação iniciará em <http://localhost:8080>.

#

## 📌 **Abelhudo**

### 🐝 Sobre o Bloco

- Bloco que possibilita ao logista, por meio da admin, visualizar as combinações geradas pela API de combinação de produtos e ativa-las.
- 
### 🐝 Preview

<img alt="Preview" title="#Preview" src="https://i.ibb.co/6BykbpN/Anima-o.gif" />

#
### 🐝 Utilizando no Projeto

- **1. Acesse o admin de sua loja e clique em Abelhudo:**

- **Selecione o produto desejado e decida, através do toggle, se deseja ou não apresentar as combinações sugeridas associadas a ele**.


#
## 💪🏻 Desenvolvido por

- [Alessandra Buzios](https://www.linkedin.com/in/alessandra-buzios/)
- [Allysson Fernando](https://www.linkedin.com/in/allyssonalmeida/)         
- [Andressa Santana](https://www.linkedin.com/mwlite/in/andressa-santana-9a9431236)             
- [Cristiane dos Santos Costa](https://www.linkedin.com/in/cristianedsc/)
- [Douglas Rodrigues](https://www.linkedin.com/in/douglas-rodrigues-pnz/)
- [Fernando Beça](https://www.linkedin.com/in/fernando-beca/)
- [Igor Santos](https://www.linkedin.com/in/igor-santos-5740b3116/)
- [Leona Evangelista](https://www.linkedin.com/in/leona-evangelista/)
- [Rômulo Rosa](https://www.linkedin.com/in/romulofrontend/)
- [Suélen Dias](https://www.linkedin.com/in/su%C3%A9len-dias-palhares-2aa47573/)

#
## 👥 Atribuições

- **Squad Leader**: Suélen Dias
- **UI/UX**: Alessandra Buzios; Igor Santos
- **Mockups**: Igor Santos
- **Back-end**: Douglas Rodrigues
- **Front-end**: Allysson Fernando; Cristiane dos Santos Costa; Leona Evangelista; Rômulo Rosa; Douglas Rodrigues; Suélen Dias
- **Admin Loja Vtex**: Suélen Dias, Fernando Beça, Andressa Santana
- **Marketing**: Cristiane dos Santos Costa; Leona Evangelista e Alessandra
- **Documentação**: Suélen Dias; Leona Evangelista; Douglas Rodrigues

#
## 📸 Preview

<img alt="Preview" title="#Preview" src="https://i.ibb.co/mTzvH6r/Home-Desktop.png" />


