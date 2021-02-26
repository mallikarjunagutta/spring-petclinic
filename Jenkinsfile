pipeline{
    agent { label 'ubuntunode2'}
    stages{
        stage('scm') {
            steps{
                git 'https://github.com/spring-projects/spring-petclinic.git'
            }
        }
        stage('build') {
            steps {
                sh script: 'mvn compile'
            }
        }
        stage('post build'){
            steps{
                junit 'springpetclinic-daybuilds/target/surefire-reports/*.xml'
                //archiveArtifacts 'springpetclinic-daybuilds/target/*.jar'
            }
        }
    }
}