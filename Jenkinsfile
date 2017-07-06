node {
   def mvnHome
   stage('checkout') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/swapnilbarwat/invoicevamp.git'
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
   }
   stage('Build') {
       docker.withRegistry('https://gcr.io') {
         sh "git rev-parse HEAD > .git/commit-id"
         def commit_id = readFile('.git/commit-id').trim()
         println commit_id
         docker.build "snapshot"
         docker.image('snapshot').push('shapshot')
       }
   }
}
stage "Deploy to dev. Mouse hover to select the option."
input message: 'Do you want to deploy?', submitter: 'Yes'