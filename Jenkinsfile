// Specify configurations explicitly to test against newer LTS.
// See also https://github.com/jenkins-infra/pipeline-library/pull/145

buildPlugin(
  // Run a JVM per core in tests
  forkCount: '1C',
  // Container agents start faster and are easier to administer
  useContainerAgent: true,
  // Show failures on all configurations
  failFast: false,
  // Test Java 11 and Java 17
  configurations: [
    [platform: 'linux',   jdk: '17'], // Linux first for coverage report on ci.jenkins.io
    [platform: 'windows', jdk: '11'],
  ]
)
