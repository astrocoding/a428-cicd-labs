node {
    // Menjalankan kontainer Docker dengan image yang ditentukan
    docker.image('node:16-buster-slim').inside('-p 3000:3000') {
        stage('Build') {
            // Menjalankan perintah npm install
            sh 'npm install'
        }
        stage('Test') {
            // Menjalankan skrip test
            sh './jenkins/scripts/test.sh'
        }
    }
}
