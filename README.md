# Documentação técnica — Desenvolvimento Web: Front-end, Ferramentas e Back-end

## 1. Visão geral

O vídeo apresenta uma introdução prática ao **desenvolvimento web**, organizada em etapas que vão dos conceitos fundamentais de front-end até uma visão geral de back-end e da publicação de sites simples.

O conteúdo visual percorre:

1. O que é desenvolvimento web
2. Front-end básico
3. Ferramentas de desenvolvimento
4. Front-end adicional
5. Back-end básico
6. Publicação de sites simples
7. Exemplo de formulário de contato

O vídeo alterna entre slides explicativos, imagens ilustrativas, navegador, editor de código e exemplos de projetos.

---

## 2. Objetivos de aprendizagem

Ao estudar o conteúdo deste vídeo, o leitor deve ser capaz de:

- distinguir **front-end** de **back-end**;
- entender o papel de **HTML, CSS e JavaScript**;
- reconhecer a função de um navegador na execução de aplicações web;
- compreender por que ferramentas de desenvolvimento fazem parte do fluxo profissional;
- identificar conceitos como **gerenciamento de pacotes**, **Git**, **merge**, **responsividade** e **frameworks/bibliotecas**;
- reconhecer a relação entre servidor, linguagem de programação e banco de dados;
- diferenciar aplicações web tradicionais de arquiteturas **serverless**;
- compreender, em nível introdutório, como um site simples pode ser publicado;
- relacionar um formulário de contato ao fluxo de front-end e back-end.

---

# 3. O que é Desenvolvimento Web

Desenvolvimento web é o conjunto de práticas utilizadas para criar, executar, manter e disponibilizar sites e aplicações acessíveis por meio da web.

De forma simplificada, uma aplicação web pode ser vista como uma cadeia:

```text
Usuário
   ↓
Navegador
   ↓
Interface / Front-end
   ↓
Requisições HTTP
   ↓
Back-end / APIs
   ↓
Banco de dados e outros serviços
```

Nem toda aplicação utiliza todos esses componentes da mesma forma. Um site puramente estático, por exemplo, pode funcionar apenas com HTML, CSS e JavaScript no navegador.

## 3.1 O navegador

O navegador é o ambiente no qual o usuário visualiza e interage com a interface web.

Entre suas responsabilidades estão:

- interpretar HTML;
- aplicar CSS;
- executar JavaScript;
- realizar requisições de rede;
- renderizar a interface;
- armazenar determinados dados locais;
- fornecer APIs para funcionalidades do ambiente web.

Exemplos de navegadores incluem Chrome, Firefox, Edge e Safari.

---

# 4. Front-end × Back-end

Uma das distinções centrais apresentadas no vídeo é:

```text
FRONT-END
Interface, interação e experiência executadas principalmente no cliente

BACK-END
Processamento, regras de negócio, APIs, persistência e serviços executados no servidor
```

## 4.1 Front-end

O front-end é a parte da aplicação com a qual o usuário interage diretamente.

Tecnologias fundamentais:

| Tecnologia | Função |
|---|---|
| HTML | Estrutura e semântica do conteúdo |
| CSS | Apresentação, layout e aparência |
| JavaScript | Comportamento, lógica e interatividade |

### Exemplo conceitual

```html
<button>Enviar</button>
```

O HTML cria o elemento.

```css
button {
  padding: 10px 16px;
}
```

O CSS define sua apresentação.

```js
button.addEventListener("click", () => {
  console.log("Botão acionado");
});
```

O JavaScript acrescenta comportamento.

> Os exemplos acima são exemplos didáticos equivalentes aos conceitos apresentados; não devem ser tratados como transcrição literal do código exibido no vídeo.

---

# 5. HTML — estrutura da página

O vídeo mostra um documento HTML básico no editor.

A estrutura fundamental de um documento HTML pode ser representada assim:

```html
<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8">
    <meta
      name="viewport"
      content="width=device-width, initial-scale=1.0"
    >
    <title>Documento</title>
  </head>

  <body>
    <!-- conteúdo -->
  </body>
</html>
```

