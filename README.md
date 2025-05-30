#  🌄 Chile Tours – Sistema de Gestão de Excursões no Chile

*Uma solução completa e moderna para gestão de experiências turísticas no Chile* ✈️

## 📊 Status do Projeto

![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow?style=for-the-badge) 
![Universidade](https://img.shields.io/badge/Uninove-Projeto%20Acadêmico-2A5CAA?style=for-the-badge&logo=graduation-cap)
![Versão](https://img.shields.io/badge/Versão-2.0-blue?style=for-the-badge)
![Java](https://img.shields.io/badge/Java-17-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.3.3-6DB33F?style=for-the-badge&logo=spring&logoColor=white)

## 🎯 Sobre o Projeto

O **Chile Tours Backend** é a API REST que alimenta o sistema de gestão de excursões turísticas. Desenvolvido com arquitetura moderna e boas práticas de desenvolvimento, oferece uma base sólida para operações turísticas no Chile.

### 🔗 Integração
*Este backend se conecta ao repositório **[Chile-Tours-Frontend](https://github.com/EmanuelVieiira/chile-tours-front)**, que contém a interface do usuário.*

## ⚡ Funcionalidades Principais

### 🗓️ **Gestão Operacional**
- **Destinos Turísticos**: Cadastro completo com localização e detalhes
- **Pacotes Personalizados**: Criação flexível de experiências únicas  
- **Controle de Disponibilidade**: Gestão em tempo real de vagas
- **Preços Dinâmicos**: Sistema inteligente de precificação

### 👥 **Experiência do Cliente**
- **Portal do Viajante**: Interface dedicada aos turistas
- **Reservas Online**: Sistema completo de booking
- **Histórico Detalhado**: Registro completo de viagens
- **Sistema de Avaliações**: Feedback e comentários dos clientes

### 🔐 **Recursos Técnicos**
- **Autenticação Segura**: Sistema de login protegido
- **API RESTful**: Endpoints bem estruturados e documentados
- **Validação de Dados**: Proteção contra entrada de dados inválidos
- **Logs Estruturados**: Monitoramento e debugging facilitados

## 🛠️ Stack Tecnológica

### ⚙️ **Backend Core**
```yaml
Linguagem: Java 17 (LTS)
Framework: Spring Boot 3.3.3
Gerenciador: Maven
Arquitetura: REST API + MVC
```



### 🗄️ **Banco de Dados**
```yaml
Suporte: MySQL / PostgreSQL
ORM: Hibernate (via Spring Data JPA)
Migrations: Flyway (opcional)
Connection Pool: HikariCP
```

## 📁 Arquitetura do Projeto

```
backend-andino/
├── src/
│ ├── main/
│ │ ├── java/
│ │ │ └── com/example/backendandino/
│ │ └── resources/
│ │ └── application.properties
├── pom.xml
```

## 🚀 Como Executar

### 📋 **Pré-requisitos**
- Java 17 ou superior
- Maven 3.8+
- MySQL 8.0+ ou PostgreSQL 12+
- IDE de sua preferência (IntelliJ, Eclipse, VS Code)

### ⚡ **Execução Rápida**
```bash
# Clone o repositório
git clone https://github.com/seu-usuario/chile-tours-backend.git

# Entre no diretório
cd chile-tours-backend

# Execute com Maven
mvn spring-boot:run
```

### 🔧 **Configuração do Banco**
```yaml
# application.yml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/chile_tours
    username: seu_usuario
    password: sua_senha
  jpa:
    hibernate:
      ddl-auto: update
    show-sql: true
```

## 🛡️ Configuração de CORS

Para desenvolvimento local, o CORS já está configurado para aceitar requisições do frontend:

```java
@Configuration
public class CorsConfig implements WebMvcConfigurer {
    
    @Override
    public void addCorsMappings(CorsRegistry registry) {
        registry.addMapping("/api/**")
                .allowedOrigins("http://localhost:3000", "http://localhost:3001")
                .allowedMethods("GET", "POST", "PUT", "DELETE", "OPTIONS")
                .allowedHeaders("*")
                .allowCredentials(true);
    }
}
```

##  Como Contribuir

Contribuições são sempre bem-vindas!

1. 🍴 **Fork** o projeto no GitHub
2. 🌿 Crie uma **branch** para sua feature
   ```bash
   git checkout -b feature/nova-funcionalidade
   ```
3. ✨ **Commit** suas mudanças com mensagens claras
   ```bash
   git commit -m "feat: adiciona sistema de avaliações"
   ```
4. 📤 **Push** para sua branch
   ```bash
   git push origin feature/nova-funcionalidade
   ```
5. 🔄 Abra um **Pull Request** detalhado

## 📜 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

---
