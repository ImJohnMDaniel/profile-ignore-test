# Profile not forceignored example project

# Reproduction Steps
- create new scratch org
    - `sfdx force:org:create -a bluefish -d 1 -f config/project-scratch-def.json -s`
- push source code to scratch org
    - `sfdx force:source:push` 
- pull source code from scratch org
    - `sfdx force:source:pull`

***FAILURE POINT
- The `force:source:pull` command pulls the `Admin.profile-meta.xml` file even though the `.forceignore` file lists `**.profile-meta.xml`

