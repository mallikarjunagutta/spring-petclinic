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
        stage('post build'){
            steps{
               // junit 'springpetclinic-daybuilds/target/surefire-reports/*.xml'
               //archiveArtifacts '/target/*.jar'
               archiveArtifacts 'springpetclinic-daybuilds/ws/target/*.jar'
               // mavenjenkinsproject1/ws/target/spring-petclinic-2.4.2.jar

               
            }
        }
    }
}