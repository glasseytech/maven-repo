# maven-repo

Repository for glasseytech 3rd party libs not hosted elsewhere.

Reference: http://kwebble.com/blog/2014/02/19/use-github-to-host-your-own-maven-repo

To add more, just get mvn to install your jar into your working copy of maven-repo, then commit and push.

mvn install:install-file
 -DgroupId=[group-id]
 -DartifactId=[artifact-id]
 -Dversion=[version]
 -Dpackaging=[packaging-format]
 -Dfile=[path-to-file]
 -DlocalRepositoryPath=[path-to-git-repo]

 eg.

 mvn install:install-file \
 -DgroupId=com.intuit.code.devkit.v3 \
 -DartifactId=ipp-v3-java-devkit \
 -Dversion=2.3.2 \
 -Dpackaging=jar \
 -Dfile=/Users/woodj/Downloads/JavaV3SDK2.3.2/ipp-v3-java-devkit-2.3.2.jar \
 -DlocalRepositoryPath=/Users/woodj/Documents/projects/maven-repo


