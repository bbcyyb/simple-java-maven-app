pipeline {
    agent {
        docker {
            image 'naven:3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTest clean package'
            }
        }
    }
}
