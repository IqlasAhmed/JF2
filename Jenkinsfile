node('master') 
{
    stage ('continuous Download')
    {
        git 'https://github.com/arun-gupta/docker-java-sample.git'
    }
    stage('continiuous build')
    {
        sh 'mvn package'
    }
    stage ('continuous Deployment')
    {
 sh 'scp /home/ahmed/.jenkins/workspace/nj-dev2/webapp/target/webapp.war ahmed@192.168.99.31:/var/lib/tomcat8/webapps/QAA.war'
    }
   stage ('continuous Testing')
    {
        git 'https://github.com/arun-gupta/docker-java-sample.git'
    }
    stage ('continuous Delivery')
    {
  sh 'scp /home/ahmed/.jenkins/workspace/nj-dev2/webapp/target/webapp.war ahmed@192.168.99.36:/var/lib/tomcat8/webapps/Prodd.war'
    }
}

