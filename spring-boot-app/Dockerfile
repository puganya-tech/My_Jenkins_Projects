# Base image with Java 25
FROM openjdk:25-jdk

# Install required tools: Maven, Docker CLI, git
RUN apt-get update && apt-get install -y \
    maven \
    git \
    curl \
    unzip \
    docker.io \
    && rm -rf /var/lib/apt/lists/*

# Set environment variables
ENV JAVA_HOME=/usr/lib/jvm/java-25-openjdk
ENV PATH=$JAVA_HOME/bin:$PATH

# Default working directory
WORKDIR /workspace

# Verify installations
RUN java -version && mvn -version && docker --version
