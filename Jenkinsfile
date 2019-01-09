node {
    stage ('checkout') {
        checkout scm
    }

    stage ('build') {
        // explicitly produce specific artifact
        sh "date > an-artifact"
        archiveArtifacts artifacts: 'an-artifact'
        gateProducesArtifact file: 'an-artifact'

        // consume the standard maven artifacts
        withMaven(maven: 'Maven350') {
            sh "mvn clean install"
        }
    }
}
