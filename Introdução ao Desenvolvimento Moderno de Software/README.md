# Introdução ao Desenvolvimento Moderno de Software

## Introdução

Conceitos de como é atualmente o desenvolvimento de software.
Primeiro, temos um exemplo: iremos lançar um produto.
DIO Bank: banco digital

Então, temos que pensar qual(is) tipo(s) de plataforma(s) iremos utilizar, para desenvolver este DIO Bank.

## Sistema Desktop x Sistema Web

### Sistema Desktop

Sistemas instalados no computador (aplicativos Windows como Office, Notepad, etc.).
Caiu em desuso porque há menos mobilidade, menos acessível ao usuário por requerer um computador.

### Sistema Web

Sistemas com tecnologia web (sites por exemplo, porém não necessariamente é um site disponível na internet - intranet por exemplo é algo acessível apenas dentro de uma empresa).
Mercado bem amplo porque praticamente tudo está na internet/usa a internet.

### Aplicação móvel

Similar a um sistema Desktop no sentido de que é necessário um instalador, levarmos em consideração várias das configurações do dispositivo, sistema operacional, etc, como faríamos com um aplicativo desktop.

## UX/UI Designer

### UX Design (User eXperience)

Design de experiência do usuário.
Visa melhorar a satisfação do cliente, melhorando a usabilidade, acessibilidade do produto.
Pensar sobre o que fazer com que o software encante o cliente.
Como será visualmente o nosso produto tela-a-tela, para encantarmos o cliente?

Ferramentas: Figma, Adobe XP, entre outras.

Funções: Pesquisas sobre as tendências de mercado sobre a experiência de usuário, criação de Protótipos de telas do produto, entender quem são as Personas (as pessoas, os usuários) do produto, e entender os Objetivos da aplicação.
Trabalha na experiência de usuário, sobre como conceitualmente deve ser o uso do produto para o cliente.

### UI Design (User Interface)

Responsável em criar o que o usuário irá ver e utilizar no produto.
Entende padrões visuais que podem ajudar o usuário na experiência de uso do software.
Profissional focado em cores, tipografia, microinterações e estilos.
Trabalha no design do produto em si.

Funções: Design, Tipografia, Cores, Layouts

Ferramentas: Invision, Visio, Adobe XD, Figma

## Front End

Modelo Cliente-Servidor
É uma estrutura de aplicação que distribui as cargas de trabalho e tarefas entre os fornecedores de um recurso ou serviço (servidores) e os requerentes dos serviços (clientes).
Front End é aquilo que tá na "tela" do usuário, a interface, a parte frontal do produto ou serviço que o usuário irá utilizar.

### Desenvolvedor Front End

Programa a parte visual do site ou aplicativo. Responsável por desenvolver por código a interface gráfica, normalmente com as tecnologias base da Web (HTML, CSS e JavaScript).
Pode ocorrer do desenvolvedor tanto programar a interface, quanto trabalhar como UX/UI. Ideal seria ter estas funções desempenhadas por colaboradores diferentes.

Normalmente primeiro se programa o Back End e depois o Front End, mas não é regra.

## Onde criamos os códigos? Em uma IDE!

IDE = ambiente de desenvolvimento integrado (Integrated Development Environment)

Programador "raíz" programa no Notepad! :v

A IDE tem várias ferramentas que ajudam na codificação, como checagem de sintaxe, teste de código, compilação, etc.

## Framework

A grosso modo, é um facilitador.
Traz diversas soluções prontas para facilitar o trabalho do desenvolvedor.
A atuação do programador pode ter muito da parte criativa, mas também muita repetição, o que seria complicado sem facilitadores.

Exemplos: Angular, Laravel e VUE

## Back End

Programa a parte funcional do site ou aplicativo (funções, cálculos, queries, etc.), ou a "parte de trás" da aplicação.
Normalmente trabalha com a ponte entre os dados, aplicando devidamente as regras de negócio, validações e garantias em um ambiente que o usuário final não terá acesso.
Exemplos de linguagens utilizadas: Java, PHP, C#.

## API (ou Application Programming Interface)

Serve como um intermediário, que permite que dois softwares conversem entre si.
Obs.: devemos pensar também na questão de segurança ao utilizarmos APIs, pois há formas dos usuários ou pessoas má-intencionadas burlarem a API e utilizarem de forma indevida a mesma.

Exemplo de API: pokeapi.co

## Full Stack

Desenvolvedor tanto na parte de Back End, quanto de Front End.
Precisam ter habilidades com uma ampla gama de linguagens de programação.

## QA (Quality Assurance)

Conjunto de ações, ou setor da empresa para executar tais ações, para garantir a qualidade da entrega do produto.
O profissional de QA deve ter conhecimento sobre as atividades do projeto, ter perfil analítico.
Checa se os padrões de qualidade estão sendo atendidos e se os requisitos mínimos estão sendo entregues.

## Infraestrutura e Cloud

Temos a relação Cliente x Servidor.
Quando desenvolvemos um produto, teremos que hospedá-lo em algum lugar.

Nuvem Privada (também pode ser chamado de on-premises datacenter): quando a empresa em si cuidará da infraestrutura dos servidores. Datacenter local.
Características e necessidades: Segurança da Tecnologia da Informação (lógica e física), Mão de obra especializada, Infraestrutura local.

Nuvem Pública: quando terceirizamos a infraestrutura dos servidores ou terceirizamos partes dessa infraestrutura).
Exemplos: Amazon Web Services (AWS), Microsoft Azure, Oracle, Salesforce, entre outros.
Vantagens: Preço (pague somente o que usar), facilidade de contratação, configuração e infraestrutura; escalabilidade e performance.
Outra vantagem, vendo os serviços do Azure e da AWS, é também a facilidade na customização e amplo catálogo de serviços e tecnologias disponíveis, não limitado apenas a IaaS.

Exemplos de serviços disponibilizados por terceiros (informações também disponíveis no curso de SC-900):
IaaS - Infrastructure as a Service
PaaS - Platform as a Service
SaaS - Software as a Service
FaaS - Function as a Service
On-premises

O profissional de Cloud Computing é responsável pela infraestrutura na nuvem oferecida aos clientes.
Não apenas projeta sistemas ou ambientes de TI, escolhe também quais tecnologias serão utilizadas, operadoras, quais peças serão integradas, entre outras funções.

## A Tech!

Vídeo interessante resumindo 50 serviços do AWS:

[![Top 50+ AWS Services Explained in 10 Minutes](http://img.youtube.com/vi/JIbIYCM48to/0.jpg)](http://www.youtube.com/watch?v=JIbIYCM48to "Top 50+ AWS Services Explained in 10 Minutes")

## Mobile

Para mobile, precisamos pensar também quanto a responsividade da aplicação, ou como a aplicação vai se comportar em dispositivos das mais diversas versões do Android e iOS, resoluções, entre outras questões.

Exemplos de ferramentas: Android Studio, Xcode.
Exemplos de linguagens utilizadas: Java, Kotlin, Swift.

Há também o desenvolvimento híbrido, em que embarcamos uma aplicação web para ambos os dispositivos.
Porém há suas desvantagens. Não é recomendado por exemplo o desenvolvimento híbrido para jogos por exemplo, pois pode pecar na questão performance.
Exemplos de tecnologias: Ionic, Flutter, React Native.

## Conclusão

### Materiais Complementares

Slides destes módulos: https://academiapme-my.sharepoint.com/:p:/g/personal/nubia_dio_me/EYHcjptuOoNPs4qzd2upfmwBaLoG_FfSdzZH3zJiBvABiw?e=XYsmFR