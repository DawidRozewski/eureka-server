# 🏠 Eureka Server

## 📌 Overview
This service acts as a **Service Discovery Server** using **Spring Cloud Netflix Eureka**.  
It allows microservices to register themselves and discover other services dynamically, enabling better scalability and fault tolerance.

---

## 🏗️ About This Project

This project is designed as a **skeleton for microservices architecture**, providing a foundation for:
- **Learning microservices communication patterns**
- **Testing service discovery and dynamic scaling**
- **Experimenting with fault tolerance mechanisms**

The focus is on demonstrating how microservices interact rather than delivering a full production-ready system.

---

## 🛠️ Technology Stack

- **Java 21**
- **Spring Boot 3.4.3**
- **Spring Cloud 2024**
- **Spring Cloud Netflix Eureka Server**
- **Maven 3.14.0**
- **Docker**

## 🛠️ Infrastructure Stack (Docker)
- **Keycloak**
- **Kafka**
- **Kafka UI**
- **Prometheus**
- **Grafana**
- **MongoDB**

---

## 🚀 Running Eureka Server

To run this service, make sure you have first **set up the environment** by following the instructions in the **[Config Server README](https://github.com/DawidRozewski/config-server)**.

Once the required services are running, start Eureka Server with:

```sh
mvn spring-boot:run
```

Eureka Server will be available at: [http://localhost:8761](http://localhost:8761)

---

## 📌 Microservices Interactions

The following microservices register themselves in Eureka:

1. **[Kafka Producer Service](https://github.com/DawidRozewski/kafka-producer-service)** - Produces messages to Kafka.
2. **[Kafka Consumer Service](https://github.com/DawidRozewski/kafka-consumer-service)** - Consumes messages from Kafka.
3. **[API Gateway Service](https://github.com/DawidRozewski/api-gateway-service)** - Routes requests and provides authentication.

---

## 🔄 Refactoring Suggestions

Looking to enhance this project? Here are some key areas for improvement:

1. **Make Eureka Highly Available**
    - Deploy **multiple Eureka instances** in a cluster.
    - Configure **peer-to-peer replication** to improve fault tolerance.

2. **Enable Security**
    - Restrict access to Eureka with **authentication**.
    - Use **Spring Security + Keycloak** to protect the registry.

---

📢 **This project is a microservices skeleton meant for learning, experimentation, and testing new ideas.**  
Feel free to modify and extend it to fit your needs! 🚀
