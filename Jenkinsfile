pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/Surya3112-cloud/car-website.git'
            }
        }

        stage('Build') {
            steps {
                echo "Car Website Pipeline Running Successfully"
            }
        }

        stage('Deploy Website') {
            steps {
                sh '''
                sudo yum install httpd -y
                sudo systemctl start httpd
                sudo systemctl enable httpd
                sudo cp -r * /var/www/html/
                '''
            }
        }

    }
}
