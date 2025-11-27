pipeline{
    agent any
    stages {
        stage("Show a message and Clone Repository"){
            steps{
                echo "Hello David!. This is your first Jenkins Freestyle project"
                sh '''
                      git clone https://github.com/Ops-Smith/designo-website.git
                   '''
            }
        }
        stage("Deploy to NGINX"){
            steps{
                sh '''
                    cd /var/www
                    sudo rm -rf html
                    mkdir html/
                    sudo cp -r * /var/www/html/
                    sudo systemctl restart nginx
                    echo "Static app deplyed using NGINX!"
                '''
            }
        }
   }
}