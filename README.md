🏗️ Proposta Arquitetural

A arquitetura do sistema ALUMNI foi projetada com foco em organização, escalabilidade e clareza na separação de responsabilidades, permitindo fácil manutenção e evolução da aplicação.

O modelo adotado segue uma abordagem modular, dividida em camadas bem definidas, contemplando desde a interação do usuário até o processamento e persistência dos dados.

📌 Visão Geral

O sistema é estruturado em três principais perspectivas arquiteturais:

Funcional (Casos de Uso) – Representa as interações entre os usuários e o sistema.
Estrutural (Classes) – Define a organização interna das entidades e seus relacionamentos.
Física (Implantação) – Mostra como os componentes são distribuídos em ambiente de execução.

As imagens correspondentes aos diagramas (caso de uso, classes e implantação) estão disponíveis no repositório em formato compactado (.zip).

👤 Diagrama de Caso de Uso

O sistema foi modelado com base em um ator genérico Usuário, que representa qualquer indivíduo autenticado na plataforma. A partir dele, derivam duas especializações:

Aluno
Egresso

Ambos herdam funcionalidades comuns, como:

Cadastro
Login
Edição de perfil

Além disso, o sistema contempla três grandes grupos de funcionalidades:

Gestão de Carreira
Visualização e publicação de vagas
Engajamento em Eventos
Visualização de eventos e confirmação de participação
Interação Social
Participação em grupos
Publicação de conteúdos

Essa estrutura reforça o objetivo da plataforma como uma rede institucional voltada ao networking e à colaboração.

🧩 Diagrama de Classes

A estrutura interna do sistema é organizada a partir da classe base Usuário, que contém atributos essenciais como nome, e-mail e senha.

A partir dela, derivam:

Aluno
Curso
Ano de ingresso
Egresso
Empresa atual
Ano de formação

O sistema também inclui entidades complementares:

Vaga → informações sobre oportunidades profissionais
Evento → dados de eventos acadêmicos
Grupo → espaços de interação entre usuários
🔗 Relacionamentos principais:
Um usuário pode publicar várias vagas
Um usuário pode participar de múltiplos eventos (relação muitos-para-muitos)
Um usuário pode ingressar em diversos grupos

Essa modelagem garante flexibilidade e extensibilidade para futuras funcionalidades.

🌐 Diagrama de Implantação

A arquitetura física do sistema é composta por três camadas principais:

💻 Cliente (Frontend)
Executado no navegador
Desenvolvido com HTML, CSS e JavaScript
Responsável pela interface e interação com o usuário
⚙️ Servidor Backend (Node.js)
Responsável pela lógica de negócio
Gerencia requisições, autenticação e comunicação com o banco de dados
Atua como intermediário entre frontend e serviços externos
☁️ Serviços e Persistência
Firebase Authentication
Gerenciamento de autenticação e segurança
Comunicação via API REST
Banco de Dados (SQLite)
Armazenamento local leve e eficiente
Comunicação via consultas SQL

Essa estrutura garante uma comunicação fluida entre os componentes e possibilita futuras expansões para ambientes distribuídos ou em nuvem.

🚀 Considerações

A proposta arquitetural do ALUMNI foi desenvolvida para equilibrar simplicidade e robustez, permitindo:

Facilidade de manutenção
Escalabilidade futura
Organização clara dos componentes
Integração eficiente entre frontend, backend e serviços externos

Essa base sólida possibilita a evolução contínua do sistema, acompanhando novas demandas e funcionalidades.
