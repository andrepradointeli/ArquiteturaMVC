![ArqMVC](https://github.com/andrepradointeli/ArquiteturaMVC/assets/159079743/406eab58-afe7-4fd8-ad7b-83acd63a34df)

### Elementos Chave e Relacionamentos:

- **View (Vista)**: Contém três interfaces principais: LOGIN SCREEN, FEEDBACKS SCREEN e DASHBOARDS. Cada uma dessas interfaces é projetada para interagir com o usuário final e capturar a entrada do usuário ou apresentar dados. Por exemplo, LOGIN SCREEN coleta informações de autenticação, enquanto FEEDBACKS SCREEN apresenta feedbacks e DASHBOARDS exibe métricas e status do jogo.
  
- **Controller (Controlador)**: Existem três controladores correspondentes: USER CONTROLLER, POST CONTROLLER e FEEDBACK CONTROLLER. Eles atuam como intermediários entre a interface do usuário (View) e o modelo de dados (Model), processando entradas do usuário, solicitando dados do Model ou atualizando-o e, em seguida, passando os dados de volta para a View para serem exibidos.

- **Model (Modelo)**: Inclui USER, FEEDBACK e POST, cada um representando a estrutura dos dados no banco de dados. Eles são os componentes centrais para gerenciamento de dados e regras de negócio e estão diretamente ligados ao DATABASE, que neste caso é PostgreSQL.

- **Database (Banco de Dados)**: PostgreSQL é o sistema de gerenciamento de banco de dados escolhido, que armazenará as tabelas e registros correspondentes aos Models.

### Decisões de Design e Implicações:

- A separação clara entre View, Controller e Model segue o padrão MVC, o que facilita a manutenção do código e a escalabilidade do projeto.
- A decisão de usar o PostgreSQL como sistema de gerenciamento de banco de dados indica a necessidade de um banco de dados robusto, escalável e que suporta recursos avançados.
- Cada controlador lida com operações CRUD para o seu modelo correspondente, o que implica uma separação de responsabilidades. Isso garante que o aplicativo possa lidar com diferentes operações de forma eficiente e modular.
- As Views são focadas na interação do usuário e são mantidas separadas da lógica de negócios, o que implica que o design do front-end pode ser alterado sem afetar a lógica de back-end.

### Alinhamento com os Objetivos e Requisitos do Projeto:

- A arquitetura apoia o objetivo de criar uma plataforma interativa, visto que possui interfaces de usuário bem definidas para login, feedback e dashboards, que são essenciais para interação do usuário.
- O foco na colaboração e comunicação é apoiado pelos módulos de feedback e postagem, onde os usuários podem interagir e compartilhar informações.
- O controle de acesso é gerenciado pelo USER MODEL e USER CONTROLLER, que é crucial para lidar com a diversidade cultural e a identificação de preconceitos, conforme mencionado nos requisitos do projeto.
- A arquitetura favorece a expansão futura e a integração de novos módulos ou funcionalidades devido à sua natureza modular e à clara separação de responsabilidades.

