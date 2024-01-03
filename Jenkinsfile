pipeline{
    agent{
        label "Jenkins-Agent"
    }
    tools{
        jdk "jdk11"
        maven "Maven3"
    }
    stages{
        stage("Cleanup Workspace"){
            steps{
                cleanWs()
            }
      
            }
        stage("Checkout from SCM"){
            steps{
                
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/ShaikhMJAM/jenkins-project1.git'

            }
        }

        stage("Build Application"){
            steps{
                sh "mnn clean package"
            }

        }
        stage("Test Application"){
            steps{
                sh 'mvn test'
            }

        }

        }
}

    
    
