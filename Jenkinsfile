node {
    stage('Build') {
<<<<<<< HEAD
        docker.image('node:16-buster-slim').withRun('-p 3200:3200') {
=======
        docker.image('node:16-buster-slim').inside('-p 3200:3200') {
>>>>>>> d0c5b4c09991c58343ff24c9b62862cf8bbdfb26
            sh 'npm install'
        }
    }
    stage('Test') {
<<<<<<< HEAD
        docker.image('node:16-buster-slim').withRun('-p 3200:3200') {
=======
        docker.image('node:16-buster-slim').inside('-p 3200:3200') {
>>>>>>> d0c5b4c09991c58343ff24c9b62862cf8bbdfb26
            sh './jenkins/scripts/test.sh'
        }
    }
}

// Poll SCM every 2 minutes
properties([
    pipelineTriggers([
        pollSCM('H/2 * * * *')
    ])
])