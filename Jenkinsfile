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



    }
  }
 
