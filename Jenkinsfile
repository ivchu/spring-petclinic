pipeline {
    environment {
        registry = "ivchu/petclinic"
        registryCredential = "dockerhub"
    }
    agent any

    stages {
        stage('Hello World') {
            steps {
                script {
                    println 'Hello World, from task 1'
                }
            }
        }
        stage('Build app') {
            steps {
                git url: 'https://github.com/ivchu/spring-petclinic.git', branch: 'main'
                echo 'Git cloned'
                sh './mvnw clean install'
            }
        }
        stage('Building image') {
            steps {
                script {
                    println 'Building docker image'
                    def petclinic = docker.build(registry + ":$BUILD_NUMBER")
                    println 'Docker image built'
                }
            }
        }
    }
}


