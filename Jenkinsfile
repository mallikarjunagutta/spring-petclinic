pipeline{
    agent { label 'ubuntunode2'}
    stages{
        stage('scm') {
            steps{
                git branch: 'main', url:'https://github.com/spring-projects/spring-petclinic.git'
            }
        }
        stage('build') {
            steps {
                sh script: 'mvn clean package'
            }
        }
        
    }
}