## 5.1 Elementos importantes

### `<!DOCTYPE html>`

Informa ao navegador que o documento utiliza HTML moderno.

### `<html>`

Elemento raiz do documento.

### `<head>`

Contém metadados, título, links para estilos e outras informações que não correspondem diretamente ao conteúdo visual principal.

### `<meta charset="UTF-8">`

Define a codificação de caracteres.

### `<meta name="viewport">`

É importante para a correta adaptação da página em dispositivos móveis.

### `<title>`

Define o título do documento apresentado pelo navegador.

### `<body>`

Contém o conteúdo que será apresentado na página.

---

# 6. CSS — apresentação e layout

O vídeo apresenta exemplos de CSS e de organização de estilos.

CSS é usado para controlar:

- cores;
- tipografia;
- espaçamento;
- dimensões;
- posicionamento;
- bordas;
- imagens de fundo;
- responsividade;
- animações e transições;
- composição visual dos componentes.

Um exemplo visualmente simples:

```css
body {
  margin: 0;
  font-family: sans-serif;
}

button {
  padding: 10px 16px;
  border-radius: 6px;
}
```

## 6.1 Variáveis e organização de estilos

Em um dos trechos de código são mostradas variáveis de estilo, incluindo referências a fontes como **Roboto** e **Fira Code**, além de uma função auxiliar para conversão de valores para `rem`.

A ideia de centralizar valores permite manter consistência e facilitar alterações futuras.

Exemplo conceitual:

```scss
$font-primary: "Roboto", sans-serif;
$font-secondary: "Fira Code", monospace;

@function rem($number) {
  @return $number / 16 * 1rem;
}
```

> O trecho acima é uma representação didática baseada no código visível; a sintaxe exata exibida no vídeo pode diferir.

---

# 7. JavaScript

JavaScript é a linguagem utilizada no navegador para implementar comportamento e lógica.

Pode ser usado para:

- responder a eventos;
- modificar o DOM;
- validar formulários;
- realizar requisições;
- consumir APIs;
- atualizar componentes;
- implementar regras de interface;
- criar aplicações completas no navegador.

## 7.1 JavaScript no ecossistema moderno

O vídeo associa o JavaScript a ferramentas e tecnologias utilizadas no desenvolvimento moderno, mostrando que ele não está limitado a pequenos scripts dentro de páginas HTML.

O ecossistema pode envolver:

```text
JavaScript
├── navegador
├── Node.js
├── gerenciadores de pacotes
├── ferramentas de build
├── bibliotecas
└── frameworks
```

---

# 8. Ferramentas de desenvolvimento

A etapa de ferramentas apresenta o ambiente utilizado pelo desenvolvedor para criar e manter projetos.

Entre os conceitos visualmente abordados estão:

- editor de código;
- terminal;
- gerenciamento de arquivos;
- controle de versão;
- gerenciamento de dependências;
- ferramentas de build;
- servidor de desenvolvimento;
- navegador para testes.

## 8.1 Editor de código

O vídeo utiliza um ambiente de edição semelhante ao **Visual Studio Code**, mostrando:

- árvore de arquivos;
- edição de código;
- terminal integrado;
- comandos;
- arquivos de projeto.

Um bom editor facilita:

- navegação;
- autocomplete;
- refatoração;
- depuração;
- integração com Git;
- execução de comandos.

---

# 9. Gerenciamento de pacotes

O vídeo apresenta visualmente o conceito de **Package Manager**.

Um gerenciador de pacotes automatiza a instalação e manutenção de dependências de um projeto.

Exemplo conceitual:

```text
Projeto
├── código próprio
├── dependência A
├── dependência B
└── dependência C
```

Em vez de instalar manualmente cada biblioteca, o projeto declara suas dependências e o gerenciador cuida da resolução e instalação.

## 9.1 Por que isso é importante?

Gerenciadores de pacotes ajudam a:

- instalar bibliotecas;
- atualizar dependências;
- reproduzir o ambiente do projeto;
- controlar versões;
- executar scripts;
- compartilhar projetos com outros desenvolvedores.

