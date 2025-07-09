# Usa uma imagem base Java para construir a aplicação
FROM openjdk:17-jdk-slim AS build

# Define o diretório de trabalho dentro do container
WORKDIR /app

# Copia o arquivo pom.xml para que as dependências possam ser baixadas
COPY pom.xml .

# Copia os arquivos de código-fonte
COPY src ./src

# Compila o projeto Maven e empacota o JAR executável
# Pula os testes para agilizar o build do Docker se não forem estritamente necessários no build
RUN mvn clean package -DskipTests

# Estágio de Runtime: Usa uma imagem base menor para a aplicação final
FROM openjdk:17-jre-slim

# Define o diretório de trabalho
WORKDIR /app

# Copia o JAR do estágio de build para o estágio de runtime
# Assumindo que o artifact gerado seja gastronomia-backend-0.0.1-SNAPSHOT.jar
COPY --from=build /app/target/gastronomia-backend-0.0.1-SNAPSHOT.jar app.jar

# Expõe a porta que a aplicação Spring Boot irá rodar
EXPOSE 8080

# Comando para rodar a aplicação quando o container iniciar
ENTRYPOINT ["java", "-jar", "app.jar"]