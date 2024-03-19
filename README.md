<h1>Conference Room Booking API</h1>

<p><strong>Descrição:</strong> API para reserva de salas de conferência, permitindo aos usuários agendar, atualizar e cancelar reservas.</p>

<h2>Tecnologias Utilizadas</h2>
<ul>
  <li>Spring Boot</li>
  <li>Spring Security</li>
  <li>JPA / Hibernate</li>
  <li>Maven</li>
  <li>H2 Database (para desenvolvimento)</li>
</ul>

<h2>Endpoints</h2>
<p>A API contém os seguintes endpoints principais:</p>
<ul>
  <li><code>POST /reservations</code> - Cria uma nova reserva</li>
  <li><code>GET /reservations</code> - Lista todas as reservas</li>
  <li><code>GET /reservations/{id}</code> - Obtém detalhes de uma reserva específica</li>
  <li><code>PUT /reservations/{id}</code> - Atualiza uma reserva existente</li>
  <li><code>DELETE /reservations/{id}</code> - Cancela uma reserva</li>
</ul>

<h2>Autenticação</h2>
<p>A API utiliza autenticação básica. Utilize as seguintes credenciais para acesso:</p>
<ul>
  <li><strong>Username:</strong> user</li>
  <li><strong>Password:</strong> password</li>
</ul>

<h2>Exemplo de Requisição e Resposta</h2>
<h3>Criar Reserva (<code>POST /reservations</code>)</h3>
<h4>Requisição</h4>
<pre><code>{
  "roomId": 1,
  "startTime": "2024-03-20T09:00:00",
  "endTime": "2024-03-20T11:00:00",
  "userId": "123"
}</code></pre>
<h4>Resposta</h4>
<pre><code>{
  "id": 1,
  "roomId": 1,
  "startTime": "2024-03-20T09:00:00",
  "endTime": "2024-03-20T11:00:00",
  "userId": "123",
  "status": "CONFIRMED"
}</code></pre>

<h2>Como Rodar o Projeto</h2>
<ol>
  <li>Clone o repositório: <code>git clone URL_DO_REPOSITORIO</code></li>
  <li>Navegue até a pasta do projeto: <code>cd conference-room-booking</code></li>
  <li>Execute o projeto: <code>./mvnw spring-boot:run</code></li>
  <li>Acesse os endpoints via Postman ou outro cliente HTTP de sua preferência.</li>
</ol>

<h2>Segurança</h2>
<p>A configuração de segurança está implementada em <code>com.sena.conferenceroombooking.security.SecurityConfiguration</code>, utilizando Spring Security para autenticação básica e proteção dos endpoints.</p>
