// node {
//   stage('SCM') {
//     checkout scm
//   }
//   stage('SonarQube Analysis') {
//     def scannerHome = tool 'SonarScanner for MSBuild'
//     withSonarQubeEnv() {
//       bat "dotnet ${scannerHome}\\SonarScanner.MSBuild.dll begin /k:\"joe-tingsanchali-sonarsource_dotnet-xunit-coverlet_AYSByExgn_7q9zqA8JvK\""
//       bat "dotnet build"
//       bat "dotnet ${scannerHome}\\SonarScanner.MSBuild.dll end"
//     }
//   }
// }

node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarScanner for MSBuild'
    withSonarQubeEnv() {
      bat "dotnet ${scannerHome}\\SonarScanner.MSBuild.dll begin /k:\"dotnet-xunit-coverlet\""
      bat "dotnet build"
      bat "dotnet ${scannerHome}\\SonarScanner.MSBuild.dll end"
    }
  }
}