No ecossistema JavaScript, exemplos comuns incluem npm, Yarn e pnpm.

---

# 10. Ferramentas de build

O vídeo mostra representações de ferramentas relacionadas ao processo de construção do projeto, incluindo **Webpack** e **Gulp**.

Ferramentas de build podem executar tarefas como:

- agrupar arquivos;
- transformar código;
- otimizar recursos;
- processar CSS;
- reduzir tamanho de arquivos;
- gerar artefatos para produção;
- automatizar tarefas repetitivas.

## 10.1 Desenvolvimento × produção

Um fluxo típico:

```text
Código-fonte
    ↓
Ferramentas de build
    ↓
Arquivos processados
    ↓
Servidor / hospedagem
    ↓
Usuário
```

---

# 11. Git e controle de versão

Em outro trecho, o vídeo apresenta o conceito de **Git** e destaca `git merge`.

Git é um sistema distribuído de controle de versão.

Ele permite registrar alterações e trabalhar com diferentes linhas de desenvolvimento.

## 11.1 Conceitos essenciais

- **repository** — repositório do projeto;
- **commit** — registro de uma alteração;
- **branch** — linha independente de desenvolvimento;
- **merge** — integração das alterações de uma branch em outra;
- **remote** — repositório remoto;
- **clone** — cópia de um repositório;
- **pull** — obtenção de alterações remotas;
- **push** — envio de alterações.

## 11.2 Fluxo simplificado

```text
main
 │
 ├── feature/login
 │       │
 │       ├── commit
 │       ├── commit
 │       └── commit
 │
 └── merge ───────────→ main
```

O uso de controle de versão é especialmente importante em equipes, pois permite rastrear mudanças e colaborar com segurança.

---

# 12. Responsividade

O vídeo também apresenta dispositivos móveis e diferentes gerações de celulares, reforçando a necessidade de desenvolver interfaces que funcionem em diferentes tamanhos de tela.

## 12.1 Design responsivo

Uma interface responsiva adapta seu layout ao espaço disponível.

Conceitualmente:

```text
Desktop
┌───────────────────────────────┐
│ menu │ conteúdo │ conteúdo     │
└───────────────────────────────┘

Mobile
┌───────────────┐
│ menu          │
├───────────────┤
│ conteúdo      │
│ conteúdo      │
└───────────────┘
```

Recursos frequentemente utilizados:

- unidades relativas;
- Flexbox;
- CSS Grid;
- media queries;
- imagens flexíveis;
- layouts fluidos.

---

# 13. Bibliotecas e frameworks de front-end

O vídeo mostra exemplos do ecossistema JavaScript moderno e apresenta, visualmente, tecnologias como **React** e **Vue**.

## 13.1 React

React é utilizado para construir interfaces baseadas em componentes.

O vídeo mostra um exemplo de componente de botão com propriedades e `children`.

A estrutura conceitual é:

```jsx
const Button = ({ children, ...props }) => {
  return (
    <button {...props}>
      {children}
    </button>
  );
};
```

O componente pode então ser reutilizado:

```jsx
<Button>
  Enviar
</Button>
```

### Vantagens do modelo de componentes

- reutilização;
- composição;
- separação de responsabilidades;
- manutenção facilitada;
- padronização visual.

---

## 13.2 Vue

O vídeo também apresenta **Vue** como parte do ecossistema de desenvolvimento front-end.

Assim como outras soluções modernas, Vue oferece mecanismos para construção de interfaces componentizadas e aplicações interativas.

A escolha entre tecnologias deve considerar:

- requisitos do projeto;
- experiência da equipe;
- ecossistema;
- manutenção;
- desempenho;
- integração com ferramentas existentes.

---

# 14. Front-end adicional

Após os fundamentos, o vídeo amplia o escopo para tecnologias e práticas adicionais.

Entre os elementos visíveis estão:

- componentes;
- frameworks/bibliotecas;
- organização de estilos;
- ferramentas de desenvolvimento;
- controle de versão;
- responsividade;
- automação;
- build.

A progressão pode ser resumida:

