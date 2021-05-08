pipeline {
    agent { label 'nodo2' }
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
