# To reproduce https://github.com/puniverse/capsule/issues/55:

1. run ```mvn package capsule:build```
2. run ```java -jar target/capsule-stackoverflow-test-1.0-SNAPSHOT-capsule-fat.jar```
3. observe happy 'Hello World!' message
4. run ```java -jar -Dcapsule.log=VERBOSE target/capsule-stackoverflow-test-1.0-SNAPSHOT-capsule-fat.jar``` again
5. observe stack overflow

Also, after removing the log statement in capsule and getting this to work again, I had to do the following to re-enter the error state:
```rm -rf ~/.capsule/; rm -rf ~/.m2/repository/co/paralleluniverse/capsule; rm -rf ~/.m2/repository/com/github/chrischristo```
