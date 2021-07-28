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

    }
}



