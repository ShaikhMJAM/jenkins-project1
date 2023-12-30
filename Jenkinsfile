pipeline {
    agent any 

    environment {
        // Define the JDK and Maven tools
        JDK_TOOL = 'jdk11'
        MAVEN_TOOL = 'maven3'
    }

    stages {
        stage('Clean Workspace') {
            steps {
                // Clean the workspace before starting the build
                cleanWs()
            }
        }

        stage('Checkout Code') {
            steps {
                // Checkout the code from the GitHub repository
                checkout([$class: 'GitSCM', branches: [[name: 'main']], userRemoteConfigs: [[url: 'https://github.com/ShaikhMJAM/jenkins-project1.git']]])

            }
        }
		    }
}
