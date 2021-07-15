pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                git url: 'https://github.com/ivchu/spring-petclinic.git', branch: 'main'
                echo 'building'
            }
        }
    }
}


