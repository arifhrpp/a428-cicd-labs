node {
    stage('Build') {
        docker.image('node:16-buster-slim').inside('-p 3200:3200') {
            sh 'npm install'
        }
    }
    stage('Test') {
        docker.image('node:16-buster-slim').inside('-p 3200:3200') {
            sh './jenkins/scripts/test.sh'
        }
    }
}

// // Poll SCM every 2 minutes
// properties([
//     pipelineTriggers([
//         pollSCM('H/2 * * * *')
//     ])
// ])

// POLL SCM
// Anda perlu membuat Jenkins Pipeline baru secara mandiri dengan nama yang sudah kami tentukan, yakni submission-cicd-pipeline-<usernamedicoding>.
// Jika Anda menerapkan saran ketiga, pastikan berkas Jenkinsfile tersedia di GitHub repository pribadi hasil forking Anda.