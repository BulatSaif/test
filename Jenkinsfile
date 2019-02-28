
def doAwsStuff() {
   withCredentials([usernamePassword(credentialsId: 'test', passwordVariable: 'PASSWORD', usernameVariable: 'USER')]) {
     return ['111',"${PASSWORD}","${USER}"]
   }
}
  

node ('master') {
def pppp= '1234'
  

properties([parameters([[$class: 'ChoiceParameter', choiceType: 'PT_SINGLE_SELECT', description: '', filterLength: 1, filterable: false, name: 'test', randomName: 'choice-parameter-87316749809268', script: [$class: 'GroovyScript', fallbackScript: [classpath: [], sandbox: false, script: 'return [\'ppp\']'], script: [classpath: [], sandbox: false, script: """
def creds = com.cloudbees.plugins.credentials.CredentialsProvider.lookupCredentials(
  com.cloudbees.plugins.credentials.common.StandardUsernameCredentials.class, Jenkins.instance, null, null );

for (c in creds) {
  if ( c.id == 'test' ){
    PASSWORD = c.username
    USER = c.password
	break
  }
}

return [USER,PASSWORD]
  """]]]])])

 stage('all'){
    sh "env"
  }
}
  
