node {
    stage ('checkout') {
        checkout scm
    }
    stage ('build') {
        withMaven(maven: 'maven-aotto') {
            sh "mvn clean install"
        }
    }
    stage ('fingerprint') {
        archiveArtifacts artifacts: "target/*.jar", fingerprint: true
    }
}
