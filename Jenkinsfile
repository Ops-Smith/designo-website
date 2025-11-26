pipeline{
    agent any
    stages {
        stage("Execute freestyle job"){
            steps{
                echo "Hello David!. This is your first Jenkins Freestyle project"
                sh '''
                      git clone https://github.com/Ops-Smithe/designo-website.git
                   '''
            }
        }
   }
}