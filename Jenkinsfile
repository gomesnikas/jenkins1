pipeline {
    agent any

    stages {
        stage('build and test') {
            matrix {

                axes {
                    axis {
                        name 'PLATEFORME'
                        values 'linux', 'macos' , 'wonwows'
                    }
                    axis {
                        name 'BROWSER'
                        values 'firefox' , 'chrome' , 'safari'
                    }
                }

                stage {
                    stage ('build') {
                        steps {
                            echo 'Construire pour ${ PLATEFORME } - ${ BROWSER }'
                        }
                    }
                    stage ('test') {
                        steps {
                            echo 'Tester pour ${ PLATEFORME } - ${ BROWSER }'
                        }
                    }
                }
                
            }
        }

        stage('deploiement production') {
            steps {
                echo 'Déployer !'
            }
        }
    }
    
}