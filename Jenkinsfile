pipeline {
    environment {
        registry = "ivchu/petclinic"
        registryCredential = "dockerhub"
    }
    agent any

    stages {
        stage('build') {
            steps {
                script {
                    println 'Hello World, from task 1'
                }
            }
        }
        stage('Cloning Git') {
            steps {
                script {
                    git 'https://github.com/gustavoapolinario/microservices-node-example-todo-frontend.git'
                    println 'Git cloned'
                }
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


