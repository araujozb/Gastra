# Gastra.io







gastronomia-saas/
│
├── backend/                     # Back-end com Spring Boot (Java)
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/seuprojeto/
│   │   │   │   ├── controller/          # APIs REST
│   │   │   │   ├── model/               # Entidades JPA (ex: Ingrediente, Receita)
│   │   │   │   ├── repository/          # Interfaces JPA
│   │   │   │   ├── service/             # Lógica de negócios e precificação
│   │   │   │   └── GastronomiaApp.java  # Classe principal (main)
│   │   │   └── resources/
│   │   │       ├── application.properties  # Configurações (ex: conexão com MySQL)
│   │   │       └── templates/              # HTML (caso use Thymeleaf)
│   │   │       └── static/                 # CSS, JS, imagens
│   └── pom.xml                         # Dependências Maven
│
├── frontend/                    # Front-end (opcional, caso use React separado)
│   ├── public/
│   ├── src/
│   │   ├── components/          # Componentes reutilizáveis
│   │   ├── pages/               # Páginas (Dashboard, Receitas, etc.)
│   │   ├── services/            # Requisições à API (axios etc.)
│   │   └── App.js
│   └── package.json
│
├── docs/                        # Documentação do projeto
│   ├── arquitetura.md
│   ├── roadmap.md
│   └── mockups/                 # Imagens, esquemas, fluxogramas
│
├── sql/                         # Scripts SQL (ex: criação de schema)
│   └── init_schema.sql
│
├── .gitignore
├── README.md                    # Instruções do projeto
└── LICENSE
