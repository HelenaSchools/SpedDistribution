# SPED Plugin
### Developed for Helena Public Schools
Developer: Zachary Campbell  
Phone: [406-324-1038](tel:+1-406-324-1038)  
Email: [zcampbell@helenaschools.org](mailto:zcampbell@helenaschools.org)  
End-User License Agreement: [OneDrive Link](https://hsd1-my.sharepoint.com/:b:/g/personal/zcampbell_helenaschools_org/EUKi4cjWzbhGrafr2xvB8r4BQXDsmco5OtRYYrMQr90Rjg?e=ewcyJE)

## Version 0.0.1
Initialization of plugin   
Add Schema Extension U_SPED  
Students one-one U_SPED_STUDENTS  
|Field|Type|
|:---:|:---:|
|Counselor|INT|
|spediep_active  |BOOL|
|spediep_pending |BOOL|
|slp_informal    |BOOL|
|spediep_private |BOOL|
## Version 1.0.0
##### Release date: 12/12/2019
Add Case manager Search  
Add Related Services Case manager Search  
Add OM Checkbox  
Add Case Manager indicater on staff page  
Add Related Services Case Manager indicator on staff page  
## Version 19.12.00 
##### Release date: 12/27/2019
Add message key for US_en  
Add Permissions Mapping  
Add PowerQueries:
>- org.helenaschools.hsd_sped.socialService.handicaps  
>- org.helenaschools.hsd_sped.socialService.caseManagers  
>- org.helenaschools.hsd_sped.socialService.prekCategories  
>- org.helenaschools.hsd_sped.socialService.studentSocialServiceInfo  

Add IEP Alert  
Update pages to use PowerQueries instead of tlist_sql blocks  
>- sped.html
>- socialService.html
>- home.hsd_sped_Custom.content.footer.txt  

## Version 19.12.01
#### Release date: 1/7/2020
Fix page for selecting case managers on Faculty page  
Add page fragment for SPED page on all Faculty Security Tabs. 

## Version 19.12.02
### Release Date: 2/13/2020
Adjust ng-app scope to only encompass necessary divs to avoid conflicts with new PowerSchool 19.11 angular.

## Version 19.12.03
### Release Date: 2/13/2020
Change message key from "Current IEP Date" to "IEP Due Date" per request. 

## Install and Setup Instructions
1. Install Sped-Schema Plugin by following the plugin install proceedures laid out by PowerSchool
1. Enable the Sped-Schema Plugin
1. Install Sped-Resources Plugin by following the plugin install proceedures laid out by PowerSchool
1. Enable the Sped-Resources Plugin
    - These are packaged separately due to a flaw in the plugin install on PowerSchools side in which the PowerQueries may not reference Schema Extensions in the same Plugin
1. Go to District Setup>Code Sets
1. Click **Add Code Set**
1. Type **SPED** 
1. Select **SPED** in the drop down
1. Click **Submit**
1. Click **Add Code**
1. Type **Handicap** for the code and display value  
1. Click **Submit**
1. Click **Add Code Set**
1. Type **HandicapCodes**
1. For each Handicap needed, enter in a code and a display value and select the Parent Code set as SPED and the Parent Code as HandicapCodes
    **In Example:** AU for the code and Autistic for the display value, CD for the code and Cognitively Delayed for the display value
1. Click **Add Code Set**
1. Type **SpedPrekCodes**
1. Select **SpedPrekCodes** from drop down
1. Back in PowerSchool, Click **Add Code**
1. Click **Add Code**
1. For each Pre-K Type needed, enter in a code and a display value and select the Parent Code set as SPED and the Parent Code as SpedPrekCodes
    **In Example:** AU for the code and Autistic for the display value, CD for the code and Cognitively Delayed for the display value

1. To populate a list of Case managers:
    1. Go to the Saff Security Settings Page
    1. Click the new SPED Information Tab
    1. Check the box for Case manager or Related Service Case Manger or both
    1. The search dropdowns on the home screen and the case manager dropdowns in the student pages will now pull case managers.
    **NOTE:** Case managers will only appear in the list at the district level and for each school they are affiliated with (i.e. in the Teacher Security Settings)