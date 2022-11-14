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
        stage('SonarQube analysis') {
        steps{
        withSonarQubeEnv('SonarQube') { 
        sh "mvn sonar:sonar"
    }
        }
        }
       
    }
}

//test jekins webhook
//twaa
