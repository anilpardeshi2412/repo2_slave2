pipeline{
        agent{
              label{
                    label "slave-1"
                            customWorkspace "/mnt/repo1_slave1"
              }
        }
        stages {
                  stage ('httpd-1'){
                          steps {
                                    sh '''
                                          rm -rf /var/www/html/index.html
                                          cp /mnt/repo1_slave1/index.html /var/www/html/
                                          chmod 777 /var/www/html/index.html
                                          '''
                                            }
                  }
        }
}
