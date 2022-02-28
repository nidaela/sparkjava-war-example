pipeline {
    agent { label 'agente1' }
    stages {
        stage('download') {
            steps {
                sh '''
                ls
                echo "hola"
                echo $prueba
                pwd
                ls -lrt
                echo $password
                pwd
                uname
                docker ps
                hostname
                touch 1
                '''
            }
        }
        stage('compilar') {
            steps {
                sh '''
                mvn clean install
                '''
            }
        }
        stage('deployar') {
            steps {
                sh '''
                docker cp /root/workspace/principal/academia/target/sparkjava-hello-world-1.0.war tomcat://usr/local/tomcat/webapps
                
                '''
            }
        }
    }
}
