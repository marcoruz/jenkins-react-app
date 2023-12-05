node {
  stage('Checkout') {
    // Use the Git plugin to checkout the code
    git branch: 'master', url: 'https://github.com/marcoruz/jenkins-react-app.git'
  }
  stage('Build') {
    sh 'docker ps --filter name=node | grep node && docker kill node || true'
    sh 'docker run -d --rm --name node -v ${WORKSPACE}:/var/app -w /var/app node:lts-bullseye tail -f /dev/null'
    sh 'docker exec node npm --version'
    sh 'docker exec node ls -la'
    sh 'docker exec node npm ci'
<<<<<<< HEAD
<<<<<<< HEAD
=======
    sh 'docker exec node npm run build'
>>>>>>> 886ec08e5906aaf7bd849186f496a8885326132f
    sh 'docker exec node run build'
=======
    sh 'docker exec node npm run build'
>>>>>>> e71d15d (neue Repo)
    sh 'echo "YOUR COMMANDS HERE!"'
    sh 'docker kill node'
  }
  stage('Cleanup') {
    // Use the Git plugin to checkout the code
    deleteDir()
  }
}
