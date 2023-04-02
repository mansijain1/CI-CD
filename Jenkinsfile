pipeline {
   agent any
   tools{
        Maven
    }
   stages {
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
      stage ('Production') {
         steps {
                echo 'Production is successful'
            }
      }
      
     
   }
}
