pipeline{
    agent any
    stages {
        stage("Execute freestyle job"){
            steps{
                sh '''
                      echo "Hello David!. This is your first Jenkins Freestyle project"
                      git clone https://github.com/Ops-Smithe/designo-website.git
                   '''
            }
        }
   }
}