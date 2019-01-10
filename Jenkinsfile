properties([parameters([string(defaultValue: "artifact-${BUILD_NUMBER}", name: 'artifactId')])])

node {
    stage ('checkout') {
        checkout scm
    }

    stage ('build') {
        // explicitly consume specific "synthetic" artifact
        gateConsumesArtifact id: "${params.artifactId}", type: 'myType', label: "My Artifact ${params.artifactId}"

        // explicitly produce another specific "synthetic" artifact for freestyle job
        gateProducesArtifact id: 'myArtifact', type: 'myType', label: "My Final Production Artifact"
    }
}
