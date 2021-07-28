pipeline {
    environment {
        registry = "ivchu/petclinic"
        registryCredential = "325621e4-ea66-46b0-a752-a82ff99a5d5c"
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
        stage('Push image to dockerhub') {
            steps {
                script {
                    println 'Pushing docker image'
                    docker.withRegistry( '', registryCredential ) {
                        petclinic.push()
                    }
                    println 'Docker image pushed'
                }
            }
        }
    }
}



