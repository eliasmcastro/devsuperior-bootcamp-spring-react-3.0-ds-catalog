<h1 align="center">
  <img alt="Logo" src=".github/logo_devsuperior.svg"/>
</h1>

<h3 align="center">
  DsCatalog
</h3>

<p align="center">O DsCatalog é um projeto para catálogo de produtos</p>

<p align="center">
  <a href="#como-executar-o-projeto">Como executar o projeto</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#configurações-de-ferramentas">Configurações de Ferramentas</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#conteúdo-do-curso">Conteúdo do curso</a>
</p>

<p align="center">Back-end</p>

<p align="center">
  <img alt="Back-end" src=".github/backend.png" width="90%">
</p>

## Como executar o projeto

### Back-end

#### Requisitos

- [Java SDK 11](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) ou versões posteriores
- [Eclipse](https://www.eclipse.org/downloads/packages) / [IntelliJ IDEA](https://www.jetbrains.com/pt-br/idea) ou [Marven](https://maven.apache.org)

#### Opcional

- [Insomnia](https://insomnia.rest)

#### Passos para a configuração

**1. Clonar este repositório**

```bash
git clone https://github.com/eliasmcastro/devsuperior-bootcamp-spring-react-3.0-ds-catalog.git
```

**2. Executar aplicação**

Se for executar pelo Eclipse

- Abrir o Eclipse -> File -> Import -> Existing Marven Projects (clicar em Next) -> Selecionar a pasta back-end do projeto (clicar em Finish)
- Executar DscatalogApplication.java (src/com.devsuperior.dscatalog) para iniciar o back-end da aplicação

Se for executar pelo IntelliJ IDEA

- Abrir o IntelliJ IDEA -> File -> Open -> Selecionar a pasta back-end do projeto (clicar em OK)
- Executar DscatalogApplication.java (src/com.devsuperior.dscatalog) para iniciar o back-end da aplicação

Se for executar com o Maven

- Entrar na pasta back-end (pelo cmd/terminal)
- Executar os comandos abaixo para iniciar o back-end da aplicação

```bash
mvn clean install -U
```

```bash
mvn spring-boot:run
```

**3. Banco de Dados H2**

- O projeto está configurado para utilizar o banco de dados H2
  - Para acessá-lo
    - http://localhost:8080/h2-console
    - JSCB URL: jdbc:h2:mem:testdb
    - User Name: sa
    - Password:
- Ao executar a aplicação automaticamente as tabelas são criadas
- Alguns dados já são populados através do arquivo (src/main/resources/data.sql) 

O aplicativo começará a ser executado em http://localhost:8080

_Dica: utilizar o Insomnia para testar as rotas_

- Abrir o Insomnia -> Application -> Preferences -> Data -> Import Data -> From File -> Selecionar o arquivo insomnia.json que está na pasta back-end

### Front-end

- Em breve

## Configurações de Ferramentas

### Back-end

#### [Java SDK 11](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) no Windows

- Efetuar o download do executável de acordo com o seu sistema operacional
- _Obs: será necessário realizar um login (criar uma conta caso não possuir) para baixar_
- Realizar a instalação
- Configuar o caminho da instalação do Java nas variáveis de ambiente do Windows de acordo com esse [tutorial](https://medium.com/@mauriciogeneroso/configurando-java-4-como-configurar-as-vari%C3%A1veis-java-home-path-e-classpath-no-windows-46040950638f)

#### [Eclipse](https://www.eclipse.org/downloads/packages) / [IntelliJ IDEA](https://www.jetbrains.com/pt-br/idea)

- Eclipse
  - Efetuar o download do Eclipse. Recomenda-se utilizar a versão (package) Eclipse IDE for Enterprise Java Developers
  - Extrair o zip para uma pasta em seu computador
- IntelliJ IDEA
  - Efetuar o download do IntelliJ IDEA e realizar a instalação

#### [Maven](https://maven.apache.org)

- Realizar a instação e configuração do maven conforme esse [tutorial](https://www.devmedia.com.br/introducao-ao-maven/25128#2)

#### [Start Spring](https://start.spring.io)

- Este site [https://start.spring.io](https://start.spring.io) ajuda na criação de um novo projeto Spring Boot

#### [Insomnia](https://insomnia.rest)

- O Insomnia serve para testar a API
- Efetuar o download e realizar a instalação

### Front-end

#### [Node.js & NPM](https://nodejs.org)

- Uma sugestão para a instação do Node.js é realizar via [package manager](https://nodejs.org/en/download/package-manager) utilizando o Chocolatey no Windows
  - Instalar o [Chocolatey](https://chocolatey.org/install)
  - Executar `cinst nodejs-lts` para instalar o Node.js
  - Executar `node -v` e `npm -v` para verificar se a instalação deu certo

#### [Visual Studio Code](https://code.visualstudio.com)

- O Visual Studio Code é um editor de código-fonte
- Efetuar o download e realizar a instalação

## Conteúdo do curso

### Back-end

- CRUD (Java, Spring Boot, Maven, H2, Postgresql, Postman, Spring Data JPA)
  - Competências
    - Criar projeto Spring Boot
    - Criar monorepo Git
    - Organizar o projeto em camadas
    - Controlador REST
    - Serviço
    - Acesso a dados (Repository)
    - Criar entidades
    - Configurar perfil de teste do projeto
    - Seeding da base de dados
    - Criar web services REST
      - Parâmetros de rota @PathVariable
      - Parâmetros de requisição @RequestParam
      - Corpo de requisição @RequestBody
      - Resposta da requisição ResponseEntity<T>
    - Padrão DTO
    - CRUD completo
    - Tratamento de exceções
    - Postman/Insomnia (coleções, ambientes)
    - Dados de auditoria
    - Paginação de dados
    - Associações entre entidades (N-N)
  - Figma do DSCatalog
    - [Link](https://www.figma.com/file/1n0aifcfatWv9ozp16XCrq/DSCatalog-Bootcamp)
  - Modelo conceitual do DSCatalog
    - [Link](.github/modelo_dados.png)
- Testes automatizados (JUnit, Mockito, MockBean)
  - Competências
    - Fundamentos de testes automatizados
      - Tipos de testes
        - Unitário: Teste feito pelo desenvolvedor, responsável por validar o comportamento de unidades funcionais de código. Nesse contexto, entende-se como unidade funcional qualquer porção de código que através de algum estímulo seja capaz de gerar um comportamento esperado (na prática: métodos de uma classe). Um teste unitário não pode acessar outros componentes ou recursos externos (arquivos, bd, rede, web services, etc.).
        - Integração: Teste focado em verificar se a comunicação entre componentes / módulos da aplicação, e também recursos externos, estão interagindo entre si corretamente.
        - Funcional: É um teste do ponto de vista do usuário, se uma determinada funcionalidade está executando corretamente, produzindo o resultado ou comportamento desejado pelo usuário.
      - Benefícios
        - Detectar facilmente se mudanças violaram as regras
        - É uma forma de documentação (comportamento e entradas/saídas esperadas)
        - Redução de custos em manutenções, especialmente em fases avançadas
        - Melhora design da solução, pois a aplicação testável precisa ser bem delineada
      - TDD - Test Driven Development
        - É um método de desenvolver software. Consiste em um desenvolvimento guiado pelos testes.
        - Princípios / vantagens:
          - Foco nos requisitos
          - Tende a melhorar o design do código, pois o código deverá ser testável
          - Incrementos no projeto têm menos chance de quebrar a aplicação
        - Processo básico:
          - Escreva o teste como esperado (naturalmente que ele ainda estará falhando)
          - Implemente o código necessário para que o teste passe
          - Refatore o código conforme necessidade
      - Boas práticas e padrões
        - Nomenclatura de um teste
          - `<AÇÃO> should <EFEITO> [when <CENÁRIO>]`
        - Padrão AAA
          - Arrange: instancie os objetos necessários
          - Act: execute as ações necessárias
          - Assert: declare o que deveria acontecer (resultado esperado)
        - Princípio da inversão de dependência (SOLID)
          - Se uma classe A depende de uma instância da classe B, não tem como testar a classe A isoladamente. Na verdade nem seria um teste unitário.
          - A inversão de controle ajuda na testabilidade, e garante o isolamento da unidade a ser testada.
        - Independência / isolamento
          - Um teste não pode depender de outros testes, nem da ordem de execução
        - Cenário único
          - O teste deve ter uma lógica simples, linear
          - O teste deve testar apenas um cenário
          - Não use condicionais e loops
        - Previsibilidade
          - O resultado de um teste deve ser sempre o mesmo para os mesmos dados
          - Não faça o resultado depender de coisas que variam, tais como timestamp atual e valores aleatórios.
    - JUnit (Básico (vanilla), Spring Boot, Repositories, Services, Resources (web), Integração)
      - Visão geral
        - https://junit.org/junit5
        - O primeiro passo é criar uma classe de testes
        - A classe pode conter um ou mais métodos com a annotation `@Test`
        - Um método `@Test` deve ser void
        - O objetivo é que todos métodos `@Test` passem sem falhas
        - O que vai definir se um método `@Test` passa ou não são as “assertions” deste método
        - Se um ou mais falhas ocorrerem, estas são mostradas depois da execução do teste
      - Annotations usadas nas classes de teste
        - `@SpringBootTest`: Carrega o contexto da aplicação (teste de integração)
        - `@SpringBootTest` | `@AutoConfigureMockMvc`: Carrega o contexto da aplicação (teste de integração & web) | Trata as requisições sem subir o servidor
        - `@WebMvcTest(Classe.class)`: Carrega o contexto, porém somente da camada web (teste de unidade: controlador)
        - `@ExtendWith(SpringExtension.class)`: Não carrega o contexto, mas permite usar os recursos do Spring com JUnit (teste de unidade: service/component)
        - `@DataJpaTest`: Carrega somente os componentes relacionados ao Spring Data JPA. Cada teste é transacional e dá rollback ao final. (teste de unidade: repository)
      - Fixtures (É uma forma de organizar melhor o código dos testes e evitar repetições)
        - `@BeforeAll`: Preparação antes de todos testes da classe (método estático)
        - `@AfterAll`: Preparação depois de todos testes da classe (método estático)
        - `@BeforeEach`: Preparação antes de cada teste da classe 
        - `@AfterEach`: Preparação depois de cada teste da classe 
    - Mockito & MockBean (@Mock, @InjectMocks, Mockito.when / thenReturn / doNothing / doThrow, ArgumentMatchers, Mockito.verify, @MockBean, @MockMvc)
      
      - Usar quando a classe de teste não carrega o contexto da aplicação. É mais rápido e enxuto. `@ExtendWith`

        ```java
        @Mock
        private MyComp myComp;
        //ou
        myComp = Mockito.mock(MyComp.class);
        ```
      
      - Usar quando a classe de teste carrega o contexto da aplicação e precisa mockar algum bean do sistema. `@WebMvcTest` | `@SpringBootTest`
      
        ```java
        @MockBean
        private MyComp myComp;
        ```
- Validação e segurança (Bean Validation, Spring Security, JWT, OAuth2)
- Domínio e ORM, autorizações (Modelo de domínio, JPA, SQL seed)
- Consultas ao banco de dados (Spring Data JPA, JPQL, SQL)
- Docker, implantação, CI/CD (Maven, Docker, Docker Hub, Amazon EC2, Amazon RDS, Travis CI, Heroku)

### Front-end

- Layout e navegação (HTML, CSS, JavaScript, TypeScript, ReactJS, Bootstrap, React Router DOM)
- Integração com API (Axios, React Hooks, React Router DOM, loaders)
- Axios, React Hooks, React Router DOM, loaders (Autenticação e autorização, React Hook Form, UNIX timestamp)
- CRUD (React Hook Form, Axios)
- Testes, implantação, CI/CD (JEST, Netlify)
- Dashboards (Apex Charts)