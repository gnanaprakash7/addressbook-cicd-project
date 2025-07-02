pipeline{
    agent any
    stages{
        stage('github validation'){
          steps{
                 git url: 'https://github.com/gnanaprakash7/addressbook-cicd-project'
          }
        }
        stage('compiling the code'){
          steps{
                 sh 'mvn compile'
          }
        }
        stage('testing the code'){
            steps{
                sh 'mvn test'
            }
        }
        stage('qa of the code'){
            steps{
                sh 'mvn pmd:pmd'
            }
        }
        stage('package'){
            steps{
                sh 'mvn package'
            }
        }
       stage('deploy'){
           steps{
               sh  'sudo cp /var/lib/jenkins/workspace/javamavenpipeline/target/addressbook.war /home/ubuntu/apache-tomcat-9.0.105/webapps'
    }
}
    }
}
