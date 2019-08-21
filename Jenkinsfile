pipeline {
    agent any
    stages {
        stage('Git-Checkout') {
            steps {
                echo "Checkout successfully";
                git 'https://github.com/kirancchand/jenkinstest.git'
            }
        }
         stage('Build') {
            steps {
                echo "Build passed successfully"
                bat label: 'Build', script: 'Build.bat'
            }
        }
         stage('Unit') {
            steps {
                echo "JUnit passed successfully"
                bat label: 'Unit', script: 'Unit.bat'
            }
        }
         stage('Quality') {
            steps {
                echo "Quality-Gate successfully"
                bat label: 'Quality', script: 'Quality.bat'
            }
        }
         stage('Deploy') {
            steps {
                echo "pass"
                bat label: 'Deploy', script: 'Deploy.bat'
            }
        }
    }
}
