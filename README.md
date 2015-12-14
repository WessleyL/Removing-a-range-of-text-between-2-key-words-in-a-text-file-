# Removing-a-range-of-text-between-2-key-words-in-a-text-file-
I'm trying to remove a block of text between the words "Current Depth" and "BHA INFORMATION"

Currently I'm using the Find and Replace window with the "Find what:" set with the regex " Current Depth.*?BHA INFORMATION INFORMATION "
This has successfully found "Current Depth -everything in between- to the end of the string BHA INFORMATION"

I'm wanting to replace it all (EXCEPT the string "BHA INFORMATION") with nothing.

There are no common or special characters before the string "BHA INFORMATION".

Example text it is finding seen below:


Current Depth                                                                           8054
                                                                                           Present Operation                                                                  Drilling ahead
                                                                                               Company Rep:                                                                      Troup/Pottinger
   Report Date            API               AFE Number                   AFE Amount                      Spud Date                           Well Name                                                   Contractor
   08/03/2015     34-013-2-0902-00-00      769-W-1010-201                 2,795,401                     01/09/2015                        Bounty Hunter 2H                                             Patterson/296
                 State                                  County                                   Township                                    Elevation                                                Days From Spud
                 Ohio                                  Belmont                                  Goshen Twp                                     1198                                                         206
             24 Hr Footage                        ROP/24 Hr Footage                             Average ROP                              Current Formation                                               Weather
                 1079                                   44.958                                                                             Red Queenston                                            68 degrees and clear
                                                                                                              TIME BREAKDOWN
      Time               Hours                 Phase                 Job           NPT Code                Vendor                 Dim. Cap.           Start Depth            End Depth                              Summary
                                                                                                                                                                                              PJSM with Patterson rig crew and all personal  H2S  
      06:00               0.3          9-5/8" String          Safety Meeting                                                                                      6,991                 6,991 Awareness  & Fit for duty
                                                                                                                                                                                              Mist drilling intermediate section  F/ 6991'  T/ 7244'   Slide/ 
      06:15               3.8          9-5/8" String          Drill to Casing Point                                                                               6,991                 7,244 Rotate. Rot WOB 38K,  RPM 45  RTQ  8K   CFM  4499  , SPP  
                                                                                                                                                                                              420,   KCL  GPM 25,  Soap 5 gal per hr  Gas 58 units,
                                                                                                                                                                                              Mist drilling intermediate section  F/ 7244'  T/ 7500'   Slide/ 
      10:00               4.0          9-5/8" String          Drill to Casing Point                                                                               7,244                 7,500 Rotate. Rot WOB 40K,  RPM 45  RTQ  8-16K   CFM  4442  , 
                                                                                                                                                                                              SPP  420,   KCL  GPM 25,  Soap 5 gal per hr  Gas 40  units,
                                                                                                                                                                                              Mist drilling intermediate section  F/ 7500'  T/ 7714'   Slide/ 
      14:00               4.0          9-5/8" String          Drill to Casing Point                                                                               7,500                 7,714 Rotate. Rot WOB 40K,  RPM 45  RTQ 8- 16K   CFM  4499  , 
                                                                                                                                                                                              SPP  420,   KCL  GPM 25-30  Soap 5 gal per hr  Gas 30 units,
                                                                                                                                                                                              P.T.S.M./Handover notes. (Fit for duty, Preparations for 
      18:00               0.3          9-5/8" String          Drill to Casing Point                                                                               7,714                 7,714 cement job.)
                                                                                                                                                                                              Mist drilling intermediate section f/ 7714' to 7809.  Wob 40 
      18:15               1.3          9-5/8" String          Drill to Casing Point                                                                               7,714                 7,809 , Rot top 42 @ bit 84, Tq 8000 to 16000, Spp 466, Cfm 4600,
      19:30               0.5          9-5/8" String          Rig Service                                                                                         7,809                 7,809 Service rig
                                                                                                                                                                                              Perform Derrick inspection and Man rider inspection. 
      20:00               0.5          9-5/8" String          Safety Meeting                                                                                      7,809                 7,809 Inspection done by 3rd party. (Bishops Lifting services.)
                                                                                                                                                                                              Mist drilling f/7809 to 7999.  Wob 30 to 35, Tq 8000 to 
      20:30               3.5          9-5/8" String          Drill to Casing Point                                                                               7,809                 7,999 11000, Rot top 40 @ bit 83,  Spp 525, Cfm 4686,
                                                                                                                                                                                              Mist pump lost its GPM output. Pull back 50 ' and slowly 
      00:00               2.0          9-5/8" String          NPT              Pumps           Highlands Drilling LLC                                             7,999                 7,999 work pipe. Work on mist pump. Once  we got pump back on 
                                                                                                                                                                                              line we had to circulate and clean hole up.
                                                                                                                                                                                              Mist drill f/ 7999 to 8054',  Wob 30 to 35  Rot top 45 @bit 
      02:00               1.0          9-5/8" String          Drill to Casing Point                                                                               7,999                 8,054 87. Slide 30 ' Rotate 25' . Spp 525, Cfm 4711
                                                                                                                                                                                              Mist pump lost GPM output. Pull back 30' and replace all 
      03:00               1.0          9-5/8" String          NPT              Pumps           Highlands Drilling LLC                                             8,054                 8,054 valves. Clean up hole prior to return drilling.
                                                                                                                                                                                              Mist drilling f/ 8054' to 8184. Wob 35, Rot top 45 @ bit 88, 
      04:00               2.0          9-5/8" String          Drill to Casing Point                                                                               8,054                 8,184 Spp483, Cfm 4691. Kcl 25 gpm, Soap 6 gpm


      Total:              24.0
                                                                                                             HOURLY OPERATIONS
                                       Circ/Cond                               Pick Up /Lay Down BHA                         Stage Loads                                                                  Injuries?
UnPlanned                              Milling                                 Lay Down BHA                                  Transport                                                                      No
Drill Lateral                          Fishing                                 Cement                                        Unload Trucks                                                              Near Miss?
Survey                                 Coring                                  Clean Pits                                    Clean Out Run                                                                  No
Drill Curve                            Wireline/Logging                        Constant                                      Slip & Cut Drill Line                                                       Incidents?
Tripping                               Plug Back                               Drill to Casing Point       19.75             Spud Work                                                                      No
BHA                                    Rig Up                                  Drill to KOP                                  Standby                                                               Total Operating Hours
Rig Repair                             Rig Down                                Drill to Log Point                            Casing Pressure Test                                                          21.00
Rig Service                         0.5 Move In                                Infield Move                                                                                                      Total Non-Operating Hours
Run Casing                             Move Out                                Load Hole                                                                                                                    3.00
WOC                                    Other                                   Load Trucks                                                                  
NU/ND                                  Safety Meeting                      0.75 NPT                          3
Testing BOP                            Well Control                            Skid Rig
                                                                                                                   MUD DATA
            Type of System                              Weight                                   Viscoscity                               Plastic Viscoscity                                             Yield Point

            HTHP Fluid Loss                            % Solids                                      PH                                   Electrical Stability                                           OW Ratio

                 Cake                            Gel Str 10 sec/10 min                              POM                                      Solids Total                                                   LGS
                                                          /
                                                                                                              BHA INFORMATION
