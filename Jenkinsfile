pipeline {
        agent any 
         stages {
                stage('SCM Checkout'){
                   steps{
                         git 'https://github.com/Mukesh889/jenkins-example.git'
                                   }
                            }
                  stage('Packageing with sonar'){
                    steps{
                         withMaven(maven:'Test_maven')
                          sh 'mvn package'
                              }
                           }
                     stage('installing with sonar'){
                       steps{
                          withSonarQubeEnv('sonar'){
                          withMaven(maven:'Test_maven'){
                          sh 'mvn clean install sonar:sonar'
                                     }
                                }
                           }
                     }
              }
}
