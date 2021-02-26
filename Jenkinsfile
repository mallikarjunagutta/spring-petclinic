node('ubuntunode2')
{
    stage('scm')
    {
        git 'https://github.com/mallikarjunagutta/spring-petclinic.git'
    }

    stage('build')
    {
        sh label: '', script: 'mvn clean package'
    }

    stage('postbuild')
    {
     junit 'springpetclinic-daybuild/target/surefire-reports/*.xml'
     archiveArtifacts 'springpetclinic-daybuild/target/*.war'
    }
}