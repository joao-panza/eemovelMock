# 📌 Mock AVR - API Mock para Integração de AVR  

🚀 Esta coleção do **Postman** foi criada para **mockar** as integrações de **AVR da EEMOVEL**.  

## 📂 Estrutura  

A coleção contém os seguintes endpoints:  

- **Criação de Solicitação** (📌 `POST /avr/solicit/integration/create_solicitation`)  
  - ✅ **201** - Solicitação criada com sucesso  
  - ❌ **400** - Erro de requisição  
  - ❌ **500** - Erro interno do servidor  

## 🔧 Como Usar  

### 🛠️ Importando a Coleção  

1. **Baixe o arquivo** `Mock AVR.postman_collection.json`.  
2. **Abra o Postman** e vá até a aba **Collections**.  
3. **Clique em "Import"** e selecione o arquivo JSON.  

### 📝 Executando as Requisições  

1. **Configure a variável `{{url}}`** com o mock disponível:  
   ```text
   https://a306d1ef-db25-4263-b6ba-699f5ed27ea5.mock.pstmn.io
   ```  
2. Selecione a requisição desejada dentro da coleção.  
3. Insira os parâmetros necessários no **Body**.  
4. Clique em **Send** para testar.  

## 🛡️ Headers Necessários  

Todas as requisições precisam dos seguintes **headers**:  

```json
{
  "x-api-key": "SUA_CHAVE_API",
  "Content-Type": "application/json"
}
```

💡 *Lembre-se de substituir `"SUA_CHAVE_API"` por um valor válido!*  

## 📤 Exemplo de Requisição  

### **Criar Solicitação**  

#### 📩 **Request**  

```http
POST /avr/solicit/integration/create_solicitation HTTP/1.1
Host: {{url}}
Content-Type: application/json
x-api-key: SUA_CHAVE_API
```

#### 📦 **Body (JSON)**  

```json
{
  "full_address": {
    "city": "São Paulo",
    "neighborhood": "Bela Vista",
    "number": "1234",
    "postal_code": "01310-100",
    "state": "SP",
    "street": "Avenida Paulista",
    "lat": -23.5634108,
    "lon": -46.6537575
  },
  "solicitation_type": "real_estate_appraisal",
  "property_type": "Apartamento",
  "business_type": "Aquisição",
  "proposer": "John Doe",
  "proposer_cpf_cnpj": "333.333.333-33",
  "trading_value": "560000",
  "email": "demo@eemovel.com",
  "phone_number": "(00) 99999-9999"
}
```

## 📬 Possíveis Respostas  

### ✅ **201 - Criado**  

```json
{
  "data": {
    "id": "66a3d4ce8a6a1b80e071b16d",
    "code": "20240726EEM1354295"
  },
  "message": "Solicitação criada com sucesso!",
  "code": 201,
  "success": true
}
```

### ❌ **400 - Bad Request**  

```json
{
  "message": "A solicitação não pôde ser processada devido a um erro na requisição.",
  "status": 400,
  "details": "Verifique os dados enviados e tente novamente."
}
```

### ❌ **500 - Internal Server Error**  

```json
{
  "message": "Um erro desconhecido ocorreu ao tentar essa rota.",
  "code": 500,
  "success": false
}
```

## 🛠️ Tecnologias Utilizadas  

- **Postman** 📨  
- **JSON** 📝  
- **API Mocking** 🛡️  

## 🤝 Contribuição  

Se precisar adicionar novos endpoints, siga os passos:  

1. **Crie uma nova requisição** no Postman.  
2. **Configure os headers e o body** conforme necessário.  
3. **Salve dentro da coleção "Mock AVR"**.  
4. **Exporte e atualize o arquivo JSON** no repositório.  

## 📄 Licença  

📝 Este projeto segue a licença **MIT**.  
