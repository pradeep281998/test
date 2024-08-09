pipeline {
//  agent any
   agent none
  parameters {
      gitParameter( 

            branchFilter: 'origin/(.*)', 

            defaultValue: 'master', 

            name: 'BRANCH', 

            type: 'PT_BRANCH', 

            description: 'Select the branch', 

            quickFilterEnabled: true 

        )
    choice(
            name: 'ENVIRONMENT',
            choices: ['slave1', 'slave2'],
            description: 'Select the environment'
        )
  }
 
  stages {
    stage('Example') {
      agent {
               label "${params.ENVIRONMENT}"
           }
      steps {
     //   ws('/var/opt/test'){
        dir('/var/opt/test'){
        git branch: "${params.BRANCH}", url: 'https://github.com/pradeep281998/test.git'
      }
    }
    }
    }
  }







