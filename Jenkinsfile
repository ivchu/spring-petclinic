pipeline {
    environment {
        registry = "ivchu/petclinic"
    }
    agent any

    stages {
        stage('build') {
            steps {
                script {
                    println 'Hello World, from task 1'
                    println 'Building docker image'
                    def petclinic = docker.build(registry)
                    println 'Docker image built'
                }
            }
        }
    }
}


