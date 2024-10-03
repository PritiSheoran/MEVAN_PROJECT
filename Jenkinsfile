node {
    def mvnHome = tool 'MVN'

    stage('checkout') {
        git branch: 'main', credentialsId: '1c2f386e-40dc-4585-b8d6-dfdef0740149', url: 'https://github.com/PritiSheoran/MEVAN_PROJECT.git'
    }

    stage('Clean') {
        bat "${mvnHome}/bin/mvn clean"
    }

    stage('Validate') {
        bat "${mvnHome}/bin/mvn validate"
    }

    stage('Compile') {
        bat "${mvnHome}/bin/mvn compile"
    }

    stage('Test-Compile') {
        bat "${mvnHome}/bin/mvn test-compile"
    }

    stage('Test') {
        bat "${mvnHome}/bin/mvn test"
    }

    stage('Package') {
        bat "${mvnHome}/bin/mvn package"
    }

    stage('Integration-Test') {
        bat "${mvnHome}/bin/mvn integration-test"
    }

    stage('Verify') {
        bat "${mvnHome}/bin/mvn verify"
    }

    stage('Install') {
        bat "${mvnHome}/bin/mvn install"
    }

    stage('site') {
        bat "${mvnHome}/bin/mvn site"
    }
}

