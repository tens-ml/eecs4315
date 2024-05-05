#-------------------------------------------------------------------------------#
#  COURSE:  EECS 4315 - Mission Critical Systems                                #
#  SYSTEM: Moodle - Educational Learning Management                             #
#  STUDY : LNT & MCL Course Project - Final Submission                          #
#                                                                               #
#  AUTHOR :  Rafael Dolores, Alex Arnold                                        #
#  CREATION DATE :   2023-May-05                                                #
#  SUBMISSION DATE : 2023-May-05                                                # 
#  CONTAINS : moodleV{0-2}.lnt, demo.svl, prop{1-13}.mcl files                  # 
#  FOLDERS: FairnessProperties, LivenessProperties, SafetyProperties, LntModels #                                                           
#-------------------------------------------------------------------------------#

This project folder contains the work done to model and test the conceptual properties of 
the Moodle system:

    (1) Official Site - https://moodle.org/
    (2) Sandbox Site - https://sandbox.moodledemo.net/

Each folder stores the following:
    (1) FairnessProperties - all MCL properties related to Fairness
    (2) LivenessProperties - all MCL properties related to Liveness
    (3) SafetyProperties   - all MCL properties related to Safety
    (4) LntModels          - revisions of the moodle system + demo.svl
    
The LNT specification of the system can be found in the following files (inside LntModels folder):
    (1) moodleV0.lnt
    (2) moodleV1.lnt - Bug fixed where the System Admin is unable to enroll the student
    (3) moodleV2.lnt 
        (i)  Inclusion of different assignment grades 
        (ii) Utilization of different variables instead of just invoking "use" command and treating 
             them as generic placeholders.

The corresponding test purposes, written in MCL language, can be found in the following files:
    (1)  prop1.mcl
    (2)  prop2.mcl
    (3)  prop3.mcl
    (4)  prop4.mcl
    (5)  prop5.mcl
    (6)  prop6.mcl
    (7)  prop7.mcl
    (8)  prop8.mcl
    (9)  prop9.mcl
    (10) prop10.mcl
    (11) prop11.mcl
    (12) prop12.mcl
    (13) prop13.mcl
    
An SVL file (inside LntModels folder) was created to simulate and execute all of the properties that are associated with each test purposes:
    - demo.svl

To compile the LNT models, please execute the following commands:
    (1) Version 0:
    $ lnt.open moodleV0.lnt generator moodleV0.bcg
    
    (2) Version 1:
    $ lnt.open moodleV1.lnt generator moodleV1.bcg

    (3) Version 2:
    $ lnt.open moodleV2.lnt generator moodleV1.bcg

To simulate the models "on the fly" with OCIS:
    (1) Version 0:
    $ bcg_open moodleV0.bcg ocis

    (2) Version 1:
    $ bcg_open moodleV1.bcg ocis

    (3) Version 2:
    $ bcg_open moodleV2.bcg ocis

To compile the MCL properties individually, please execute the following command:
    $ lnt.open moodleV{version-number}.lnt evaluator4 {property_file_name}.mcl -diag

To compile all of the MCL properties in one execution, please execute the following command:
    $ svl demo.svl