```text
HTML
 ↓
CSS
 ↓
JavaScript
 ↓
Git + Package Manager
 ↓
Build tools
 ↓
Componentes
 ↓
React / Vue
 ↓
Aplicações mais complexas
```

---

# 15. Back-end básico

A partir de aproximadamente 11 minutos, o vídeo muda o foco para **BACK END**.

O slide apresenta três elementos centrais:

```text
SERVER
   +
LANGUAGE
   +
DATABASE
```

Esses componentes representam uma visão simplificada de uma aplicação de servidor.

## 15.1 Servidor

O servidor recebe requisições e executa operações necessárias para atender ao cliente.

Exemplo:

```text
Browser
   │
   │ HTTP request
   ▼
Server
   │
   ├── regra de negócio
   ├── autenticação
   ├── validação
   └── acesso a dados
```

---

# 16. Linguagens de back-end

O vídeo mostra exemplos de linguagens/tecnologias associadas ao back-end, incluindo visualmente:

- PHP;
- JavaScript;
- C#.

O importante é compreender que a linguagem é uma escolha de implementação do servidor. Diferentes linguagens podem oferecer recursos adequados a diferentes projetos e equipes.

Exemplos de ecossistemas possíveis:

```text
PHP
JavaScript / Node.js
C#
Python
Java
Go
Ruby
```

A escolha não deve ser feita apenas pela popularidade da linguagem, mas pelo contexto técnico do projeto.

---

# 17. Banco de dados

O banco de dados é responsável por armazenar informações que precisam persistir.

Exemplos conceituais:

```text
Usuários
Produtos
Pedidos
Mensagens
Configurações
```

Uma aplicação pode consultar, inserir, atualizar ou excluir dados.

## 17.1 Fluxo típico

```text
Cliente
  ↓
API
  ↓
Back-end
  ↓
Banco de dados
  ↓
Back-end
  ↓
Resposta HTTP
  ↓
Cliente
```

Esse padrão permite separar a interface das regras de negócio e da persistência.

---

# 18. Serverless

O vídeo apresenta o conceito de **SERVERLESS**.

Serverless não significa que não existam servidores. Significa que a infraestrutura de servidores é abstraída do desenvolvedor em maior grau e normalmente administrada por um provedor de nuvem.

Uma arquitetura serverless pode utilizar:

- funções sob demanda;
- serviços gerenciados;
- armazenamento;
- bancos de dados gerenciados;
- APIs;
- autenticação.

Benefícios potenciais:

- menor necessidade de administrar servidores;
- escalabilidade automática em determinados cenários;
- cobrança baseada em uso em alguns serviços;
- integração rápida com serviços de nuvem.

Também existem trade-offs, como dependência do provedor, limites de execução, latência inicial em algumas arquiteturas e maior complexidade de observabilidade em determinados sistemas.

---

# 19. AWS e serviços de nuvem

O vídeo apresenta visualmente a **AWS** associada ao conceito de serverless.

A Amazon Web Services oferece serviços de infraestrutura e plataforma que podem ser usados para:

- hospedar aplicações;
- executar funções;
- armazenar arquivos;
- fornecer bancos de dados;
- disponibilizar APIs;
- monitorar aplicações;
- controlar identidade e acesso.

A ideia central para o iniciante é:

```text
Aplicação
   ↓
Serviços de nuvem
   ↓
Infraestrutura administrada pelo provedor
```

---

# 20. Sites simples

Na parte final, o vídeo apresenta o conceito de **sites simples**.

Um site simples pode não exigir uma arquitetura de aplicação complexa.

Por exemplo:

```text
HTML
CSS
JavaScript
   ↓
Build opcional
   ↓
Hospedagem
```

Exemplos de projetos que podem ser adequados a esse modelo:

- página institucional;
- landing page;
- portfólio;
- documentação;
- página de apresentação;
- site informativo.

Quando não existe necessidade de processamento de servidor, uma solução estática pode reduzir custo e complexidade.

---

# 21. Ambiente local e servidor de desenvolvimento

O vídeo mostra uma execução local com endereços semelhantes a:

```text
http://localhost:3000
```

