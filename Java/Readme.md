# 🖥️ UniAlfa Eventos - Aplicação Desktop (Java)

Aplicação desktop desenvolvida em Java para gerenciamento de eventos acadêmicos da UniALFA.

## 📋 Descrição

Esta aplicação desktop permite gerenciar eventos, palestrantes e cursos através de uma interface gráfica desenvolvida com Java Swing.

## 🚀 Tecnologias

- **Java 21** - Linguagem de programação
- **Maven** - Gerenciamento de dependências
- **MySQL Connector** - Driver JDBC para conexão com banco de dados
- **Swing** - Framework para interface gráfica

## 📦 Estrutura do Projeto

```
Java/
├── src/main/java/hackatton/
│   ├── dao/          # Camada de acesso a dados
│   ├── gui/          # Interface gráfica (Swing)
│   ├── model/        # Modelos de dados
│   ├── service/      # Lógica de negócio
│   └── Main.java     # Classe principal
└── pom.xml           # Configuração Maven
```

## 🔧 Pré-requisitos

- **Java JDK 21** ou superior
- **Maven 3.6+**
- **MySQL** rodando com o banco `unialfa` configurado

## 📥 Instalação

### 1. Configure o Banco de Dados

Certifique-se de que o banco de dados `unialfa` está criado e configurado. Veja o README principal para instruções.

### 2. Configure a Conexão

Edite o arquivo `src/main/java/hackatton/dao/Dao.java` e ajuste as credenciais do banco de dados:

```java
this.connection = DriverManager.getConnection(
    "jdbc:mysql://localhost:3306/unialfa?useTimezone=true&serverTimezone=UTC",
    "root",        // Seu usuário MySQL
    ""             // Sua senha MySQL
);
```

### 3. Instale as Dependências

```bash
mvn clean install
```

O Maven irá baixar automaticamente as dependências necessárias, incluindo o MySQL Connector.

## 🚀 Execução

### Opção 1: Via Maven

```bash
mvn exec:java -Dexec.mainClass="hackatton.Main"
```

### Opção 2: Compilar e Executar Manualmente

```bash
# Compilar
mvn compile

# Executar
java -cp target/classes:target/dependency/* hackatton.Main
```

### Opção 3: Gerar JAR Executável

```bash
mvn package
java -jar target/poo-maven-a-1.0-SNAPSHOT.jar
```

## 📝 Funcionalidades

- Gerenciamento de eventos
- Cadastro de palestrantes
- Gerenciamento de cursos
- Interface gráfica intuitiva

## ⚠️ Notas

- Certifique-se de que o MySQL está rodando antes de executar a aplicação
- A aplicação requer conexão com o banco de dados `unialfa`
- Para mais informações sobre o projeto completo, consulte o README principal na raiz do repositório

