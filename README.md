# Oracle GeoData Brasil

Base geográfica reutilizável para Oracle Database e Oracle APEX contendo dados de estados e municípios brasileiros.

Este projeto foi criado para servir como estrutura base em aplicações Oracle, incluindo:

- Oracle APEX
- APIs REST
- Sistemas ERP
- Sistemas de agendamento
- Sistemas imobiliários
- Dashboards
- Aplicações web e mobile
- Projetos acadêmicos
- Estudos Oracle SQL

---

# Estrutura do Projeto

```text
oracle-geodata-brasil/
│
├── database/
│   ├── estados.sql
│   ├── municipios.sql
│
├── data/
│   ├── estados.csv
│   ├── municipios.csv
│
├── seeds/
│   ├── estados_seed.sql
│   ├── municipios_seed.sql
│
└── README.md
```

---

# Objetivo

Disponibilizar uma base geográfica padronizada e reutilizável para projetos Oracle.

O projeto contém:

- Estrutura SQL das tabelas
- Dados brutos em CSV
- Scripts de carga (seed)
- Relacionamentos entre estados e municípios
- Dados preparados para Oracle Database

---

# Tecnologias Utilizadas

- Oracle Database
- Oracle SQL
- Oracle APEX
- SQL Developer
- Git
- GitHub

---

# Modelagem

## Estados

Tabela responsável pelos estados brasileiros.

Principais informações:

- UF
- Nome
- Região
- Latitude
- Longitude

---

## Municípios

Tabela responsável pelos municípios brasileiros.

Relacionamento:

```text
ESTADOS (1) -> (N) MUNICIPIOS
```

Principais informações:

- Código IBGE
- Nome do município
- Estado
- DDD
- Fuso horário
- Coordenadas geográficas

---

# Como Utilizar

## 1. Criar as tabelas

Execute os scripts da pasta:

```text
database/
```

Ordem recomendada:

```sql
estados.sql
municipios.sql
```

---

## 2. Inserir os dados

Execute os scripts da pasta:

```text
seeds/
```

Ordem recomendada:

```sql
estados_seed.sql
municipios_seed.sql
```

---

# Observações Técnicas

- Latitude e longitude utilizam tipo NUMBER
- IDs utilizam IDENTITY
- Municípios possuem chave estrangeira para estados
- Dados preparados para Oracle Database
- Scripts compatíveis com Oracle SQL Developer

---

# Melhorias Futuras

- Normalização de regiões
- Oracle Spatial
- Scripts automáticos CSV -> SQL
- API REST Oracle
- Integração com mapas
- Versionamento automatizado de seeds

---

# Licença

Projeto disponível para estudos, aprendizado e projetos pessoais.
