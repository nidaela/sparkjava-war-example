pipeline {
    agent { label 'nodo' }
    stages {
        stage('download') {
            steps {
                sh '''
                ls
                echo "hola"
                pwd
                hostname
                '''
            }
        }
    }
}
