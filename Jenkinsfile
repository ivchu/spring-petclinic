pipeline {
    agent any

    stages {
        stage('Build') {
            git url: 'https://github.com/ivchu/spring-petclinic.git', branch: 'main'

            echo 'Build docker image'
        }
    }
}



