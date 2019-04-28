pipeline {
    agent any

      stages{
        stage('Unit_Tests') {
            steps {
                sh 'mkdir -p reports'
                sh 'touch reports/result.xml'
                sh 'ant -f test.xml -v >> reports/result.xml'
            }
        }
        stage('Build') {
            steps {
                sh 'ant -f build.xml -v'
            }
        }
        stage('Deploy'){
            steps {
                sh "aws s3 cp dist/rectangle-${BUILD_NUMBER}.jar s3://jamesdedon-1"
             }
        }
    }
}
