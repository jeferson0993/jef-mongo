# Novas Tecnologias em BD

## Aula 10 - Proposta de Sistema com Base de Dados Orientada a Documentos - 1,5

* A partir do conteúdo de texto e vídeo disponibilizados na plataforma, escolha um domínio de negócio (por exemplo, uma mercearia, academia, clínica veterinária, clube, etc) e faça uma modelagem simplificada para uma base de dados orientada a documentos usando o MongoDB. 

* Descreva a aplicação e apresente a modelagem proposta, ilustrando como os dados serão organizados e as possíveis interações entre coleções e documentos. 

* Elabore uma lista de relatórios (pelo menos 4) que seriam importantes para o negócio em questão.

* Faça em formato de apresentação de slides.

# [Link para a apresentação online](http://bit.do/jef-mongo)

## Este trabalho tem o objetivo de apresentar a modelagem de um sistema de gerenciamento de Biblioteca. O sistema tem por finalidade controlar entrada e saída de acervos, controle de usuários, e emissão de relatórios gerenciais

#### Books Collection:
```json
{
  "books": [
    {
      "id": 0,
      "title": "",
      "isbn": 0,
      "author": [
        {}
      ],
      "published-year": 0,
      "topics": [
        ""
      ],
      "language": "",
      "total": 0,
			"min-stock": 0,
      "availables": 0,
      "borrowed": [
        {
          "reader": {},
          "date": "timestamp"
        }
      ]
    }
  ]
}
```

#### Users Collection
```json
{
  "users": [
    {
      "id": 0,
      "nome": "",
      "type": [
        ""
      ],
      "documents": [
        {
          "cpf": "",
          "matricula": ""
        }
      ],
      "contacts": [
        {
          "personal": [
            ""
          ],
          "professional": [
            ""
          ]
        }
      ],
      "historic": [
        {
          "book": {},
          "borrowed-start": "",
          "borrowed-end": ""
        }
      ]
    }
  ]
}
```

#### Borrowers Collection
```json
{
	"borrowers": [
		{
			"id": 0,
			"reader": {
				"id": 0,
				"nome": "",
				"type": [
					""
				],
				"documents": [
					{
						"cpf": "",
						"matricula": ""
					}
				],
				"contacts": [
					{
						"personal": [
							""
						],
						"professional": [
							""
						]
					}
				],
				"historic": [
					{
						"book": {},
						"borrowed-start": "",
						"borrowed-end": ""
					}
				]
			},
			"books": [
				{
					"id": 0,
					"title": "",
					"isbn": 0,
					"author": [
						{}
					],
					"published-year": 0,
					"topics": [
						""
					],
					"language": "",
					"total": 0,
					"availables": 0,
					"borrowed": [
						{
							"reader": {},
							"date": "timestamp"
						}
					]
				}
			],
			"date": "timestamp"
		}
	]
}
```

#### Fines Collection
```json
{
  "fines": [
    {
      "id": 0,
      "reader": {},
      "books": [
        {}
      ],
      "borrowed-start": "",
      "borrowed-end": "",
      "price": 0
    }
  ]
}
```