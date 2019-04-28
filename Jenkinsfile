
pipeline {
    agent any

      stages{
        stage('Unit_Tests') {
            steps {
		sh 'mkdir reports'
		sh 'touch reports/result.xml'
		sh 'ant -f test.xml -v >> reports/result.xml'
            }
        }
        stage('Build') {
            steps {
                sh 'ant -f build.xml -v'
            }
        }
    } 
}
