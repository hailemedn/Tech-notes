2026-08-19
Tags: #npc #cmg

# 04 Gy and Sy failure cause to watch out for

|            |                                  |                                  |            |
| ---------- | -------------------------------- | -------------------------------- | ---------- |
| cause code | Diameter  Reject Cause           | Rejection Category               | Interfaces |
| 4012       | CreditLimitReached               | Business Failures/User behavior  | GY         |
| 5031       | RatingFailed                     | Technical Failure                | GY         |
| 4011       | CCNotApplicable                  | Technical Failure                | GY         |
| 4010       | EndUserSvsDenied                 | Business Failures/User behaviour | GY         |
| 5030       | UserUnknown                      | Technical Failure                | GY,SY      |
| 5012       | UnableToComply                   | Technical Failure                | GX,GY,SY   |
| 5005       | MissingAvp                       | Technical Failure                | GX,GY      |
| 5004       | InvalidAvpValue                  | Technical Failure                | GX,GY,SY   |
| 5003       | AuthRejected                     | Business Failures/User behaviour | GX,GY      |
| 5002       | UnknownSessionId                 | Technical Failure                | GX,GY,SY   |
| 5001       | AvpUnsupported                   | Technical Failure                | GX,GY      |
| 3002       | UnableToDeliver                  | Technical Failure                | GX,GY,SY   |
| 3004       | Too Busy                         | Technical Failure                | GX,GY,SY   |
| 5141       | Trigger Event                    | Technical Failure                | GX         |
| 5198       | Roverload Control                | Technical Failure                | GX         |
| 5198       | Unknown ( vender_1045 code 5198) | Technical Failure                | SY         |