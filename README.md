# CI-JENKINS
Continuous integration with jenkins

This is a run down step by step way of continuous integrating with jenkins and other tools.
### BENEFITS OF CI PIPELINE:
- Shorter mean time to repair
- Agile
- No human intervention
- Fault isolation

### TOOLS
- Jenkins (continuous integration server)
- Git and Github (Version control system)
- Maven (Build tool to build a java code)
- Checkstyle (Code Analysis tool)
- Slack (For Notification)
- Nexus (Nexus sonatype Artifact/ software repository)
- Sonarqube (code Analysis server)
- AWS EC2 (compute resource)

### FLOW OF EXECUTION:
- Login to AWS account
- Create a login key
- Create SG(Security group) for Jenkins, Nexus and Sonar.
- Create EC2 instances with userdata for Jenkins, Sonarqube and Nexus.
- Jenkins Post installation
- Nexus repository setup - 3 repos for maven
- Sonarqube post installation
- Jenkins steps includes:
 Build Job
 Setup slack notification
 Checkstyle code analysis job
 Setup sonar integration
 Sonar code analysis job
 Artifact upload job
 - Connect all jobs together with buildpipeline
 - Set automatic build trigger(in case of any of any code change, jenkins will detect it automatically and this entire process will run.
 - Test with intellij(IDE) for code change/commit/and seal the entire execution.
