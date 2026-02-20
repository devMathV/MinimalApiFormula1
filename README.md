# 🏎️ F1 Teams & Drivers API

## 📖 Sobre a API
API RESTful desenvolvida com Fastify e TypeScript que fornece informações sobre equipes e pilotos de Fórmula 1. A API disponibiliza endpoints para consulta de times e pilotos, com suporte a busca individualizada de pilotos por ID.

## 🚀 Tecnologias
- **Node.js** - Ambiente de execução JavaScript
- **[Fastify](https://www.npmjs.com/package/fastify)** - Framework web de alta performance
- **[TypeScript](https://www.npmjs.com/package/typescript)** - Superset tipado de JavaScript
- **[@fastify/cors](https://www.npmjs.com/package/@fastify/cors)** - Plugin para gerenciamento de CORS

## 📍 Endpoints

### GET /teams
Retorna a lista completa de todas as equipes de F1 cadastradas, incluindo informações como ID, nome e base da equipe.

**Resposta:** `200 OK` - Array de objetos com id, name e base das equipes.

### GET /drivers
Retorna a lista completa de todos os pilotos cadastrados, com informações sobre ID, nome e equipe atual.

**Resposta:** `200 OK` - Array de objetos com id, name e team dos pilotos.

### GET /drivers/:id
Retorna os dados de um piloto específico baseado no ID fornecido como parâmetro na rota.

**Parâmetros:** `id` - Número inteiro identificador do piloto

**Respostas:**
- **`200 OK`** - Objeto com id, name e team do piloto encontrado
- **`404 Not Found`** - Mensagem de erro quando o piloto não existe

## 🔧 Instalação

```bash
# Clone o repositório
git clone https://github.com/devMathV/MinimalApiFormula1

# Acesse o diretório
cd ApiComFastify

# Instale as dependências
npm run install
```

## 📦 Scripts Disponíveis

- **`start:dev`** - Inicia o servidor em modo desenvolvimento utilizando as variáveis de ambiente do arquivo .env
- **`start:watch`** - Inicia o servidor com hot-reload, reiniciando automaticamente a cada alteração no código
- **`install`** - Instala todas as dependências necessárias para o funcionamento do projeto

## 🗂️ Estrutura de Dados

**Teams**
```json
{
  "id": 1,
  "name": "Ferrari",
  "base": "Woking, United Kingdom"
}
```

**Drivers**
```json
{
  "id": 1,
  "name": "Max Verstappen",
  "team": "Red Bull Racing"
}
```