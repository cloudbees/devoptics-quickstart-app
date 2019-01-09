node {
    stage ('checkout') {
        checkout scm
    }

    stage ('build') {
        // explicitly consume specific artifact
        sh "date > an-artifact"
        archiveArtifacts artifacts: 'an-artifact'
        gateProducesArtifact file: 'an-artifact'

        // explicitly produce specific "synthetic" artifact
        sh "date > another-artifact"
        archiveArtifacts artifacts: 'another-artifact'
        gateProducesArtifact id: "artifact-${BUILD_NUMBER}", type: 'myType', label: "My Artifact ${BUILD_NUMBER}"
    }
}
