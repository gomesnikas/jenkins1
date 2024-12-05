pipeline {
    agent any

    triggers {
        pollSCM('* * * * *')
    }

    stages {
        stage('build') {
            steps {
                echo 'Builde !'
            }
        }
    }
}