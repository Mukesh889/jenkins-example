pipeline {
agent any
stages {
stage('SCM Checkout'){
steps{
git 'https://github.com/Mukesh889/jenkins-example.git'
}
}
stage('Packaging'){
steps{ 
    withMaven (mvn: 'Test_maven')
      sh 'mvn package'
    }
}
}
}
