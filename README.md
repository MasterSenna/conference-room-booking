Conference Room Booking API
 

Descrição
API para reserva de salas de conferência, permitindo aos usuários agendar, atualizar e cancelar reservas.

Tecnologias Utilizadas
Spring Boot
Spring Security
JPA / Hibernate
Maven
H2 Database (para desenvolvimento)
Endpoints
A API contém os seguintes endpoints principais:

POST /reservations - Cria uma nova reserva
GET /reservations - Lista todas as reservas
GET /reservations/{id} - Obtém detalhes de uma reserva específica
PUT /reservations/{id} - Atualiza uma reserva existente
DELETE /reservations/{id} - Cancela uma reserva
Autenticação
A API utiliza autenticação básica. Utilize as seguintes credenciais para acesso:

Username: user
Password: password
Exemplo de Requisição e Resposta
Criar Reserva (POST /reservations)
Requisição
json
Copy code
{
  "roomId": 1,
  "startTime": "2024-03-20T09:00:00",
  "endTime": "2024-03-20T11:00:00",
  "userId": "123"
}
Resposta
json
Copy code
{
  "id": 1,
  "roomId": 1,
  "startTime": "2024-03-20T09:00:00",
  "endTime": "2024-03-20T11:00:00",
  "userId": "123",
  "status": "CONFIRMED"
}
Como Rodar o Projeto
Clone o repositório: git clone URL_DO_REPOSITORIO
Navegue até a pasta do projeto: cd conference-room-booking
Execute o projeto: ./mvnw spring-boot:run
Acesse os endpoints via Postman ou outro cliente HTTP de sua preferência.
Segurança
A configuração de segurança está implementada em com.sena.conferenceroombooking.security.SecurityConfiguration, utilizando Spring Security para autenticação básica e proteção dos endpoints.
