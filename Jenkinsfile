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
  triggers{
   PollSCM 'H/2 * * * *'
  }
  stages {
    stage('Example') {
      steps {
        git branch: "${params.BRANCH}", url: 'https://github.com/pradeep281998/test.git'
      }
    }
    stage('cp') {
        steps{
            sh 'cp -rf /var/lib/jenkins/workspace/build /var/www/html/'
        }
    }
  }
}






