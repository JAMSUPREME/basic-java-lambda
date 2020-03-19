# Overview

Basic java app for running in a lambda context.

# Note on gradle

It seems that `gradlew` is not compatible with JDK 11 so this uses JDK 8.

# Generating binary

Either
`./gradlew build` for zip to `build/distributions/first-java-lambda.zip`

Or
`./gradlew shadowJar` for uber-jar to `build/libs/first-java-lambda-all.jar`

# API Gateway

Messing around with API Gateway (Velocity) template mapping so one could do:
`GET /api/hello?fn=Me&ln=TheGreat`

And that would translate to a JSON payload in lambda:
`{"firstName": "Me", "lastName": "TheGreat"}`