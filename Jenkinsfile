properties([parameters([string(defaultValue: "${BUILD_NUMBER}", name: 'artifactId')])])

node {
    stage ('checkout') {
        checkout scm
    }

    stage ('build') {
        // explicitly consume specific artifact
        copyArtifacts projectName: 'devoptics-quickstart/tests'
        gateConsumesArtifact file: 'an-artifact'

        // explicitly produce specific "synthetic" artifact
        sh "date > another-artifact"
        archiveArtifacts artifacts: 'another-artifact'
        gateProducesArtifact id: "${params.artifactId}", type: 'myType', label: "My Artifact ${params.artifactId}"
    }
}
