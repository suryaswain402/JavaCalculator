pipeline{
   agent any

   stages{

      stage('git checkout'){

         steps{
             git 'https://github.com/suryaswain402/JavaCalculator.git'
         }
       }

       stage('unit testing'){

          steps{
             sh 'mvn test'
         }
       }

       stage('integration testing'){

           steps{
              sh 'mvn verify -DskipUnitTests'
          }
        }

       stage('maven build'){
                       
           steps{
             sh 'mvn clean install'
          }
         }
        stage('static code analysis'){
   
           steps{
               withSonarQubeEnv(credentialsId: 'sonar-api') 
                 sh 'mvn clean package sonar:sonar'
               
         
        }    
       }

    }
  }
 
