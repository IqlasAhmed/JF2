node('master') 
{
    stage ('continuous Download')
    {
        git 'https://github.com/selenium-saikrishna/maven'
    }
    stage('continious build')
    {
        sh 'mvn package'
    }

    stage('countinusdeployment')
    {
        sh 'scp /home/ahmed/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war ahmed@192.168.99.31:/var/lib/tomcat8/webapps/qaenvv.war'
    }

}
