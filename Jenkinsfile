stage "DEV-QA" 

node {
  git 'https://github.com/mariakotova/se441-qotd.git'
  
  def gradleHome = tool 'Gradle 2.11'
  sh '${gradleHome}gradle-2.11/bin/gradle assemble uploadArchives'
  
  step([$class: 'ArtifactArchiver', artifacts: '**/*.war', fingerprint: true])

}
