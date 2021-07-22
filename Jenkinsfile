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
                    git url: 'https://github.com/ivchu/spring-petclinic.git', branch: 'main'
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


