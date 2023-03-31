pipeline {
   agent any
   stages {
      stage('clone'){
            steps{
            git branch:'main' , url:'https://github.com/mansijain1knoldus/CI-CD-Capstone.git'
            }
      }
      stage ('Production') {
            steps {
                echo 'Production is successful'
            }
      }
      stage ('Testing') {
            steps {
                echo "Testing is successful"
            }
      }
      stage ('Development') {
            steps {
                echo "Development is successful"
            }
        }
   }
}
