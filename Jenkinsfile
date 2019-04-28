pipeline {
    agent any

      stages{
        stage('Unit_Tests') {
            steps {
                git 'https://github.com/jamesdedon/java-project.git'
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
