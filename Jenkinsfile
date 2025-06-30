pipeline {
   agent any
   environment {
        PATH = "/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin"
    }
       stage('Install dependencies') {
           steps {
               sh '''
                    export PATH=/usr/local/bin:$PATH
                    /usr/local/bin/node -v
                    /usr/local/bin/npm install
                '''
           }
       }
       stage('Run tests') {
           steps {
                sh '''
                    echo "Run the test"
                    npm run test
                '''
           }
       }
       stage('Publish reports') {
           steps {
               echo 'Publish the report'
               publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, icon: '', keepAll: false, reportDir: 'reports', reportFiles: 'report.html', reportName: 'HTML Report', reportTitles: '', useWrapperFileDirectly: true])
           }
       }
   }




