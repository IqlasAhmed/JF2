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
}

