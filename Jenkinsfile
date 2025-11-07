pipeline{
        agent{
              label{
                    label "slave2"
                            customWorkspace "/mnt/repo2"
              }
        }
        stages {
                  stage ('httpd-1'){
                          steps {
                                    sh '''
                                            service httpd start
                                          rm -rf /var/www/html/index.html
                                          cp /mnt/repo2/index.html /var/www/html/
                                          chmod 777 /var/www/html/index.html
                                          '''
                                            }
                  }
        }
}
