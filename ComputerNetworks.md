## [OSI Model (Open Systems Interconnection Model](https://www.imperva.com/learn/application-security/osi-model/)
![image](https://user-images.githubusercontent.com/74251229/191927410-1ffdfc80-e1ed-43b8-94a2-90a5c724b0ef.png)

## [TCP/IP Model](https://www.researchgate.net/publication/327483011_A_Survey_of_Protocol-Level_Challenges_and_Solutions_for_Distributed_Energy_Resource_Cyber-Physical_Security/figures?lo=1)
![image](https://user-images.githubusercontent.com/74251229/191930253-01da9139-f833-46b8-a51b-6a50e11d1ac4.png)


## [Transport Layer Protocols](https://youtu.be/jJyXpMmXJI0)
S.NO. | TCP  |  UDP |
|-----|------|-------|
| 1 | Connection Oriented | Connection less |
| 2 | Reliable | Less Reliable |
| 3 | Error control is mandatory, So header needs to have checksum | Error control is optional, so checksum is optional and 0 can be sent in checksum instead of particular checksum |
| 4 | Slow transmission because it needs to build connection before sending the data | Fast transmission because it does not need to make connection |
| 5 | More overhead (20-60 bytes Header need to use as it contains everything for error control or flow control or congestion control like flag etc.) | Less overhead (8 bytes Header only because it has less fields) |
| 6 | Flow control (data if discarded due to any reason, it will send again), congestion control  | No Flow Control and Congestion Control |
| 7 | Ordering | Unordering |
| 8 | Examples: http, ftp | DNS |

![image](https://user-images.githubusercontent.com/74251229/191934278-3d141040-0681-4dfe-bedc-7b2879c52335.png)



