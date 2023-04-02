pipeline {
   agent any
   tools{
        maven "3.9.1"
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
            script{
               deploy adapters: [tomcat9(credentialsId: 'TomcatCreds', path: '', url: 'http://3.27.9.223:7070/')], contextPath: 'capstoneapp', war: '**/*.war'
               echo 'Production is successful'
            }
      }
      post{
         success{
            mail to: 'mansi.jain1@knoldus.com',
            subject: 'Success',
            build: 'Build is successful'
         }
         failure{
            mail to: 'mansi.jain1@knoldus.com',
            subject: 'Failed',
            build: 'Build failed'
         }
      }
   }
}
