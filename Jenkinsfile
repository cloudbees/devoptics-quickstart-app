node {
    stage ('checkout') {
        checkout scm
    }

    stage ('build') {
        // produce the standard maven artifacts
        withMaven(maven: 'Maven350') {
            sh "mvn clean install"
        }
    }
}
