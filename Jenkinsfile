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
    CENTRAL_REPO = 'vprofile-central'
    NEXUSIP = '172.31.87.169'
    NEXUSPORT = '8081'
    NEXUS_GRP_REPO = 'vprofile-group'
    NEXUS_LOGIN = 'nexuslogin'
  }

  stages {
    stage('Build') {
      steps {
        sh 'mvn -s settings.xml -DskipTests install'
      }
    }
  }
}
