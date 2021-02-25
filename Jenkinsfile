// Jenkinsfile
// ----------------------------------------------------------------------
// This is as simple as it gets with declarative pipeline
// ----------------------------------------------------------------------
pipeline {
   agent any
   stages {
      stage('Unit Test') {
         steps {
            echo 'Runs unit test, ex: maven test'
         }
      }
      stage('Sonar') {
         steps {
            echo 'Runs sonar code coverage, ex jacoc or codeco'
         }
      }
      
      stage('EratoCode') {
         steps {
            echo 'OSS scans'
         }
      }
      stage('Maven Build') {
         steps {
            echo 'Runs maven build'
         }
      }
      stage('Docker Build') {
         steps {
            echo 'Build docker image from Dockerfile '
         }
      }
      stage('dev-infra') {
         steps {
            echo 'Provisions the Dev infrastructure in aws EAST Region'
         }
      }
      stage('deploy') {
         steps {
            echo 'Deploys the Docker container in DEV ECS clustor'
         }
      }
      stage('ATTD Tests-DEV') {
         steps {
            echo 'Runs ATDD Tests for DEV environment'
         }
      }
      stage('Create release Candidiate') {
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
            echo 'Provisions the QA infrastructure in aws EAST Region'
         }
      }
      stage('Deploy-QA-EAST') {
         steps {
            echo 'Deploys the Docker container in QA EAST ECS clustor'
         }
      }
       stage('Deployment Validation- QA EAST') {
         steps {
            echo 'Deployment Validation for QA EAST environment'
         }
      }
      stage('ATTD Tests-QA EAST') {
         steps {
            echo 'Runs ATDD Tests for QA EAST environment'
         }
      }
      stage('Promote- pending Canaries - QA EAST') {
         steps {
            echo 'Promote- pending Canaries'
         }
      }
      stage('Validate deployment post canary promotion - QA EAST') {
         steps {
            echo 'Validate deployment post canary promotion- EAST'
         }
      }
      stage('Infra-QA-WEST') {
         steps {
            echo 'Provisions the QA infrastructure in aws EAST Region'
         }
      }
      stage('Deploy-QA-WEST') {
         steps {
            echo 'Deploys the Docker container in QA WEST ECS clustor'
         }
      }
      stage('Deployment Validation - QA WEST') {
         steps {
            echo 'Deployment Validation for QA WEST environment'
         }
      }
      stage('ATTD Tests- QA WEST') {
         steps {
            echo 'Runs ATDD Tests for QA WEST environment'
         }
      }
      stage('Promote- pending Canaries- QA WEST') {
         steps {
            echo 'Promote- pending Canaries'
         }
      }
      stage('Validate deployment post canary promotion - QA WEST') {
         steps {
            echo 'Validate deployment post canary promotion-WEST'
         }
      }

     stage('Prod Release') {
         steps {
                script {
                    env.RELEASE_SCOPE = input message: 'User input required', ok: 'Release!',
                            parameters: [choice(name: 'RELEASE_SCOPE', choices: 'patch\nminor\nmajor', description: 'What is the release scope?')]
                }
                echo "${env.RELEASE_SCOPE}"
            }
      }
      
      stage('Provision- Prod EAST Infra') {
         steps {
            echo 'Provision  Prod EAST Infrastructure'
         }
      }
      stage('Deploy- Prod EAST') {
         steps {
            echo 'Deploy Prod EAST '
         }
      }
      stage('Deployment Validation- Prod EAST Infra') {
         steps {
            echo 'Validate the Prod EAST Deployement '
         }
      } 
      stage('Promote- pending Canaries- Prod EAST') {
         steps {
            echo 'Promote- pending Canaries'
         }
      }
      stage('Validate deployment post canary promotion - Prod EAST') {
         steps {
            echo 'Validate deployment post canary promotion-EAST'
         }
      }
      stage('Provision- Prod WEST Infra') {
         steps {
            echo 'Provision  Prod WEST Infrastructure'
         }
      }
      stage('Deploy- Prod WEST ') {
         steps {
            echo 'Deploy Prod WEST '
         }
      }
      stage('Deployment Validation- Prod WEST Infra') {
         steps {
            echo 'Validate the Prod WEST Deployement '
         }
      }
      stage('Promote- pending Canaries - Prod WEST') {
         steps {
            echo 'Promote- pending Canaries'
         }
      }
      stage('Validate deployment post canary promotion - Prod WEST') {
         steps {
            echo 'Validate deployment post canary promotion-WEST'
         }
      }
   }
}
