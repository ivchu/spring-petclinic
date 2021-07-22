pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                echo 'Hello World, from task 1'
                def petclinic = docker.build "ivchu/petclinic:${env.BUILD_TAG}"
            }
        }
    }
}
