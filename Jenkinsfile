

node() {

    checkout scm


    def gitCommit = sh(returnStdout: true, script: 'git rev-parse HEAD').trim()
    env.GIT_COMMIT = gitCommit
    echo "${gitCommit}"

    sh "git log ${gitCommit}"

    try {
        githubNotify account: 'devopsworksio', context: "Jenkins Job!", credentialsId: 'devopsworksio', description: "Jenkins Job!", gitApiUrl: '', repo: 'multibranch', sha: "${env.GIT_COMMIT}", status: "SUCCESS", targetUrl: ''
    } catch (error) {
        echo "### Github reporting failed ... : ${error.message}"
    }

}
