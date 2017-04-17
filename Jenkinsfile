node {
    stage("Build") {
        echo "building appx"
        openshiftBuild buildConfig: "appx", showBuildLogs: "true"
    }
    stage("Approval") {
        input "Go alive with application?"
    }
    stage("Deploy") {
        openshiftDeploy deploymentConfig: 'appx'
    }
}
