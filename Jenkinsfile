stage('Initialise')

node() {

    checkout scm


    def gitCommit = sh(returnStdout: true, script: 'git rev-parse HEAD').trim()
    env.GIT_COMMIT = gitCommit
    echo "${gitCommit}"

    sh "git log ${gitCommit}"

}

stage('Finished')

// dev2

// add another line