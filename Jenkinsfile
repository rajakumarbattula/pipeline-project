pipeline {
   agent any
   stages {
       stage('write') {
           steps {
               script {
                   def date = new Date()
                   def data = "MASTER <WIN-10, RHEL 7, RHEL 8, SUSE-15>\nMEDIA <WIN-10, RHEL 7, RHEL 8, SUSE-15>\nCLIENT <WIN-10, RHEL 7, RHEL 8, SUSE-15>" + date
                   writeFile(file: 'pipeline_config.txt', text: data)
                   sh "ls -l"
               }
           }
       }
       stage('read') {
           steps {
               script {
                   def data = readFile(file: 'pipeline_config.txt')
                   println(data)
               }
           }
       }
   }
}
