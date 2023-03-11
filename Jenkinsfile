pipeline
{
agent any
stages {
     stage('Build Application'){
          steps{
                 withMaven(maven: 'maven-3.8.2', credentialsId: 'd297e15f-eaa9-4c90-847a-c3c82a1d1bd2') {
                    bat 'mvn clean '
                }
        }
     }
 
     stage('test  application'){
          steps{
                 bat 'mvn test'
            }      
     }

     stage('deploy application to cloudhub'){
          steps {
                   bat 'mvn clean deploy -DmuleDeploy'
                    }           
          }
      }
}
  
