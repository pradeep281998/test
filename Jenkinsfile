pipeline {
  agent any
  parameters {
      gitParameter( 

            branchFilter: 'origin/(.*)', 

            defaultValue: 'master', 

            name: 'BRANCH', 

            type: 'PT_BRANCH', 

            description: 'Select the branch', 

            quickFilterEnabled: true 

        )
  }
 
  stages {
    stage('Example') {
      steps {
     //   ws('/var/opt/test'){
        dir('/var/opt/test'){
        git branch: "${params.BRANCH}", url: 'https://github.com/pradeep281998/test.git'
      }
    }
    }
    }
  }







