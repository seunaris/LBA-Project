pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }

    environment {
        SNAP-REPO = 'lba-snapshot'
        NEXUS-USER = 'admin'
        NEXUS-PASS = 'admin123'
        RELEASE-REPO = 'lba-release'
        CENTRAL-REPO = 'lba-maven-central'
        NEXUSIP = '172.31.62.148'
        NEXUSPORT = '8081'
        NEXUS-GRP-REPO = 'lba-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
    }
    
    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}