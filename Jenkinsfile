pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                git url: 'https://github.com/ivchu/spring-petclinic.git', branch: 'main'
                echo 'building docker image'

                script {
                    dockerImage = docker.build("ivchu/petclinic:${env.BUILD_ID}")
                }
            }
        }
    }
}
