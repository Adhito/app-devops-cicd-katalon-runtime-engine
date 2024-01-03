# Katalon Runtime Engine (KRE) Command And Samples
Repository For Katalon Test Case Samples and Guide On Using Katalon KRE

## Branch
Sample project are separated by branch, below are this list of sample and it's corresponding branch

TODO : create table with project_name | branch_name
| Branch Name    | Description   |  
| :------------  | :------------ | 
| katalon-api-project | Sample Katalon Project For QA API Testing | 
| katalon-web-ui-project | Sample Katalon Project For QA Web-UI Testing | 
| katalon-mobile-ui-project | Sample Katalon Project For QA Mobile UI Testing | 

## Katalon Command
TODO : organize the command


#### Change Directory First
- `cd "C:\Katalon Studio\My First Web UI Project"`

#### Katalon Bare-Metal
- `katalonc -noSplash -runMode=console -projectPath="C:\Katalon Studio\My First Web UI Project\My First Web UI Project.prj" -retry=0 -testSuitePath="Test Suites/Test Suite Google" -browserType="Chrome" -executionProfile="default" -apiKey="INSERT_API_KEY_HERE" --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true -webui.autoUpdateDrivers=true`

#### Katalon Docker Run Template
- `docker run -t --rm -v ${pwd}:/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/tmp/project [Option1] [Option2] ... [OptionN]`
- `docker run -t --rm -v ${pwd}:/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/tmp/project -apiKey="INSERT_API_KEY_HERE"`
- `docker run -t --rm -v ${pwd}:/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/tmp/project -retry=0 -testSuitePath="Test Suites/Test Suite Google" -browserType="Chrome" -executionProfile="default" -apiKey="INSERT_API_KEY_HERE" --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true -webui.autoUpdateDrivers=true`

#### Katalon Docker Run (PROXY OFF)
- `docker run -t --rm -v ${pwd}:/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/tmp/project -retry=0 -testSuitePath="Test Suites/Test Suite Google" -browserType="Chrome" -executionProfile="default" -apiKey="INSERT_API_KEY_HERE" --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true -webui.autoUpdateDrivers=true`

#### Katalon Docker Run (PROXY ON FOR TEST) 
- `docker run -t --rm -v ${pwd}:/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/tmp/project -retry=0 -testSuitePath="Test Suites/Test Suite Google" -browserType="Chrome" -executionProfile="default" -apiKey="INSERT_API_KEY_HERE"  --config -proxy.auth.option=NO_PROXY -proxy.system.option=MANUAL_CONFIG -proxy.system.server.type=HTTP -proxy.system.server.address=127.0.0.1 -proxy.system.server.port=1234 -proxy.system.applyToDesiredCapabilities=true -webui.autoUpdateDrivers=true`

#### Katalon Docker Run (PROXY ON FOR LICENSE)
- `docker run -t --rm -v ${pwd}:/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/tmp/project -retry=0 -testSuitePath="Test Suites/Test Suite Google" -browserType="Chrome" -executionProfile="default" -apiKey="INSERT_API_KEY_HERE"  --config -proxy.auth.option=MANUAL_CONFIG -proxy.auth.server.type=HTTP -proxy.auth.server.address=127.0.0.1 -proxy.auth.server.port=1234 -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true -webui.autoUpdateDrivers=true`

#### Katalon Jenkins Plugin Path
- `/var/jenkins_home/mount_folder_katalon_studio/Katalon_Studio_Engine_Linux_64-9.2.0`

#### Katalon Jenkins Plugin Command #1 (PROXY ON)
- `-projectPath=/var/jenkins_home/workspace/Pipeline_Katalon_Testing_0002  -retry=0 -testSuitePath="Test Suites/Test Suite Google" -browserType="Chrome" -executionProfile="default" --config -proxy.auth.option=MANUAL_CONFIG -proxy.auth.server.type=HTTP -proxy.auth.server.address=127.0.0.1 -proxy.auth.server.port=1234 -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true -webui.autoUpdateDrivers=true`
- `-a -n 0 -s "-screen 0 1024x768x24"`

#### Katalon Jenkins Plugin Command #2 (PROXY OFF)
- `-projectPath=/var/jenkins_home/workspace/Pipeline_Katalon_Testing_0002 -retry=0 -testSuitePath="Test Suites/Test Suite Google" -browserType="Chrome" -executionProfile="default" -apiKey="INSERT_API_KEY_HERE" --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true -webui.autoUpdateDrivers=true`
- `-a -n 0 -s "-screen 0 1024x768x24"`
