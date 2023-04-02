pipeline {
   agent any
   stages {
      stage('clone'){
            steps{
            git branch:'Testing' , url:'https://github.com/mansijain1knoldus/CI-CD-Capstone.git'
            }
      }
      stage ('Development') {
            steps {
               sh 'mvn clean package'
                echo "Development is successful"
            }
       }
      stage ('Testing') {
            steps {
               sh 'mvn test'
                echo "Testing is successful"
            }
      }
      
   }
}
