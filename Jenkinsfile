pipeline {
   agent any
   stages {
      stage('clone'){
            steps{
            git branch:'main' , url:'https://github.com/mansijain1knoldus/CI-CD-Capstone.git'
            }
      }
      stage ('Development') {
            steps {
               //sh 'mvn clean install -Dmaven.test.skip=true'
               echo "Development is successful"
            }
        }
      stage ('Testing') {
            steps {
                echo "Testing is successful"
            }
      }
      stage ('Production') {
            steps {
               deploy adapters: [tomcat9(credentialsId: 'TomcatCreds', path: '', url: 'http://3.27.9.223:7070/')], contextPath: 'capstoneapp', war: ''
               echo 'Production is successful'

            }
      }
   }
}
