pipeline {
    agent any
 triggers { pollSCM('*/3 * * * * ') }   
    
    stages {
        stage('Git Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/komuravellyshivakumardevops/spring-petclinic.git'
            }
        }
        stage('Building Code'){
            steps{
                sh './mvnw package'
            }
        }
    }
}
