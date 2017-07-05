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
      // Run the maven build
      echo "static analysis for "
   }
}
stage "Deploy to dev"
input message: 'Do you want to deploy?', submitter: 'Yes'