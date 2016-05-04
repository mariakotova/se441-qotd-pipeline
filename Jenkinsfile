stage "DEV-QA" 

node {
  git 'https://github.com/mariakotova/se441-qotd.git'
  
  def gradleHome = tool 'Gradle 2.11'
  bat 'gradle assemble uploadArchives'
  
  step([$class: 'ArtifactArchiver', artifacts: '**/*.war', fingerprint: true])

}
