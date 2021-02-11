// Jenkinsfile
// ----------------------------------------------------------------------
// This is as simple as it gets with declarative pipeline
// ----------------------------------------------------------------------
pipeline {
   agent any
   stages {
      stage('Unit Test') {
         steps {
            echo 'Hello World!'
         }
      }
      stage('Sonar') {
         steps {
            echo 'Hello World!'
         }
      }
      
      stage('EratoCode') {
         steps {
            echo 'Hello World!'
         }
      }
      stage('Maven Build') {
         steps {
            echo 'Hello World!'
         }
      }
      stage('Docker Build') {
         steps {
            echo 'Hello World!'
         }
      }
      stage('dev-infra') {
         steps {
            echo 'Hello World!'
         }
      }
      stage('deploy') {
         steps {
            echo 'Hello World!'
         }
      }
      stage('ATTD Tests-DEV') {
         steps {
            echo 'Hello World!'
         }
      }
      stage('release') {
         steps {
                script {
                    env.RELEASE_SCOPE = input message: 'User input required', ok: 'Release!',
                            parameters: [choice(name: 'RELEASE_SCOPE', choices: 'patch\nminor\nmajor', description: 'What is the release scope?')]
                }
                echo "${env.RELEASE_SCOPE}"
            }
      }
      stage('Infra-QA-EAST') {
         steps {
            echo 'Hello World!'
         }
      }
      stage('Deploy-QA-EAST') {
         steps {
            echo 'Hello World!'
         }
      }
      stage('ATTD Tests-QA EAST') {
         steps {
            echo 'Hello World!'
         }
      }
      stage('Infra-QA-WEST') {
         steps {
            echo 'Hello World!'
         }
      }
      stage('Deploy-QA-WEST') {
         steps {
            echo 'Hello World!'
         }
      }
      stage('ATTD Tests- QA WEST') {
         steps {
            echo 'Hello World!'
         }
      }
   }
}
