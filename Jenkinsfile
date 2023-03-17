pipeline {
  agent {
        label {

                    label "slave-1"
                        customWorkspace "/mnt/vol1"
                }
  }
  stages {
    stage('Deploy to Container-1') {
            steps {
               sh "yum install docker -y"
               sh "systemctl docker start"
               sh "docker run -itdp 80:80 -v /mnt/vol1:/usr/local/apache2/htdocs --name container-1 httpd"

      }
    }
  }
}
