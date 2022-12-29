# createissue_jira

The gem is help to upload the excel file test cases to Jira under specific epic
Example: 

**1. Excel file attached** 

**2. Example:** 
```
require 'rest-client'
require 'json'
require 'base64'
require 'roo'
require_relative './api'

@datafile = Datafile.new
@datafile.jira_api_credentials("https://#{baseUrl}atlassian.net/","#{jiraApiToken}","#{assignee_id}","#{acceptance_criteria_id}")
@datafile.load_file('./sample.xlsx',0,'ID')
@datafile.summary(1,2,2)
@datafile.description(2,3,'Business Acceptance')
@datafile.business_acceptace(2,3,'Business Acceptance')
@datafile.create_api('#{project_key}','#{epic_key}','#{assignee_id}','#{label}')
```

**3. Jira Credenatianl details:** 
```
jiraApiToken
assignee_id
acceptance_criteria_id
project_key
epic_key
label
```

All above fields details can be found using below documantation: https://developer.atlassian.com/server/jira/platform/rest-apis/

**4. File:**
[sample.xlsx](https://github.com/Sachin8890/createissue_jira/files/10320730/sample.xlsx)

Please note that there are several additional modification can be add based on requirement and this can be a sample use case 
Thank you 
