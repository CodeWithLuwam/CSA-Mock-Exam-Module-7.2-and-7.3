# CSA-Mock-Exam-Modul-7.2-Migration-and-Integration

## Syetm Update Sets
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
