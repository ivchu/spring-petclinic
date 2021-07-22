pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                script {
                    println 'Hello World, from task 1'
                    def petclinic = docker.build("ivchu/petclinic:${env.BUILD_TAG}")
                }
            }
        }
    }
}


