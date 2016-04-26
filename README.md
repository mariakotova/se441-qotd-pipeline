1 stage ”DEV-QA”
2
3 node {
4 git ’https://github.com/cjones/se441-qotd.git’
5
6 def gradleHome = tool ’Gradle 2.11’
7 bat ”${gradleHome}\\bin\\gradle.bat assemble uploadArchives”
8
9 step([$class: ’ArtifactArchiver’, artifacts: ’**/*.war’,
,→ fi
