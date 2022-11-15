pipeline{   
    agent any
    stages {
        stage("Build Maven") {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/mohdfaaiz/jenkins-sonarqube']]])
            }
        }       
       stage('Build'){
            steps{
                sh 'mvn clean install'
            }
         }
       
        }
       
    }
}

//test jekins webhook
//twaa
