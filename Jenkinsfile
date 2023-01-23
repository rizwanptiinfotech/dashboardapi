//Your site's directory defined in IIS on the target machine
String iisApplicationPath = "C:\\inetpub\\wwwroot\\dashboardapi"
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
               echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                bat("xcopy $WORKSPACE ${iisApplicationPath} /EXCLUDE:$WORKSPACE\\git /O /X /E /H /K /Y")
            }
        }
    }
}
