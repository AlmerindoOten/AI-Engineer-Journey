Json: forma organizada de armazenar informações.
Comum a varias linguagens. 
Facil analise e interpretação por apis.

Estrutua do Json: Objeto
└── usuarios
    └── Array
        ├── Objeto
        │   ├── nome
        │   └── idade
        │
        └── Objeto
            ├── nome
            └── idade

Objetos aninhados
usuario
 ├── nome
 ├── idade
 └── endereco
      ├── cidade
      └── estado
Para consultar cidade: usuario.endereco.cidade

EX: 
{
    "empresa": {
        "nome": "TechCorp",
        "endereco": {
            "cidade": "São Paulo",
            "estado": "SP"
        },
        "funcionarios": [
            {
                "nome": "João",
                "cargo": "Dev"
            },
            {
                "nome": "Maria",
                "cargo": "Designer"
            }
        ]
    }
}
para saber quem eh a desingner da empresa:m
empresa.funcionarios[1].cargo
→ Designer

Vazios: 
[]    → lista vazia
{}    → objeto vazio
null  → ausência de valor
""    → texto vazio
0     → número zero
false → valor booleano falso

