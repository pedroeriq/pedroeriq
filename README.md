graph TB
    A[Iniciar Cliente]
    A --> B[Definir IP e Porta do Servidor]
    B --> C[Criar Socket]
    C --> D[Tentar Conectar ao Servidor]
    
    D -->|Conectado| E[Enviar Mensagem ao Servidor]
    D -->|Erro de Conexão| M[Exibir Erro de Conexão] --> H[Fim]
    
    E --> F[Aguardar Resposta do Servidor]
    F --> G[Receber Resposta]
    
    G -->|Resposta Recebida| H[Exibir Resposta]
    G -->|Erro na Recepção| N[Exibir Erro de Recepção] --> H
    
    H --> I[Fechar Conexão]
    I --> J[Fim]
