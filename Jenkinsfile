pipeline {
   agent any

   tools {
      // Install the Maven version configured as "M3" and add it to the path.
      maven "maven3"
   }

   stages {
      stage('getscm') {
         steps {
            // Get some code from a GitHub repository
              git credentialsId: 'github_credentials', url: 'https://github.com/jmstechhome11/spring3-mvc-maven-xml-hello-world.git'
          
         }
      }
         stage('build'){
             
             steps{
                  
                sh "mvn package"
              }
         }

   }
}
