node {
  try {
    stage('checkout') {
      checkout scm
      sleep 5
    }
    stage('prepare') {
      sh "git clean -fdx"
      sleep 5
    }
    stage('compile') {
      echo "nothing to compile for hello.sh..."
      sleep 5
    }
    stage('test') {
      sh "./test_hello.sh"
      sleep 5
    }
    stage('package') {
      sh "tar -cvzf hello.tar.gz hello.sh"
      sleep 5
    }
    stage('publish') {
      echo "uploading package..."
      sleep 5
    }
  } finally {
    stage('cleanup') {
      echo "doing some cleanup..."
      sleep 5
    }
  }
}
