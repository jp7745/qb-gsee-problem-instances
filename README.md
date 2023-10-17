# qb-gsee-problem-instances
Ground State Energy Estimation Problem Instances for the Quantum Benchmarking Program

**WARNING!  WORK IN PROGRESS!**


### See the `examples` directory for examples on:

1. Reading/modifying/writing back instances
2. Validating that instance adhere to the schema.  Proposed schema is here:  https://github.com/jp7745/qb-file-schemas
3. TODO: using TBD database program to review instances


### Warning! Automated Actions:

There is a nightly (or manually triggered) Github action to validate all `problem_instance` JSON files and *move* errored files to the `problem_instances_WITH_SCHEMA_ERRORS` directory.


There is a nightly (or manually triggered) Github action to generate the `summary.csv` file.  This file should not be edited; edits will be overwritten.

### TODO:
1. convert catalysis instances to `problem_instance` files.
2. complete SFTP repository for all Hamiltonians, edit URL pointers in `problem_instance` files.


### License:

Copyright 2023 L3Harris Technologies, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.