e referências a um servidor de desenvolvimento.

`localhost` representa o próprio computador do desenvolvedor.

Portas diferentes permitem que diferentes serviços sejam executados simultaneamente.

Exemplo:

```text
localhost:3000 → aplicação
localhost:3001 → outro serviço
```

## 21.1 Por que usar servidor local?

Um servidor local permite:

- testar a aplicação;
- observar alterações rapidamente;
- simular o ambiente web;
- verificar requisições;
- depurar problemas antes da publicação.

---

# 22. Publicação e transferência de arquivos

O vídeo mostra uma etapa relacionada à disponibilização de um site, incluindo uma interface de transferência/gerenciamento de arquivos.

O conceito geral é:

```text
Computador do desenvolvedor
          │
          │ arquivos
          ▼
Servidor de hospedagem
          │
          ▼
       Internet
          │
          ▼
       Usuário
```

Dependendo do provedor e da arquitetura, a publicação pode ocorrer por:

- FTP/FTPS;
- SSH/SFTP;
- Git;
- pipelines de CI/CD;
- plataformas de hospedagem;
- serviços de armazenamento estático.

---

# 23. Formulário de contato

O vídeo termina apresentando uma interface de **Formulário de Contato**, com campos como:

- Nome;
- E-mail;
- Mensagem;
- botão de envio.

Um formulário é um excelente exemplo para conectar front-end e back-end.

## 23.1 Fluxo completo

```text
Usuário preenche formulário
          ↓
Front-end valida os dados
          ↓
POST /contato
          ↓
Back-end recebe a requisição
          ↓
Validação no servidor
          ↓
Processamento / armazenamento / envio
          ↓
Resposta HTTP
          ↓
Interface informa o resultado
```

## 23.2 Validação

A validação deve ocorrer no cliente para melhorar a experiência do usuário, mas **nunca deve depender exclusivamente da validação no navegador**.

O servidor deve validar novamente os dados recebidos.

Exemplo de regras:

```text
Nome:
- obrigatório
- tamanho aceitável

E-mail:
- obrigatório
- formato válido

Mensagem:
- obrigatória
- tamanho máximo
```

---

# 24. Segurança de formulários

Em uma implementação real, o formulário deve considerar:

- validação de entrada;
- proteção contra spam;
- rate limiting;
- autenticação quando necessário;
- proteção contra ataques de injeção;
- proteção de credenciais;
- HTTPS;
- tratamento adequado de erros;
- armazenamento seguro.

Nunca se deve confiar cegamente em dados enviados pelo navegador.

---

# 25. Arquitetura resumida

Os conceitos do vídeo podem ser reunidos em uma arquitetura didática:

```text
                         INTERNET
                            │
                            ▼
                    ┌──────────────┐
                    │   Browser    │
                    └──────┬───────┘
                           │
                           │ HTTP/HTTPS
                           ▼
                    ┌──────────────┐
                    │  Front-end   │
                    │ HTML/CSS/JS  │
                    └──────┬───────┘
                           │
                           │ API
                           ▼
                    ┌──────────────┐
                    │   Back-end   │
                    │   Server     │
                    └──────┬───────┘
                           │
             ┌─────────────┴─────────────┐
             ▼                           ▼
      ┌─────────────┐             ┌─────────────┐
      │ Banco de    │             │ Serviços de │
      │ dados       │             │ nuvem       │
      └─────────────┘             └─────────────┘
```

---

# 26. Fluxo de desenvolvimento recomendado

Com base nos conceitos apresentados, um fluxo inicial de aprendizagem pode ser:

```text
1. HTML
   ↓
2. CSS
   ↓
3. JavaScript
   ↓
4. Git
   ↓
5. Package Manager
   ↓
6. Responsividade
   ↓
7. Build tools
   ↓
8. React ou Vue
   ↓
9. APIs
   ↓
10. Back-end
   ↓
11. Banco de dados
   ↓
12. Deploy
```

---

# 27. Checklist do iniciante

## Fundamentos

