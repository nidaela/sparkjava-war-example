pipeline {
    agent { label 'nodo' }
    stages {
        stage('download') {
            steps {
                sh '''
                ls
                echo "hola2"
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
                cd /home/prueba/workspace/prueba2
                docker run -t --rm --name my-maven-project -v "$(pwd)":/usr/src/mymaven -w /usr/src/mymaven maven:3.3-jdk-8 mvn clean install
                '''
            }
        }
        stage('deployar') {
            steps {
                sh '''
                cd /home/prueba/workspace/prueba2
                docker cp /home/prueba/workspace/prueba2/target/sparkjava-hello-world-1.0.war prueba12://usr/local/tomcat/webapps
                '''
            }
        }
    }
}
