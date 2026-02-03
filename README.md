# DS Eventos

Aplicação Spring Boot para gerenciamento de eventos com JPA/Hibernate e H2 (em memória). Entidades principais: `Atividade`, `Bloco`, `Participante`, `Categoria`. Dados iniciais carregados por `src/main/resources/import.sql`.

## Tecnologias
- Java
- Spring Boot
- JPA / Hibernate
- H2 (in-memory)
- Maven

## Como executar
- Pela linha de comando:
\`\`\`bash
mvn clean package
mvn spring-boot:run
\`\`\`
- Na IDE: executar a classe `br.com.missio.dseventos.DseventosApplication` (main).

## Acesso H2
- Console H2 (se habilitado): `http://localhost:8080/h2-console`  
- JDBC URL padrão: `jdbc:h2:mem:testdb` (verificar `application.properties`)

## Dados iniciais
O arquivo `src/main/resources/import.sql` insere categorias, atividades, blocos, participantes e associações `participante_atividade`. Ajustar a ordem de inserção ou usar cascades adequados se ocorrerem erros de integridade.

## Estrutura principal
- `src/main/java/br/com/missio/dseventos/entities` — entidades JPA
- `src/main/resources/import.sql` — dados iniciais
- `src/main/resources/application.properties` — configurações

