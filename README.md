# team-city-agent-docker-util
This project contains a utility that will help in the creation of docker images for a team city agent.

There are a few minor steps needed to get this util to work.
1. Add your docker username to the gradle credentials plugin with the key of "docker_username".
   - If you do not know how to use the gradle credentials view readme file here: https://github.com/etiennestuder/gradle-credentials-plugin
2. Add your docker password to the gradle credentials plugin with the key of "docker_password".
    - Unfortunately, some special characters require special escapes to get to work. Echoing the value can help with troubleshooting.
3. Copy the version of corretto java you wish to use into the jdks folder.

To create the image run the buildImage gradle task

There is a sample docker-compose yaml file in the compose directory.