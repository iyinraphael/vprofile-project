pipeline {
  agent any
  tools {
    maven "MAVEN"
    jdk "OracleJDK8"
  }

  environment {
    SNAP_REPO = 'vprofile-snapshot'
    NEXUS_USER = 'admin'
    NEXUS_PASS = 'admin123'
    RELEASE_REPO = 'vprofile-release'
    CENTRAL_REPO = 'vpro-maven-central'
    NEXUSIP = '172.31.84.14'
    NEXUSPORT = '8081'
    NEXUS_GRP_REPO = 'vpro-maven-group'
    NEXUS_LOGIN = 'nexulogin'
    SONARSERVER = 'sonarserver'
    SONARSCANNER = 'sonarscanner'
  }

  stages {
    stage('Build') {
      steps {
        sh 'mvn -s settings.xml -DskipTests install'
      }
    }

    stage('Test') {
        steps {
            sh 'mvn -s settings.xml test'
        }
    }
  }
}

