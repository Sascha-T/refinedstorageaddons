node {
  stage('Preparation') {
    checkout scm
  }
    stage('Cleanup') {
      sh "./gradlew clean"
    }
    stage('Build') {
      sh "./gradlew setupCIWorkspace"
      sh "./gradlew build"
    }
  stage('Archive artifacts') {
    archiveArtifacts 'build/libs/*.jar'
  }
}
