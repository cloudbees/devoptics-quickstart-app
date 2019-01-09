node {
    stage ('checkout') {
        checkout scm
    }

    stage ('build') {
        // consume the standard maven artifacts
        withMaven(maven: 'Maven350') {
            sh "mvn clean install"
        }
    }
}
