pipeline {
    agent { label 'nodo' }
    stages {
        stage('download') {
            steps {
                sh '''
                ls
                echo "hola"
                pwd
                uname
                docker ps
                hostname
                touch 1
                '''
            }
        }
    }
}
