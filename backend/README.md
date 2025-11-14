src/
├── domain/
│   ├── entities/
│   │   └── Product.js
│   ├── value-objects/
│   │   └── Money.js
│   ├── repositories/
│   │   └── ProductRepository.js
│   └── services/
│       └── ProductService.js
├── infrastructure/
│   ├── database/
│   │   ├── connection.js
│   │   └── repositories/
│   │       └── ProductRepositoryPostgres.js
│   ├── http/
│   │   ├── controllers/
│   │   │   └── ProductController.js
│   │   ├── middleware/
│   │   │   ├── errorHandler.js
│   │   │   ├── validation.js
│   │   │   └── auth.js
│   │   └── routes/
│   │       └── productRoutes.js
│   └── utils/
│       ├── logger.js
│       └── validators.js
├── application/
│   └── use-cases/
│       └── product/
│           ├── CreateProductUseCase.js
│           ├── GetProductUseCase.js
│           ├── UpdateProductUseCase.js
│           └── DeleteProductUseCase.js
├── shared/
│   ├── errors/
│   │   ├── AppError.js
│   │   ├── DomainError.js
│   │   └── InfrastructureError.js
│   └── utils/
│       ├── responseHandler.js
│       └── queryBuilder.js
└── app.js



#### /domain (Camada de demínio)

### Propósito
- Coração do negocio: Contém as regras e lógica central do sistema/aplicação
- Independente de tecnologia: Não sabe nada sobre web, banco de dados, ou frameworks
- Representa o conhecimento especialista do dominio do e-commerce

### Subpastas e suas responsabilidades

domain/entities/

- Contém os objetos principais do negócio que têm identidade única
- Exemplo: Product, ProductCategory, User, Order...
-  