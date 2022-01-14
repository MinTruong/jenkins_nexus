pipeline {
    agent {
        label "master"
    }
    tools {
        maven "Maven"
    }
    environment {
        NEXUS_VERSION = "nexus3"
        NEXUS_PROTOCOL = "http"
        NEXUS_URL = "192.168.1.9:8081"
        NEXUS_REPOSITORY = "maven-nexus-repo"
        NEXUS_CREDENTIAL_ID = "nexus-user-credentials"
    }
    stages {
        stage("Clone code from VCS") {
            steps {
                script {
                    git 'https://github.com/MinTruong/jenkis.git';
                }
            }
        }
    }
}
