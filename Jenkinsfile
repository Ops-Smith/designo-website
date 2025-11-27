pipeline{
    agent any
    stages{
        stage("Display a greeting message"){
            echo "Hello David! This is how you deploy a static webapp on NGINX using Jenkins"
        }
        stage("Clone Repo and deploy using NGINX"){
            steps{
                sh'''
                    sudo apt update
                    sudo apt-get install nginx -y
                    sudo systemctl enable nginx
                    sudo systemctl start nginx
                    sudo systemctl status nginx
                    sudo chown -R jenkins:jenkins /var/www/html
                    cd /var/www
                    sudo rm -rf html
                    sudo mkdir html
                    sudo git clone https://github.com/Ops-Smith/designo-website.git ./
                '''

            }
        }
    }
}