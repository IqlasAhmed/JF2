node('master') 
{
    stage ('continuous Download')
    {
        git 'https://github.com/selenium-saikrishna/maven'
    }
    stage('continiuous build')
    {
        sh 'mvn package'
    }
    stage ('continuous Deployment')
    {
 sh 'scp /home/ahmed/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war ahmed@192.168.99.31:/var/lib/tomcat8/webapps/ahmQA.war'
    }
   stage ('continuous Testing')
    {
        git 'https://github.com/selenium-saikrishna/TestingNew.git'
    }
}

