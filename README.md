# CSA-Mock-Exam-Modul-7.2-Migration-and-Integration

## System Update Sets
![](https://github.com/CodeWithLuwam/CSA-Mock-Exam-Modul-7.2-Migration-and-Integration/blob/main/Images/System%20Update%20Sets.png?raw=true)
![](https://github.com/CodeWithLuwam/CSA-Mock-Exam-Modul-7.2-Migration-and-Integration/blob/main/Images/System%20Update%20Sets%20part%202.png?raw=true)
1. What is an Update Set in ServiceNow?
    - [ ] A. A collection of tables and fields that store CMDB data
    - [x] B. A group of configuration and customization changes that can be moved from one instance to another
    - [ ] C. A method of importing external data into ServiceNow
    - [ ] D. A tool used only for debugging scripts

2. What type of file format does an Update Set use?
    - [ ] A. JSON
    - [ ] B. CSV
    - [x] C. XML
    - [ ] D. XLSX

3. What does an Update Set contain? (Choose three)
    - [x] A. A set of record details uniquely identifying the update set
    - [x] B. A list of configuration changes
    - [x] C. A state to determine if another instance can retrieve and apply changes
    - [ ] D. Application data like Incident records

4. Which table does ServiceNow use to track changes for Update Sets?
    - [ ] A. sys_update_set
    - [x] B. sys_update_xml (Customer Update)
    - [ ] C. sys_app
    - [ ] D. cmdb_ci

5. What is the purpose of the default Update Set?
    - [ ] A. To move configurations safely between instances
    - [x] B. To capture changes made in the instance without adding those changes to user-created update sets
    - [ ] C. To store only system platform updates
    - [ ] D. To automatically merge update sets

6. What is the recommended best practice for migrating changes between instances?
    - [ ] A. Always use the Default Update Set
    - [x] B. Use a named Update Set
    - [ ] C. Export individual records as XML manually
    - [ ] D. Only make changes directly in production

7. What are the available operations for Update Sets? (Choose four)
    - [x] A. Create
    - [ ] B. Delete permanently
    - [x] C. Complete
    - [x] D. Retrieve
    - [x] E. Preview
    - [x] F. Commit

8. Which of the following is a risk when using multiple update sets individually?
    - [ ] A. CMDB corruption
    - [x] B. Leaving out sets or committing them in the wrong order
    - [ ] C. Breaking the UI theme
    - [ ] D. Losing system logs

9. What feature allows grouping multiple update sets together so they can be previewed and committed in bulk?
    - [ ] A. Application Scope
    - [ ] B. Update Set Merging
    - [x] C. Batch Update Sets
    - [ ] D. Instance Sync

10. Where do you navigate in ServiceNow to create or set an Update Set?
    - [ ] A. All > System Definition > Tables
    - [x] B. All > System Update Sets > Local Update Sets
    - [ ] C. All > System Applications > Studio
    - [ ] D. All > System Import Sets
   
## What is captured in an Update Set?
![](https://github.com/CodeWithLuwam/CSA-Mock-Exam-Modul-7.2-Migration-and-Integration/blob/main/Images/What%20is%20Captured%20in%20an%20Update%20Set%3F.png?raw=true)
1. Which of the following is captured in an Update Set?
    - [ ] A. Tasks
    - [x] B. Business Rules
    - [ ] C. New Users and Groups
    - [ ] D. Modified Configuration Items (CIs)

➡ Business Rules are process records and are captured. Tasks, new users/groups, and modified CIs are data (not captured).

2. You create a new UI Policy to show or hide fields on a form. Will it be captured in an Update Set?
    - [x] A. Yes
    - [ ] B. No
          
➡ UI Policies are process records, so they are included.

3. Which of the following is NOT captured in an Update Set?
    - [ ] A. Report definitions (including visualization type and sharing settings)
    - [ ] B. List configuration
    - [x] C. New Data Records
    - [ ] D. Client Scripts
          
➡ Update Sets capture configuration changes, not actual data like new incidents or user records.

4. A developer wants to move user records between instances. Which method should they use?
    - [ ] A. Update Set
    - [x] B. Export XML
    - [ ] C. Unload Dashboard
    - [ ] D. System Clone
          
➡ Data records (like users, CIs) must be moved with Export XML, not Update Sets.

5. You’ve built a new dashboard with multiple portal pages. Will this automatically be transferred in an Update Set?
    - [ ] A. Yes
    - [x] B. No
          
➡ Portal pages from dashboards aren’t automatically included in Update Sets.

6. Which function should you use to move a dashboard and all its related portal pages?
    - [ ] A. Export XML
    - [ ] B. Import Set
    - [x] C. Unload Dashboard
    - [ ] D. Transform Map
   
➡ The “Unload Dashboard” function is required to move dashboards with portal pages.

7. Which of the following is an example of a process record captured in an Update Set?
    - [x] A. Roles
    - [ ] B. New Data Records
    - [ ] C. Scheduled Jobs
    - [ ] D. Tasks
          
➡ Roles are captured. Scheduled Jobs, Tasks, and new data records are data, not captured.

8. Why do Update Sets not capture actual data records (such as incidents or user records)?
    - [ ] A. To reduce performance load on the instance
    - [x] B. Because Update Sets are designed for configuration and customization changes
    - [ ] C. Because Update Sets automatically encrypt data records
    - [ ] D. To comply with ITIL data handling rules
          
➡ They’re meant to move system configuration, not operational/transactional data.

9. Which of the following will be excluded from an Update Set unless special functions are used?
    - [ ] A. Report Definitions
    - [ ] B. Fields
    - [x] C. Dashboard portal pages
    - [ ] D. UI Policies
          
➡ Dashboards require the “Unload Dashboard” function to be included.

10. Which of these statements best describes what an Update Set captures?
    - [ ] A. It captures all data, including incidents and tasks.
    - [ ] B. It captures only system logs for auditing.
    - [x] C. It captures customizations and configuration changes, but not actual data.
    - [ ] D. It captures both configuration changes and production data.
          
➡ That’s the ServiceNow definition of Update Sets.

## Create and select an Update Set
![](https://github.com/CodeWithLuwam/CSA-Mock-Exam-Modul-7.2-Migration-and-Integration/blob/main/Images/Create%20and%20Select%20an%20Update%20Set.png?raw=true)
1. Which of the following best describes the purpose of an Update Set?
    - [ ] A. To store actual data records like incidents and tasks
    - [x] B. To store configuration and customization changes
    - [ ] C. To back up all user records for recovery
    - [ ] D. To schedule automated jobs

2. Where do you navigate in the application navigator to create a new update set?
    - [ ] A. All > System Definitions > Update Sets
    - [x] B. All > System Update Sets > Local Update Sets
    - [ ] C. All > System Properties > Update Set Management
    - [ ] D. All > Configuration > Update Sets

3. Which button should you click to make the new Update Set the target for configuration changes?
    - [ ] A. Save
    - [ ] B. Submit
    - [x] C. Submit and Make Current
    - [ ] D. Activate

➡ “Submit” only creates it. “Submit and Make Current” sets it as the active Update Set.

4. What state must an Update Set be in before you can set it as the current set?
    - [ ] A. Complete
    - [ ] B. Draft
    - [x] C. In progress
    - [ ] D. Closed

➡ Only Update Sets in the “In progress” state can be made current.

5. Which of the following naming conventions is considered best practice for Update Sets?
    - [ ] A. Random words chosen by the developer
    - [ ] B. Only numbers, e.g., "001"
    - [x] C. Including initials, story numbers, or descriptive keywords
    - [ ] D. Using today’s date only

➡ This ensures clarity when managing multiple Update Sets.

6. Why is it recommended to use descriptive keywords in an Update Set name?
    - [ ] A. To ensure the system can automatically assign it to a user
    - [x] B. To make it easily identifiable and maintain clarity when managing multiple sets
    - [ ] C. To allow the Update Set to be exported in XML format
    - [ ] D. To improve system performance
➡ Helps organize and recognize Update Sets across teams.

7. Which of the following actions creates a new Update Set?
    - [ ] A. Right-clicking on the Update Set table and selecting Insert
    - [x] B. Navigating to Local Update Sets and clicking New
    - [ ] C. Cloning the production instance
    - [ ] D. Running an import set

8. Which field in the Update Set form allows you to describe its purpose in more detail?
    - [ ] A. Parent
    - [ ] B. Release date
    - [ ] C. Application
    - [x] D. Description
          
➡ The description field is intended to clarify its purpose.

9. After submitting a new Update Set, which button must you click to begin capturing configuration changes into it?
    - [x] A. Submit and Make Current
    - [ ] B. Update
    - [ ] C. Save as Default
    - [ ] D. Capture Changes

➡ Otherwise, changes would go into the previously active Update Set.

10. Which of the following examples is a properly named Update Set?
    - [ ] A. “Set1”
    - [x] B. “LUW-CRM-05”
    - [ ] C. “Today’s Changes”
    - [ ] D. “Test”

➡ Follows best practice: initials + descriptive keyword/number.

## Mark an Update Set complete
![](https://github.com/CodeWithLuwam/CSA-Mock-Exam-Modul-7.2-Migration-and-Integration/blob/main/Images/Mark%20an%20Update%20Set%20complete.png?raw=true)
1. When should you mark an update set as Complete?
    - [ ] A. As soon as you create it
    - [x] B. After configurations are finished and conflicts are resolved
    - [ ] C. Before testing is complete
    - [ ] D. Whenever you want to stop tracking changes
  
2. Once an update set is marked as Complete, additional customizations can still be tracked in it.
    - [ ] True
    - [x] False

3. What happens when you mark an update set as Complete?
    - [x] A. It becomes available for migration to other instances
    - [ ] B. It automatically merges with the parent update set
    - [ ] C. It is deleted from the instance
    - [ ] D. It reopens in “In Progress” status
  
4. If you need to make additional changes after marking an update set as Complete, what should you do?
    - [ ] A. Change the state back to “In Progress”
    - [ ] B. Delete the update set and start over
    - [x] C. Create a new update set for the additional changes
    - [ ] D. Edit the completed update set directly
  
5. You mark an update set as Complete and later realize you forgot a customization. What is the recommended action?
    - [ ] A. Reopen the completed update set
    - [ ] B. Add the change directly to the completed update set
    - [x] C. Create a new update set and commit the additional change there
    - [ ] D. Merge the change manually into the XML file
  
6. Naming conventions for update sets help manage them more effectively. For example, instead of “Performance Enhancements,” you could name them “Performance Enhancements” and “___________.”
    - [x] “Performance Enhancements 2”
  
# 7.3 Applying and Update Set
![](https://github.com/CodeWithLuwam/CSA-Mock-Exam-Modul-7.2-Migration-and-Integration/blob/main/Images/Applying%20an%20Update%20Set.png?raw=true)
1. What are the three typical steps in the Update Set migration process?
    - [ ] A. Extract, Validate, Commit
    - [x] B. Retrieve, Preview, Commit
    - [ ] C. Import, Validate, Release
    - [ ] D. Download, Install, Test

✅ Explanation: The standard ServiceNow update set migration process is: <br>
Retrieve (import the XML into the target instance),<br>
Preview (check for conflicts or errors),<br>
Commit (apply the changes to the target instance). 

2. What is the purpose of the Preview step when migrating update sets?
    - [ ] A. To back up the instance before committing
    - [x] B. To compare changes with the target instance and detect conflicts
    - [ ] C. To automatically commit updates without errors
    - [ ] D. To assign sys_id values to all records

✅ Explanation: Previewing allows administrators to identify conflicts or incompatibilities between the update set and existing records before committing, ensuring a smoother migration.

3. What happens if two update sets modify the same record?
    - [ ] A. Both changes merge automatically
    - [x] B. The newest change overwrites the older one
    - [ ] C. Both changes fail to commit
    - [ ] D. ServiceNow blocks the migration

✅ Explanation: ServiceNow follows a “last write wins” approach. The most recent update overwrites earlier changes during migration.

4. What does ServiceNow recommend as the maximum number of records in an update set to reduce conflicts and simplify review?
    - [ ] A. 50
    - [ ] B. 75
    - [x] C. 100
    - [ ] D. 200

✅ Explanation: Best practice is to limit update sets to around 100 records to keep them manageable and minimize conflict risk.

5. Which of the following is true about loading update sets between different ServiceNow family releases?
    - [ ] A. Update sets from a newer release always work on older releases
    - [ ] B. Update sets from an older release always work on newer releases
    - [x] C. Additional testing may be required to ensure compatibility between versions
    - [ ] D. Update sets are version-independent and never require testing

✅ Explanation: Loading update sets from older to newer releases is generally supported but still requires testing; loading from newer to older may require even more validation.

6. Why is it important to ensure all platform records have consistent sys_id fields across instances?
    - [ ] A. sys_id fields determine update set execution order
    - [x] B. sys_id mismatches can cause record duplication and migration issues
    - [ ] C. sys_id fields are used only for reporting and do not affect migration
    - [ ] D. sys_id fields reset automatically during update set commit

✅ Explanation: sys_id uniquely identifies a record. If they differ between environments, migration may create duplicate records or fail.

7. What is the best way to mitigate sys_id mismatches between production and sub-production instances?
    - [ ] A. Manually update sys_id values in each record
    - [x] B. Clone production into sub-production instances before using update sets
    - [ ] C. Disable sys_id validation during commit
    - [ ] D. Use a script to auto-generate sys_id values

✅ Explanation: Cloning ensures sys_id consistency across environments, which avoids problems with record references during migration.

8. Where do you navigate in ServiceNow to retrieve update sets from an XML file?
    - [ ] A. All > System Update Sets > Update Sources
    - [x] B. All > System Update Sets > Retrieved Update Sets
    - [ ] C. All > System Diagnostics > Update Set Logs
    - [ ] D. All > Applications > Update Management

✅ Explanation: To import an update set from XML, you navigate to Retrieved Update Sets and upload the file.

9. What is the main risk of committing an update set without previewing it first?
    - [ ] A. Longer commit times
    - [ ] B. Missing system logs
    - [x] C. Undetected conflicts or incompatibilities may break the instance
    - [ ] D. The update set will not import correctly

✅Explanation: Skipping preview risks committing changes that conflict with existing records, which can cause errors or unexpected behavior.

10. Which statement about update sets is NOT true?
    - [ ] A. Update sets capture configuration changes in an instance
    - [ ] B. Update sets can be exported as XML and imported into another instance
    - [x] C. Update sets automatically include data like incident records and user records
    - [ ] D. Update sets should be previewed before committing

✅ Explanation: Update sets capture configuration changes (forms, fields, scripts, etc.) but not transactional data like incidents or users.

## Retrieval from a remote instance
1. In which instance do you navigate to retrieve an update set from a remote instance?
    - [ ] A. Development instance
    - [ ] B. Sub-production instance
    - [x] C. Production instance
    - [ ] D. Test instance

✅ Explanation: The screenshot specifies: “In the Production instance: Navigate to All > System Update Sets > Update Sources.”

2. What menu path is used to retrieve update sets from a remote instance?
    - [ ] A. All > System Update Sets > Retrieved Update Sets
    - [x] B. All > System Update Sets > Update Sources
    - [ ] C. All > System Update Sets > Update Logs
    - [ ] D. All > Applications > Update Management

✅ Explanation: Remote retrieval requires navigating to Update Sources in the production instance.

3. What information must you provide when creating a new Update Source record for a remote instance?
    - [x] A. URL, Username, Password, Instance Type, Active flag, and Short Description
    - [ ] B. URL only
    - [ ] C. sys_id of the update set
    - [ ] D. Family release version

✅ Explanation: The form requires these fields to establish the connection to the remote instance.

4. What button should be used to verify connectivity to a remote instance before retrieving update sets?
    - [ ] A. Sync
    - [ ] B. Validate
    - [x] C. Test Connection
    - [ ] D. Check Update

✅ Explanation: The screenshot shows a Test Connection button to confirm the connection details are correct.

5. What are the three main steps when applying an update set (local or remote)?
    - [ ] A. Validate, Import, Release
    - [x] B. Retrieve, Preview, Commit
    - [ ] C. Extract, Transform, Load
    - [ ] D. Upload, Merge, Release

✅ Explanation: Both local and remote update sets follow the same process: Retrieve → Preview → Commit.

6. What happens automatically when retrieving update sets from a remote instance?
    - [ ] A. The update sets are committed immediately
    - [x] B. The platform automatically previews the update sets during retrieval
    - [ ] C. All update sets are merged into one
    - [ ] D. The sys_ids are reset to match production

✅ Explanation: With remote instances, ServiceNow streamlines the process by automatically running the preview step.

7. Which update sets are available for retrieval when connecting to a remote instance?
    - [ ] A. All update sets in the remote instance
    - [x] B. Only update sets marked as Complete
    - [ ] C. Only update sets created by the admin user
    - [ ] D. All update sets since the last connection

✅ Explanation: Only update sets in the Complete state are transferred from the remote (sub-production) instance.

8. After retrieving an update set from a remote instance, where do you access it in the production instance?
    - [ ] A. Update Sources module
    - [x] B. Retrieved Update Sets related list
    - [ ] C. Update Set Logs
    - [ ] D. System Diagnostics

✅ Explanation: Retrieved update sets are available through the Retrieved Update Sets related list for preview/commit.

9. What is the last step after retrieving and previewing an update set from a remote instance?
    - [ ] A. Validate it
    - [ ] B. Re-export it as XML
    - [x] C. Commit the update set
    - [ ] D. Refresh the connection

✅ Explanation: Once retrieved and previewed, you must commit the update set to apply changes.

10. Why is it necessary to set up connectivity to each sub-production instance when using remote update sets?
    - [ ] A. To clone sys_id values
    - [x] B. To transfer completed update sets from sub-production into production
    - [ ] C. To automatically update the CMDB
    - [ ] D. To share transactional data like incidents and tasks

✅ Explanation: Establishing connectivity ensures completed update sets can be moved from sub-production to production.