- [ ] Sei o que é desenvolvimento web.
- [ ] Sei diferenciar front-end e back-end.
- [ ] Sei criar um documento HTML.
- [ ] Sei aplicar CSS.
- [ ] Conheço JavaScript básico.
- [ ] Sei usar o navegador para testar uma página.

## Ferramentas

- [ ] Sei usar um editor de código.
- [ ] Sei usar o terminal.
- [ ] Entendo o que é um package manager.
- [ ] Sei o que é Git.
- [ ] Entendo branch e merge.
- [ ] Sei por que ferramentas de build existem.

## Front-end moderno

- [ ] Entendo componentes.
- [ ] Conheço React ou Vue.
- [ ] Sei construir layouts responsivos.
- [ ] Sei trabalhar com formulários.
- [ ] Sei consumir uma API.

## Back-end

- [ ] Entendo o papel de um servidor.
- [ ] Sei o que é uma API.
- [ ] Entendo o conceito de banco de dados.
- [ ] Sei diferenciar processamento no cliente e no servidor.
- [ ] Conheço o conceito de serverless.

## Publicação

- [ ] Sei o que significa `localhost`.
- [ ] Entendo o processo de deploy.
- [ ] Sei diferenciar desenvolvimento local de produção.
- [ ] Conheço formas de enviar/publicar arquivos.

---

# 28. Glossário pesquisável

| Termo | Definição curta |
|---|---|
| API | Interface que permite comunicação entre sistemas |
| Back-end | Camada responsável por processamento, regras e serviços no servidor |
| Banco de dados | Sistema para persistência e consulta de informações |
| Branch | Linha independente de desenvolvimento em Git |
| Browser | Aplicação usada para acessar e executar conteúdo web |
| Build | Processo de transformar/preparar o projeto para execução ou distribuição |
| CSS | Linguagem de estilos utilizada para apresentação de documentos web |
| Deploy | Processo de disponibilizar uma aplicação em um ambiente |
| DOM | Representação da estrutura do documento manipulável pelo JavaScript |
| Front-end | Camada da aplicação voltada à interface e interação |
| Git | Sistema de controle de versão distribuído |
| HTML | Linguagem de marcação usada para estruturar páginas web |
| HTTP | Protocolo usado para comunicação entre cliente e servidor |
| JavaScript | Linguagem de programação amplamente utilizada na web |
| localhost | Endereço que representa o computador local |
| Merge | Operação que integra alterações entre branches |
| Node.js | Ambiente de execução JavaScript fora do navegador |
| Package Manager | Ferramenta para instalar e administrar dependências |
| React | Biblioteca/ecossistema para construção de interfaces com componentes |
| Responsive Design | Abordagem para adaptar interfaces a diferentes telas |
| Serverless | Modelo em que a infraestrutura de servidores é abstraída do desenvolvedor |
| SFTP | Protocolo seguro para transferência de arquivos |
| Vue | Framework progressivo para construção de interfaces |
| Webpack | Ferramenta de empacotamento/build do ecossistema web |
| Gulp | Ferramenta de automação de tarefas |
| AWS | Plataforma de serviços de computação em nuvem |

---

# 29. Linha do tempo do vídeo

| Tempo aproximado | Conteúdo |
|---|---|
| 00:00–00:30 | Introdução e apresentação das etapas |
| 00:30–01:30 | Desenvolvimento web e distinção front-end/back-end |
| 01:30–03:00 | Conceitos introdutórios e exemplos visuais |
| 03:00–04:00 | Introdução prática ao código |
| 04:00–05:30 | HTML e CSS |
| 05:30–06:30 | Ambiente de desenvolvimento |
| 06:30–08:00 | Ferramentas, package manager e build |
| 08:00–09:00 | Git, merge e responsividade |
| 09:00–10:30 | Front-end moderno e componentes |
| 10:30–11:30 | Ecossistema de frameworks/bibliotecas |
| 11:30–12:30 | Back-end: servidor, linguagem e banco |
| 12:30–13:00 | Sites simples |
| 13:00–14:00 | Ambiente/publicação e transferência |
| 14:00–14:45 | Formulário de contato e encerramento |

