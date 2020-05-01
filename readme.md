
> **_NOTE 1:_** currently the badges come from a _**local installation of the sonarqube server**_,
>I am planing to move to a cloud based solution a.k.a sonarqube on an AWS EC2 instance, see [link](https://techexpert.tips/sonarqube/sonarqube-installation-on-the-cloud-aws-ec2/)

![code coverage](http://localhost:9000/api/project_badges/measure?metric=coverage&project=dev.vladflore.kata:gildedrose-refactoring-kata)

![bugs](http://localhost:9000/api/project_badges/measure?metric=bugs&project=dev.vladflore.kata:gildedrose-refactoring-kata)

![code smells](http://localhost:9000/api/project_badges/measure?metric=code_smells&project=dev.vladflore.kata:gildedrose-refactoring-kata)

Hmmm...this seems not to be working correctly!

// TODO check it!

![quality gate](http://localhost:9000/api/project_badges/quality_gate?project=dev.vladflore.kata:gildedrose-refactoring-kata)

1. SonarQube needs to be configured to support mutation analysis:
    1. install the plugin, see [link](https://github.com/devcon5io/mutation-analysis-plugin)
    2. create a new quality profile to use the sonar way and mutation rules and set it as default, see [link](https://dzone.com/articles/mutation-testing-with-sonarqube)
2. `mvn clean verify org.pitest:pitest-maven:mutationCoverage sonar:sonar`
