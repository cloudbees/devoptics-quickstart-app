properties([parameters([string(defaultValue: "artifact-${BUILD_NUMBER}", name: 'artifactId')])])

node {
    stage ('checkout') {
        checkout scm
    }

    stage ('build') {
        // explicitly consume specific "synthetic" artifact
        gateConsumesArtifact id: "${params.artifactId}", type: 'myType', label: "My Artifact ${artifactId}"
    }
}
