# Projeto 4 — Painel de Cotações & Clima

Aplicação desenvolvida em **Python** e **Django** que consome uma API externa de cotações ([AwesomeAPI](https://economia.awesomeapi.com.br/)), registra os dados em banco de dados e exibe o histórico atualizado em tempo real na interface web utilizando **Django REST Framework** e JavaScript assíncrono (`fetch`).

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.12+**
- **Django 6.1+**
- **Django REST Framework**
- **Requests** (para requisições HTTP externas)
- **HTML5 / CSS3 / JavaScript (ES6)**
- **SQLite** (Banco de dados padrão)

---

## 📂 Estrutura do Projeto

```text
projeto4/
├── painelapi/
│   ├── settings.py      # Configurações globais e URL externa
│   ├── urls.py          # Roteamento global
│   └── wsgi.py
├── painel/
│   ├── models.py        # Modelo RegistroCotacao (DecimalField)
│   ├── views.py         # Tratamento de requisições HTTP e ListAPIView
│   ├── serializers.py   # Serializador do DRF
│   ├── urls.py          # Rotas de /consultar/ e /api/historico/
│   ├── tests.py         # Testes unitários com Mocks
│   └── templates/
│       └── painel/
│           └── consultar.html # Template com fetch() e manipulação do DOM
├── manage.py
├── requirements.txt
└── .gitignore