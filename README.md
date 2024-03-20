# qb-gsee-problem-instances

Ground State Energy Estimation (GSEE) `problem_instance` JSON files for the Quantum Benchmarking (QB) Program.

### What is it?

A set of `problem_instance` JSON files that contain the metadata about a specific challenge problem in GSEE.  The file also includes requirements for the performer in terms of runtime and accuracy.  The schema for the JSON file is here:  https://github.com/jp7745/qb-file-schemas

### Where is the data?

The data files may be large, so typically the JSON file only contains the metadata and URLs to where the data files may be downloaded.

### How do I download the associated data files (e.g., Hamiltonians)?

Each `problem_instance` file may point to data sets on different servers, so you'll need to contact the POCs referenced in each `problem_instance`` file.

For the current set of GSEE `problem_instances`` provided by the BOBQAT team, the data lives on an SFTP server at `sftp.l3harris.com``. The read-only credentials for accessing the Hamiltonian files are available on the QB program basecamp here XXX_insert_link_XXX.

You may use any SFTP client you want.  There is an example Python script to programmatically download the files in the `examples` directory.

###  How do I submit a new `problem_instance` file?

Develop your own `problem_instance` JSON file, filling in most of the self-explanatory fields and generating *new* UUIDs for your instance and associated files.  

When developing a new `problem_instance` file, Microsoft VS code will usually automatically pull the schemas and to give you hints on what fields are required and the associated format.  Restart VS Code or use the `JSON: Clear Schema Cache` action to update schemas.  If this continues to fail, VS Code users can manually download schemas and manually associate a schema with a filename by regex.  There are a variety of other tools for validating your JSON file.  See the `examples` folder.

The `problem_instance` JSON metadata file should be placed in the appropriate repository. E.g., for GSEE, the file would go into this repository.

The associated data files that go along with your `problem_instance` file will be placed somewhere else.  If you don't have your own server, L3Harris can host your files on the SFTP server.  L3Harris has additional *read/write* credentials for the SFTP server that may be shared with other teams.

Note that the schema includes a field for `license`, so you may choose the appropriate license for your `problem_instance` and related data.

###  What if the JSON schema doesn't have the fields I want to use?

The schemas live in a different repository:  https://github.com/jp7745/qb-file-schemas

Contact the BOBQAT team and we'll discuss modifying the schema.

### Warning! Automated Actions:

There is a nightly (or manually triggered) Github action to validate all `problem_instance` JSON files and *move* errored files to the `problem_instances_WITH_SCHEMA_ERRORS` directory.

There is a nightly (or manually triggered) Github action to generate the `summary.csv` file.  This file should not be edited; edits will be overwritten.





### License:

Copyright 2024 L3Harris Technologies, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.