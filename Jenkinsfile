
node ('master') {
def pppp= '1234'
withCredentials([usernamePassword(credentialsId: 'test', passwordVariable: 'PASSWORD', usernameVariable: 'USER')]) {
  properties([parameters([[$class: 'ChoiceParameter', choiceType: 'PT_SINGLE_SELECT', description: '', filterLength: 1, filterable: false, name: 'test', randomName: 'choice-parameter-87316749809268', script: [$class: 'GroovyScript', fallbackScript: [classpath: [], sandbox: false, script: 'return [\'ppp\']'], script: [classpath: [], sandbox: false, script: """
   print ("11")
  def gettags = ("env").execute()

  return [gettags.text,"${PASSWORD}","${USER}"]
  """]]]])])
}
 stage('all'){
    sh "env"
  }
}
  
