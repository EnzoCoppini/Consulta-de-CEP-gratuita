# 🔍 API de Consulta de CEP
Este é um projeto Java com Spring Boot que fornece uma API REST para consultar informações de um CEP utilizando o serviço gratuito [ViaCEP](https://viacep.com.br/).
## 🚀 Como executar o projeto localmente
### ✅ Pré-requisitos
- Java 17 ou superior
- Maven
### ▶️ Passos
1. Clone este repositório:
```bash
git clone https://github.com/seu-usuario/nome-do-repo.git
```
2. Acesse a pasta do projeto:
```bash
cd nome-do-repo
```
3. Execute a aplicação com o Maven Wrapper:
```bash
./mvnw spring-boot:run
```
Ou, se preferir, importe o projeto em uma IDE (como IntelliJ ou Eclipse) e execute a classe `CepApplication.java`.
## 🌐 Endpoint disponível
### `GET /cep-consulta/{cep}`
Consulta os dados de um CEP utilizando a API ViaCEP.
#### 🔁 Exemplo de requisição:
```
GET http://localhost:8080/cep-consulta/01001000
```
#### 📄 Exemplo de resposta:
```json
{
  "cep": "01001-000",
  "logradouro": "Praça da Sé",
  "complemento": "lado ímpar",
  "bairro": "Sé",
  "localidade": "São Paulo",
  "uf": "SP",
  "ibge": "3550308",
  "gia": "1004",
  "ddd": "11",
  "siafi": "7107"
}
```
## 🛠️ Tecnologias utilizadas
- Java 17+
- Spring Boot
- Spring Web (RestController)
- RestTemplate
- Maven
- API pública [ViaCEP](https://viacep.com.br/)
## 📂 Estrutura do projeto
```
com.enzo.cep
├── CepApplication.java          // Classe principal
├── controller
│   └── CepController.java       // Endpoint de consulta de CEP
└── dto
    └── CepDTO.java              // Representação dos dados retornados da API ViaCEP
```
## 💡 Possíveis melhorias futuras
- Validação de CEP (formato e existência)
- Tratamento de erros com `@ExceptionHandler`
- Integração com Swagger (documentação interativa)
- Cache de resultados para otimizar chamadas à API ViaCEP
## 📄 Licença
Este projeto é de uso livre para fins pessoais, acadêmicos ou de demonstração.