> Os tempos são aproximados, obtidos pela inspeção do conteúdo visual do vídeo.

---

# 30. Relações entre os principais conceitos

## HTML → CSS → JavaScript

```text
HTML       = estrutura
CSS        = apresentação
JavaScript = comportamento
```

## Git → colaboração

```text
Código
 ↓
Commit
 ↓
Branch
 ↓
Merge
 ↓
Projeto integrado
```

## Package Manager → dependências

```text
Projeto
 ↓
package.json / manifesto
 ↓
Package Manager
 ↓
Dependências
```

## Front-end → Back-end

```text
Interface
 ↓
HTTP request
 ↓
API
 ↓
Regra de negócio
 ↓
Banco de dados
 ↓
HTTP response
 ↓
Interface
```

---

# 31. Pontos técnicos importantes

### 31.1 Cliente e servidor têm responsabilidades diferentes

Não é recomendável colocar toda a lógica no navegador. Regras críticas e validações de segurança devem ser verificadas no servidor.

### 31.2 JavaScript não é somente front-end

JavaScript pode ser executado fora do navegador, como no Node.js, permitindo sua utilização em aplicações de servidor e ferramentas.

### 31.3 Framework não substitui fundamentos

React, Vue e outras ferramentas facilitam a construção de aplicações, mas não eliminam a necessidade de compreender:

- HTML;
- CSS;
- JavaScript;
- HTTP;
- navegador;
- acessibilidade;
- segurança;
- arquitetura.

### 31.4 Site simples não significa site mal construído

Uma aplicação estática pode ser tecnicamente excelente quando seus requisitos não exigem banco de dados ou processamento de servidor.

### 31.5 Serverless não elimina a infraestrutura

A infraestrutura continua existindo; a principal diferença é que uma parte maior da administração fica sob responsabilidade do provedor.

---

# 32. Síntese final

O vídeo apresenta uma visão geral do desenvolvimento web partindo dos fundamentos e avançando para um ecossistema profissional.

A ideia central pode ser resumida em:

```text
DESENVOLVIMENTO WEB
│
├── FRONT-END
│   ├── HTML
│   ├── CSS
│   ├── JavaScript
│   ├── Responsividade
│   ├── Componentes
│   └── React / Vue
│
├── FERRAMENTAS
│   ├── Editor
│   ├── Terminal
│   ├── Package Manager
│   ├── Build tools
│   └── Git
│
└── BACK-END
    ├── Servidor
    ├── Linguagem
    ├── API
    ├── Banco de dados
    ├── Serverless
    └── Nuvem
```

O exemplo de formulário de contato funciona como uma síntese prática: a interface é construída no front-end, os dados podem ser enviados por HTTP para um back-end e o servidor pode validar, processar, armazenar ou encaminhar essas informações.

---

**`Informática para Internet`**

O suporte fornecido por corporações permite-nos o desenvolvimento e implementação de programas, projetos e recursos para Eduardo.Inf.Br. Através dessas parcerias é possível que empreendedores e proprietários de pequenas empresas, recebam ampla variedade de conteúdos e ferramentas por meio de sistemas e suporte. "[Eduardo.Inf.Br](https://informatizar.netlify.app/)".

---

<img 
    align="left" 
    alt="HTML"
    title="HTML" 
    width="30px" 
    style="padding-right: 10px;" 
    src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/html5/html5-original.svg" 
/>
<img 
    align="left" 
    alt="CSS" 
    title="CSS"
    width="30px" 
    style="padding-right: 10px;" 
    src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/css3/css3-original.svg" 
/>
<img 
    align="left" 
    alt="JavaScript" 
    title="JavaScript"
    width="30px" 
    style="padding-right: 10px;" 
    src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg" 
/>
<img 
    align="left" 
    alt="Bootstrap"
    title="Bootstrap" 
    width="30px" 
    style="padding-right: 10px;" 
    src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/bootstrap/bootstrap-original.svg" 
/>
<img 
    align="left" 
    alt="Git" 
    title="Git"
    width="30px" 
    style="padding-right: 10px;" 
    src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/git/git-original.svg" 
/>
