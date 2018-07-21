# Note for 2018 EAST experiments



## 2018/05/26 (Saturday)

+ 76721 **1st PEFIT control shot** with new PCS system, lost control after **1.9s**.
+ 76722 PEFIT works fine, **6.33s** PF6 over current
+ 76723 PCS **hst7 down**, seems **PEFIT down**, 1.49s, PEFIT data failed to store
+ 76724~76726  IC did not work, IC did not recieve PCS command
+ 76735 PEFIT close q profile calculation module. 7.36s lost control
+ 76742 **PEFIT soft-landing shot**



## 2018/05/27 (Sunday)

+ 76833 PEFIT down, **out of memory**, swith to rtefit next shot
+ after 76858 restart PCS, because we found the PCS built-in PEFIT module makes the GPU card out of memory, which may cause control system down. New PEFIT version: libpefit129.a_180411_5
+ 76859-76860 10s soft landing with RTEFIT/ISOFLUX control.

## 2018/05/28 (Monday)

+ 76904 Before this shot, update PEFT to libpefit129.a_180411_7.





## 2018/05/31 (Thuesday)

**Purpose:**

​	D3D-EAST joint experiment: Plasma Control on Ram-down for Disruption Avoidance & Profile Control Development Tests.

**Leader:** David Humphreys & Bingjia Xiao

**Session Leader**:  Jayson Barr, William Wehner

Science Corrdinate: Zhengping Luo

Physics Operator : Erzong Li, Xianzu Gong

PCS: Ruirui Zhang, Qiping Yuan

#### Shotlists

**Reference shot:**74907

##### Build discharge platform.

+ 77121, restore 77113 (last ohmic shot last night), Ohmic shot.. Lost control when plasma reach flat top. Density is too high.
+ 77122 Repeat, tune density. bad too. Because the GPU was occupied. May be a accidental event.
+ 77123 Restore 77122, bad
+ 77124 Repeat, change the ip ramp-up rate, (1.5, 0.4)—>(1.7, 0.4)
+ **77125** repeat, remove density FB.  Good.
+ **77128** Good.  LHW 4.6G 800kW.
+ 77129 Repeat.  Bad, not breakdown.
+ **77130**/77131 Repeat without changes. Good shot. (What??).
+ 77132 LHW—> 1.5MW 4.6G, 0.5MW 2.45G, ecrh1, ecrh2 700kW;
+ 77133 Repeat, increase density to 2.5; extend ecrh 3s.

##### ramp-down experiment

+ 77134 Repeat, make a IP bump at flat top phase (3.5s to 6.9s), extend PLHI2 length 0.5s to 8s (start of ramp-down phase); ramp rate =0.25MA/s
+ 77135 Repeat, increase 4.6G LH power to 2MW. Ramp rate=0.5MA/s. H-mode.
+ 77136 Repeat.
+ 77137 Increase 1cm gapin & 1cm Rp, meantime change the Gain of G&D for Zx1 at limitedcontrol. PLHI2 (4.6G) 5.1s shotdown.
+ 77138 only increase 5mm gapin.  **Bad**.
+ 77139 Repeat 77137.
+ **77140** Repeat, Switch to PCS control LHW (FF only). Some of LHW channels protected, the power did not reach the request value. (next shot, PCS will reduce the power request a little bit), Ramp rate = 0.75MA/s
+ 77141 Repeat, Reduce the LHW power request, extend 4.6G LHW to 8.5s.
+ 77142 Repeat.
+ 77143 Cut off all power at 7s.  **Bad**, lost control after 3.78s. Because William increased the IP pertubation, but the LHW power did not catch up (setting problem). Next shot, remove the IP bump.
+ 77144 No IP bump. Cut off all auxiliary heating power at 7s. UFO at 7.4s ?? kills the plasma?.
+ 77145 Repeat without changing. **PCS watchdog problem**.
+ 77146 Repeat. lost control after 0.83s, **accidental event**? 
+ 77147 Repeat. 
+ 77148 start ramp down at 5s, cut off all auxiliary power at 4s. Keep the ramp rate 0.75MA/s. ECRH did not cut off at 4s (instead at 5.2s, next shot 4s.)
+ 77149 Repeat, ask ECRH reduce 1s pulse length (try to cut off at 4s).
+ 77150 Repeat, ask ECRH1 reduce 0.3s, ECRH3 reduce 0.7s. 
+ 77151 Repeat, ask 2.45G LHW reduce pulse 0.3s (bring forward 300ms LHW1  high-voltage trigger); **PCS watchdog problem**.
+ 77152 Repeat, ok
+ 77153 extend ECRH pulse length 1s to 5s; extend LHW pulse length to 5.5s.  ok
+ 77154 try to make the plasma limited.
+ 77155 make limited plasma earlier. But after reaching limited plasma at 5.0s, the plasma changed back to diverted plasma at ~5.1s last to 5.26s.
+ 77156 change Rp shape value from 0 to -2cm at 4.7s. Still has a time window with diverted plasma.
+ 77157 reduce the R value from 163cm to 160cm for both up and bottom X point at 4.7s.w

**Total 24 shots, effective shots: 19**.



## 2018/06/04 (Monday)

**Purpose:**

Triggered VDE's for Model Re-validation and Maximum Controllability Assessment. Trigger VDE's to collect data for proximity control; Release/Catch for $\Delta Z_{max}$

**Shotlists:**

**Reference shot:**

+ 77332 ohmic reference shot (ne=1.5)
+ 77333 Ohmic reference shot (ne=2)  **PCS watchdog problem, Bad**
+ 77334-77335, **Bad**.
+ 77336 Open RMP power before this shot, then we meet PF power protection problem, and no magnetization. **Bad**
+ 77337 lost control after 0.6s. **Bad**
+ 77338 PCS watchdog problem. **Bad**
+ 77339 After restarting DAQ system, Ohmic reference shot built.

**TVDE & Profile Control Exps:**

+ 77340 Setting q ctrl starts 0.8s then stops at 5.5s, then from 5.5s try to extend the plasma elongation (setting Zxtop from 79cm to 91cm & drsep from 2cm to 1cm). Ask LHW 4.6G system gives 4.5s power (cut off at 5.5s for ohmic discharge for TVDE). 
  + **Results:** *Bad*. 
  + Lost control  after 0.8s. q ctrl will ask LHW power from 1.5s
  + Seems the LHW trigger time (1s)  is not match with q ctrl setting (Need them response from 0.7s. Should change the trigger time to 0.7s).
+ 77341 Repeat. 
  + Results: Not good for q ctrl; Bad for TVDE
+ 77342 Retrieve a IP=400kA shot 77339, Repeat q ctrl and TVDE setting.
  + Results: CPU 5 cycle time is small (1ms), give a wrong q calculation, the plasma was killed at 0.88s.
+ 77343 Repeat, change cycle time for CPU 5 10ms (unit is $\mu s$)
  + Results: Bad. 1.5s.
+ 77344 Repeat, change the LHW requires time.
  + **Watchdog problem**
+ 77345 -- 77346 Same problem, lost control after 1.5s.
+ 77347 Restore 77339. Everything is **fine**.

--------------------------------------------------------------------------------

 Try TVDE exp

+ **77348** Repeat, Setting shape variation from 5.5s.  **OK**
+ **77349** Repeat, Setting shape variation from 5.5s, change Zxtop to 100cm, change Rp from 2.5cm offset to -5.5cm.  The $\kappa_{max}=1.74$, did not reach what we expected.
+ **77350** Repeat, remove the drsep setting from 5.6s (reduce 1cm). 
+ **77351** Repeat, add 6.2s with 100cm Zxtop & Zxbottom. Plasma changed to limited after 6.0s.

-----------------------------------------------------------------------

+ **one and half hours pause for visiting** ??? WF
+ **77352** Repeat, but using IP control category to control IP. Keep shape control did not change. Peferect repeat.

+ **77353** 5.8s remove all PF & IC ctrl. (Switch to zero M-matrix at DN1 phase and limitedcontrol phase for Zx at 5.8s) $\gamma_{fitted}=120$
+ **77354** move the shap variation from 5.5 to 6.6, turn off control at 6.8. $\gamma_{fitted}=140$
+ **77355** repeat 77354, but call M matrix back (turn on PF & IC control).
+ 77356 Repeat 77355, but change Zx1_GP from -20e3 to -15e3 at 6.0 My **bad** for wrong GP setting.
+ 77357 Repeat, change Zx1_GP from -20e3 at 6.0s to -15e3 at 6.1s. My **bad** for wrong GP setting. 
+ **77358** Repeat, change Zx1_GP from -200e3 at 6.0s to -150e3 at 6.1s.
+ **77359** Repeat, change Zx1_GP from -200e3 at 6.0s to -250e3 at 6.1s.  Smiliar $\gamma$ with 358
+ **77360** Repeat, change Zx1_GP from -200e3 at 6.0s to -300e3 at 6.1s. $\gamma=600$, **close-loop**
+ 77361 Based on 77360, kick off the VDE from 7.0s. (**PEFIT died**).
+ 77362 Repeat 77361. (**Watchdog** problem) Restart  PCS.
+ **77363** Repeat 77360, open-loop TVDE start at 7.0s.
+ 77364 Repeat, change Zx1_GP from -200e3 at 6.0s to -400e3 at 6.1s, close-loop. Plasma shrinks a lot at 6.5s, seems an accidental event.
+ **77365** restore 77363, **open-loop** TVDE at **7.2**s.  Increase the sample rate to 10k from 6.5s to 7.5s. $\gamma_{fitted}=551$
+ **77366** Restore 77364, **close-loop**.  $\gamma_{fitted}=602$
+ 77367 Repeat, open-loop at 7.2s, Profile control required a zero IP, which killed plasma.
+ 77368 Repeat, open-loop at 7.2s, Same problem with 77367.
+ 77369 Repeat, open-loop at 7.2s. VDE after 7.0s.$\gamma_{fitted}=518$ from 7.0275s to 7.054s.
+ 77370 repeat,  no changes, Seems the plasma can not reach our open-loop setting point. Similar growth rate.
+ **77372** Restore 77360, change Zx1_GP from -200e3 at 6.0s to -300e3 at 6.1s. **close-loop** ,
+ **77373** Repeat, close-loop, move the shape variation 1s earlier (from 5.7 for Rp, 5.6 for Zxtop & Zxbottom) 
+ 77374 Repeat, tune PF1 & PF2 for DN1 phase, keep others same. lost control after 1.1s. (UFO?)
+ 77375 repeat 77374. 
+ **77376 Restore 77372, **close-loop** control, but change IP from 0.4MA at 5.5s to 0.36MA at 6.5s and 8s. $\gamma_{fitted}=698$
+ **77377** Repeat but with **open-loop** control, turn off PF & IC control at 7.15s. $\gamma_{fitted}=375$
+ **77378** restore 77376, close-loop but increase IP from 0.4MA at 5.5s to 0.45MA at 6.5s & 8s. 
+ **77379** Repeat, but increase IP from 0.4MA at 5.5s to 0.42MA at 6.5s & 8s; and release the trip level for IP to 80kA.$\gamma_{fitted}=658$
+ **77380** Repeat, **open-loop** control, turn off PF & IC control at 7.13s. $\gamma_{fitted}=455$.
+ 77381 Restore 77377, **open-loop** control, move the trigger time to 7.21s (from 7.15s). 
  + Bad.  Because I did not restore whole shot, only discharge shape & isoflux category, which makes the IP control in-consistent with each two categories.
+ **77382** Restore 77377, **open-loop control**, trigger time at 7.21s, IP triplevel to 80kA. $\gamma_{fitted}=400$
+ **77383** Restore 77376, **close-loop** control, keep IP triplevel to 80kA, $\gamma_{fitted}=588$.
+ 77384 Repeat,  profile control makes some changes, we are not.

-----------------------------------

*Try $dZ_{max}$* cntrl

+ 77385 repeat, but change the shape variation time from 6.6s to 5.5s, and tune the PS7 & PS8, increase gapin from 3.5cm to 5.5cm.
+ 77386 repeat, remove the IP current reduction points, change Zxtop & Zxbottom variation time from 5.5s to 3.0s
+ 77387 Repeat, change Zxtop & Zxbottom variation time back to 5.5s.
+ 77388 Repeat, tune PS5 & PS6.
+ 77389 Repeat, tune PS1-PS8 based on 77388,  remove Rp set point at 7.5 (keep Rp same), 
+ 77390 tune PS1-PS8 based on 77388,  remove Rp set point at 7.5 (keep Rp same), 
+ **77391** Repeat, tune PS1-PS4 & PS11 & PS12, increase the gapin from 5.5cm at 7.5s t0 7.5cm. Shape control is good.
+ 77392 Repeat, tune PS1-PS4, change Drsep to 1.5cm at 6.0s; Gapin to 10.5cm at 7.5s.
+ 77393 Repeat, tune PS11-PS12 (remove the 8.0s point), change Mmatrix for Seg06 from -100e3 to -150e3. **IP trip, bad**.
+ 77394 Repeat, change Mmatrix for Seg06 back. Bad. The problem is come from the in-consistent of the Drsep setting in DN1 phase & ParaEquilibrium (PEFIT)



## 2018/06/06-06/07 (Wednesday & Thursday)

**Purpose:**

Recovery UQSF (300kA), try MIMO with IC in voltage mode, reference shot: **75704**.

**Shotlists:** (**IC in voltage mode**)

+ 77471, Restore 75704 (future shot 75740_uqsf_300kA), without modification, using 77470 Density & Gas injection category. Only breakdown.
+ **77472**, Repeat, without change (same as 75704). **PEFIT did not recieve control points, no ctrl error response back to PCS**. Reason: in-consistent setting for Algorithm selection in ISOFLUX & ParaEquilibrium Category. Lost control after 7.39s. 
+ 77473, Repeat, lost control after switching to IOSUSN phase, 2.8s.  Seems the plasma condition changed a lot compared to 75704. After selecting isousn sequence in ParaEquilbrium category, we got ctrl errors. The M matrix is Y.H. Wang's, not from italy colleagues. Can not use snowflake algorithm in ParaEquilibrium, which need provide Br & Bz ctrl error for X point in Y.H. Wang's MIMO matrix.
+ 77474 Repeat, change the M matrix to USNMIMO_180606_1. **Watchdog problem**.
+ **77475**, Repeat, using M matrix with  USNMIMO_180606_1. **Lost control after switching to ISOUSN MIMO control**
+ 77476, Repeat, reduce density to 1.6 from 2.0. Watchdog problem.

(06/07 Thursday)

+ **77544**, restore 77475, try MIMO control with USNMIMO_180606_1 ("Controller_data_exp_1.xls"), move start time of isoflux from 0.5s to 2.6s. **Lost control after 2.76s**.
  + The 0.5s start time for isoflux is a old problem of rtefit, keeping time start same as start time in rtefit to avoid the rtefit fail. This campaign, we use petit code, we don't have this problem.
  + If we used integrate gain in isoflux, the error will be integrated from the start time of isoflux, we need avoid this, otherwise there will be a big accumulated error by Integrateint control.
+ 77545 Repeat, UQSF 300kA MIMO control with USNMIMO_180606_2 ("Controller_data_exp_2.xls"), move start time of isoflux from 2.6s to 2.7s, tune PID parameters based on the xls file. **Watchdog** problem.
+ 77546 Repeat,  **No breakdown**.
+ 77547 Repeat, **No breakdown**.
+ **77548** Repeat UQSF 300kA MIMO control with USNMIMO_180606_2 ("Controller_data_exp_2.xls"), move start time of isoflux from 2.6s to 2.7s, tune PID parameters based on the xls file. **Lost control after 2.8s**.
+ 77549-77551(?) Restore 77472 ISOFLUX, only FB seg1. Bad. PS5 over current. (Y.H. Wang's shot)



**Note:**

+ 3:10PM Nanna Bao gives the coefficients for POINT acquisition in PCS, provide to PCS system.
+ POINT **77456** , 77457 calibriation good.
  + Need get rid of the bad channels;
  + Need Point group provides the dignostic weight;
  + Filter time is about **20ms** for POINT diagnostics;
  + Profile control cycle is 10ms;

----------------

**Profile control test:**

1. profile response shots (FF with LHW)
   + 77568/77569 Repeat 77567, but LHW 4.6G was controlled by PCS.
   + 77570 Repeat, but start LHW 4.6G from 3.9s (pcs FF command start from 3.9s). LHW did not response (no 4.6G LHW), we lost plasma at 6.21s.
   + 77571 Repeat. LHW provides two steps (1.5s-4s 0.9MW; 4.0-4.9s 1.7MW), then lost plasma. In this shot, NBI1L power increased a lot (40kV--2--50kV)
   + 77572 Repeat, reduce gas injection a little bit (by operator) to avoid lost plasma too earlier. Good.
   + 77573 Repeat, but stop LHW command at 6.5s. H-mode
   + 77574-77578 Repeat, decrease the NBI1L power (to 45kV);
   + **77579** Repeat, try control profile FB with magnetic $q_0$ by LHW, without IP control, soft landing; $I_p=0.5MA$, $n_e=3.5\times 10^{19} m^{-3}$
   + 77580-581 Repeat, add IP control by control profile category too. 1.1s.



## 2018/06/08 (Friday)

**Purpose:**

Profile control, reference shot: **77575**.

**Shotlists:** (**IC in voltage mode**)

- 77642, Restore 77575, with LHW 2.45G & 4.6G (ctrled by PCS), but 4.6G LHW failed in. Soft landing. IP reduced to 450kA.
- **77643**, Repeat, Both LHW works fine. FF only.
- **77644**, Repeat, profile control with FB ($q_0$ & $q_{90}$ both). Soft landing. Good. Pointname for q0 in PCS "pfsq00" (Target point name: "pftytm_1"), $q_{90}$ in PCS "pfsq09", no point data.
- **77645**, Repeat, profile control with FB q & IP (When the control $q_{90}$, then give a IP target called : "IPSJIP" for IP control). Go through.
- **77646**, Repeat, Go through. Point comes.
- **77647**, Repeat,  Go through. Point comes.



## 2018/06/13 (Wednesday)

**Purpose:**

Off-Normal & Fault Response algorithm test

**Shotlist**:

1. 77916, future shot: 997310 - PF1 Error test
2. 77917, future shot: 997311 -  (just load Alarms category) - PF1 Limit test;  PCS watchdog
3. 77918, PF1 Limit test
4. 77919, future shot: 997314 - (just load Alarms category) - RMP1 error test
5. 77920, future shot: 997315 - (just load Alarms category) - RMP1 limit test



## 2018/06/29 (Friday)

Reference shot: 70860 (UQSF ohmic discharge)

Try to restore UQSF 250kA ohmic discharge

1. 78137 Restore 70860 (except **shot start**, density & gas injection), data sampling to 0 from 1.0s, Using PEFIT. (1s之后全采样)。**Bad**. Maybe wrong setting for PEFIT.
2. 78138 Repeat, setting "ISOFLUX Sequence" start point to 2.7s (should consistent with ISOFLUX cateogry), reduce density ff a little bit.  **Bad**. Seems PEFIT did not work.
3. 78139 Repeat, PCS watch dog problem. **Bad**.
4. **78140** Repeat, without change. Repeat 78060. **OK**

**IC_Voltage Mode**:

Reference shot: 77475 (75704) MIMO

5. 78141, restore **77475**, (using 78140 density, gas injection, Discharge->shot start, data acquisition, but 78135 calibration data (cause PCPF6 coeeficient changed)). M matrix for Xpoint using Br & Bz control. PCS watchdog. Bad

6. 78142 Repeat, IC tripped. 

7. 78143 Repeat, did not check the IC current between -5s to -4.5s.

8. **78144** Repeat, remove the shotstart GP_IC = 1.0. MIMO **GOOD**. (ITALY MIMO)  X-point Br & Bz control (M_Br, Bz), 6.12s.

   **M matrix**: 

   usnitaly -- Controller_data_exp_2.xls

   usnitaly_1_180606--> Controller_data_exp_1.xls

   usnitalyrz --> M_75704_12-Jun-2018.xls (X-point Rx,Zx ctrl)

9. 78145 Repeat, VS control tau1 -0.2; tau2 (0.01)*10. **Failed**. Lost control after switching to VS control (2.1s)

10. 78146 Repeat, VS control restore tau1(1.5), tau2 * 10 (ms). **Failed** too.

11. **78147** Restore 76144, change M matrix to usnitaly_1_180606. **Good**. 7.0s

12. 78148 Repeat extend to 10s discharge setting. **PCS watchdog**. 

13. 78149 Repeat without changing.  **PCS watchdog**.

14. 78150 Repeat without changing. PCFL35 broken. **Bad**.

15. **78151** Repeat, **remove PCFL35** from RTEFIT & PEFIT. 8.0s. **Good**. 

16. 78152, repeat, tune gas GP for good density control. PEFIT died. **Bad**.

17. **78153**, repeat, (after PCS restart), 7.39s. **OK**. 6.5s IC has a big step.

18. **78154**, switch to M matrix (usnitalyrz) -- Rx, Zx cntrl. 8.54s. **Good**.

19. 78155-78158, switch to M matrix usnwyh.  PF system error.

20. 78159, repeat, HCN signal bad, lost control after 1.35s. **Bad**.

21. **78160**, repeat M matrix usnwyh, 8.4s. **OK**. Density control bad. HCN signal becomes weak.

## 2018/06/30 (Saturday)

Reference shot:

future shot: 78140_54265: based on shot 78140, calling 78160 IP control category, then set "limitedcontrol" algorithm M matrix for  IP control to 0; then all phase algorithm M matrix for IP control to 0; Using **54265** M matrix for ITER-like control setting to USN2 in isousn phase. (But this M matrix is to LSN, make sure it match to USN !!!, Zx1 M matrix value should be reversed) & correspond PID parameters.

1. 78182 normal shape discharge, ramp-down. Remove PEFIT algorithm, using RTEFIT. Get rid of PCS watchdog problem.



2. 78183 restore 78140, using RTEFIT, PEFIT follow. Watchdog problem.

3. 78185/78186, restore future shot "78140_54265". Lost control after switfhing to  isoflux (2.73s), but PCS can not stop normally.

4. 78187-78196  PCS system maintain & PCS test, 

5. 78197 Restore 78182, normal  shape discharge, lost control after 6.0s. **OK**. 该用PCS testbed运行

   **IC-voltage Mode**

| shot number | setting                                                      | results   | comments                                                     |
| ----------- | ------------------------------------------------------------ | --------- | ------------------------------------------------------------ |
| 78198       | restore 78169                                                | 5.3s      | PEFIT, PCS testbed                                           |
| 78199       | Repeat, k2*1.5 in VS ctrl, pcdvlp0319, pcdvlp0521            | 8.3s      | eliminate oscillation                                        |
| 78200       | repeat, set Ematrix Rx2 value & Gp_rx2 in limited cntrl,     | 8.3s      |                                                              |
| 78201       | Repeat, reset Ematrix rx2 -> 907 & increase seg_gp from 1.0--> 1.5 in isousn | 8.3s      | Not works for rx2 because of wrong setting to limitedcontrol, should set in newrz |
| 78202       | Repeat, correct setting for rx2 ematrix 907                  | 8.3s      |                                                              |
| 78203       | Repeat, rx2 ematrix 2.83e7                                   | 8.3s      |                                                              |
| 78204       | Repeat, using zx2 ematrix 2.83e6, using pcdvlp0319 (=Vloop3-Vloop19) to substitute the derivative value of zx2 | 2.85s bad | 尝试用两个单匝环电压信号差来计算Zp的Derivative值             |
| 78205       | repeat, $\tau_1$ from 1.5 to 1.8                             | 2.85s bad |                                                              |
| 78206       | repeat, $\tau_1$ back to 1.5, $k_2$ back to 0.054            | 2.85s bad |                                                              |
| 78207       | restore 78203, rx2 ematrix 2.83e6                            | 3.0s      |                                                              |
| 78208       | restore 78151, $k_2$ changed from 0.054 to 0.081             | 7.1s      |                                                              |
| 78209       | Using usnitaly & new PID                                     | 2.72s     |                                                              |

## 2018/07/02 (Monday)

Future shot: 78186_usn_qsfCom

Based on 78186, using calculated FF for USN shape discharge for UQSF comparison (pcs_ff_180701.00010), RZIp control only, changed to 250kA.

| shot number | setting                                                      | results                   | comments                                                     |
| :---------- | ------------------------------------------------------------ | ------------------------- | ------------------------------------------------------------ |
| 78217       | IC test                                                      |                           | OK                                                           |
| 78222       | Reference ohmic shot                                         | OK                        |                                                              |
|             | **IC-voltage driven mode**                                   |                           |                                                              |
| 78223       | restore 78203, setting Ematrix for vic1(-6.51e5) & dvloop0319 (2.83e6) | 3.3s                      | Calibration data for pcdvloop0319  (800)                     |
| 78224       | repeat, reduce density to 1.2, reload calibration data from shot 78203, vic1 coefficient wrong | 7.7s                      | PF1 over current, next shot reduce to 8s.                    |
| 78225       | Repat, reduce discharge length to 8s, $\tau_2$ changed to 0.02ms from 0.01ms in VS controller, vic1 coefficient (-813) | 6.6s                      |                                                              |
| 78226       | Repeat, tune VS controller $k_1 \times 1.5$                  | 0s                        | -4s PF power problem ?                                       |
| 78227       | repeat 78226                                                 | 2.6s Z oscillation bigger | PCS saving shot is 78226                                     |
| 78228       | Using new E matrix in newrz phase to test differential vloop signals to calcualte the $dz/dt$ , VS controller $k1$ reduced to its half in 78225 | 1.0s bad                  | Need modify the PID for ZX2 (which is used as a derivative value for fast z cntrl) |
| 78229       | Repeat, tune PID for ZX2 in newrz                            | 1.3s bad                  |                                                              |
| 78230       | Tune density, repeat                                         | 2.3s bad                  |                                                              |
|             | **DZ_max control ($\kappa=1.8$)**                            |                           |                                                              |
| 78231       | Build DN $\kappa=1.8$ shape with RZIp only                   | Bad                       |                                                              |
| 78232       | Repeat, using PID parameters from  52444 for limitedctrl     | bad                       |                                                              |
| 78233       | Extend shaping to 1.5s, keep IP flat top at 1.1s             | has flat top, still bad   |                                                              |
| 78234       | Tune GI to -400 (from -200)                                  | Bad too                   |                                                              |
| 78235       | Tune PF11 ff current (+200A)                                 | Wrong direction in FF     |                                                              |
| 78236       | Tune PF7 ff current (+200A),                                 | 1.2s SMBI too strong      |                                                              |
| 78237       | Modify Rp target value, tune IP target at 0.2s to 0.128MA    | VDE                       | $\gamma \approx 700 /s$                                      |
| 78238       | Set shaping time at 1.2s, tune Rp target to 1.885m at (1.1s) | VDE                       |                                                              |
| 78239       | Tune PF11 ff current (+100A),                                | Z oscillation             |                                                              |
| 78240       | Repeat, using vloop differential signal to check the $dz/dt$ calculation | Z oscillation             | not too much change                                          |
| 78241       | increase ZX1_GD to check the new dz/dt                       | oscillation becomes big   |                                                              |
| 78242       | increase both ZX1_GP & GD 2 times                            | shorter plasma            | It seems the PID can not adjusted                            |
| 78243       | Restore 78240, modify ZX1_Taup, ZX2_TauD                     |                           | 减小了延迟，增大噪声，观察控制能力是否好转                   |
| 78244       |                                                              |                           |                                                              |

| shot number | setting                                                      | results                                | comments                                                |
| ----------- | ------------------------------------------------------------ | -------------------------------------- | ------------------------------------------------------- |
| 78254       | restore 78144, remove FL35                                   | repeat, 6.21s                          |                                                         |
| 78255       | reduce density target                                        | 3.12s, oscillation                     |                                                         |
| **78256**   | repeat, reduce cpu3 sample intervals to save all density signal | 6.75s **good**                         | ramp-down phase                                         |
| 78257       | Repeat, introduce GI for all segs in ISOUSN                  | **watchdog** red light                 |                                                         |
| **78258**   | repeat 78257, GI=5 for all segs with Italy's MIMO matrix (2) | **Good**                               |                                                         |
| 78259       | Repeat, switch to wyh's MIMO matrix                          | 3.5s Bad                               | 汪悦航的MIMO矩阵                                        |
| **78260**   | Repeat 78258, but GI=10                                      | 7.18s **Good**                         |                                                         |
| **78261**   | Repeat, launch PEFIT transition algorithm                    | 7.25s                                  | 黄耀的PEFIT过渡算法启用                                 |
| 78262       | Repeat 78259, new MIMO matrix without GI on segs             | 6.6s not bad                           | 汪悦航的MIMO矩阵                                        |
| 78264       | Restore 78260, reduce IP target from 300kA (4.5s) to 250kA (5.5s) | 5.58s                                  | 试着                                                    |
| **78265**   | Restore 78260， increase IP target from 300kA (4.5s) to 320kA (5.5s) | 6.2s **not bad**                       | 前馈不合适了，MIMO矩阵也可能需要更新                    |
| 78266       | Repeat, set Taud=1ms, GD=10 for all segments in isousn phase | 1.3s gas injection                     | 强充气导致等离子体熄灭                                  |
| 78267       | Repeat 78266                                                 | 2.95s Gd量大了                         |                                                         |
| 78268       | Repeat, set Taud=1ms, GD=5 for all segments in isousn phase, set k2=0.1 (from 0.081) in VS controller | DAQ problem?? No breakdown             |                                                         |
| 78269       | Repeat 78268,                                                | 2.8s                                   | Fast Z控制变好                                          |
| 78270       | Repeat, set GD=1 for all segments in isousn phase, set k2=0.09 (from 0.1) in VS controller | 2.89s                                  |                                                         |
| **78271**   | Restore 78265                                                | 7.1s **Good**                          |                                                         |
|             |                                                              |                                        |                                                         |
| 78272       | restore 78262, add GI for segments                           |                                        |                                                         |
|             | **USN shape discharge**                                      |                                        | 试图建立USN参考位形                                     |
| **78273**   | Based on 78271, using ff from future shot 78186_usn_qsfCom   | 2.9s. Not bad.                         | Lost control after switching to Isoflux USN             |
| 78274       | Using new MIMO matrix "usnwyh", launch PEFIT transition algorithm (2.7--> 3.0s) | 3.2s Not bad, but PF5 over current     | USN                                                     |
| **78275**   | Switch to MIMO matrix back to 28273 (usnitaly)               | 3.1s                                   | $\gamma \approx 520$ USN                                |
|             |                                                              |                                        |                                                         |
| 78276       | restore 78262, Gp for br & bz reversed (wyh MIMO ctrl)       | ramp-down                              | 为验证wyh的反馈控制方向？ QSF                           |
| 78277       | Restore 78275, $k1 \times 1.5$ (3.225e-4) & $k2 \times 1.5$ (0.1215) | 2.74s, fast z ctrl becomes better      | 似乎是杂质？ QSF                                        |
| **78278**   | Repeat 78277                                                 | 2.75s VDE  problem                     | bigger $\gamma$**USN**                                  |
| 79279       | Rstore 78261 with new calculated MIMO matrix (wyh)           | 6.7s. ramp-down                        | 计算矩阵时，Br和Bz方向调整为原来的负方向 QSF （汪悦航） |
| 79280       | Repeat, tune gas injection                                   | ramp-down                              | QSF （汪悦航）                                          |
| 79281       | Repeat, tune gas injection                                   | ramp-down                              | 太强充气 QSF（汪悦航）                                  |
| 79282       | Repeat, add GI (5) for all segments                          | 4.0s control errors become bigger, bad | QSF 密度高，无SMBI3 （汪悦航）                          |
| 78283       | Restore **78278**                                            | 2.75s VDE problem?                     | **USN** discharge                                       |
| **78284**   | Repeat, $k_1 \times 2/3$ (1.433e-4)& $k_2 \times 2/3 $ (0.054) | 6.55s **Good**                         | USN                                                     |
| **78285**   | Based on 78284, calling 71464 (UQSF) ff current (only load Rref, Zref in limitedcontrl) | 6.7s **Good**                          | **UQSF**                                                |
| 78286       | Repeat, using 71464 basis shape in isousn (load all Rref, Zref, Zx1ref in limitedctrl & newrz) | 2.13s Bad                              | UQSF                                                    |
| 78287       | Repeat 78285, but using 71464 basis shape                    | **bad**                                | UQSF                                                    |
| 78288       | Restore 78285, using 71464 basis shape, tune IP at 0.2s & Rref at 0,2s | 3.96s SMBI3 gas in                     | UQSF 充气导致？                                         |
| **78289**   | Repeat，call 78282 gas injection                             | 6.9s **Good**                          | UQSF                                                    |
| **78290**   | Repeat, using 78284 FF                                       | 7.5s **Good**                          | USN                                                     |
| 78291       | Repeat 78289                                                 | 3.52s Bad                              | UQSF 充气                                               |
|             |                                                              |                                        |                                                         |



## 2018/07/04

78373: restore 78209, open PFC MIMO (System), IC voltage-driven mode; Lost control after 2.78s.



## 2018/07/09

78663:wyh，test  for X-point MIMO control.  fl34坏了导致PEFIT重建错误，控制误差计算也是错误的。实验结果无法判断有效。



## 2018/07/10

实验计划：

1. 2.9s加入LHW 4.6G 基底（0.6MW？）， ECR3 0.5MW，保证L模；3.0s到4.5s密度到2.5；4.6s开始升功率到满功率; (4 shots+2shots gas injection)

**Reference shot:** 78289 & 78290 (x 未完成)

2. MIMO control

3. Vloop calculated dz/dt for vertical control

4. Radiative feedback test (piggyback)

**Shot lists:**

**IC voltage-drive mode**.

| shot number | setting                                                      | results                                    | comments                                                     |
| ----------- | ------------------------------------------------------------ | ------------------------------------------ | ------------------------------------------------------------ |
| 78787       | Restore **78289**, call LHW (2.45G 0.5MW; 4.6G 0.6MW) & ECR3 in at 2.9s; Density target: 1.2 | Bad density FB. 2.95s                      | Wrong setting for Density FB from POINT                      |
| 78788       | Repeat, ECR3 start at 4.5s (pulse 2s), LHW 2.45G start at 2.9s, 4.6G from 4.6s (PCS ctrl); density 1.2; | 4.6s; not good.                            | IT reduce 0.5kA for ECE                                      |
| 78789       | Repeat, remove all RF heating.                               | 6.42s; oscillation                         | ohmic shot                                                   |
| **78790**   | Repeat, tune density FF                                      | 7.45s; better                              | ohmic shot                                                   |
| **78791**   | Repeat, ECR3 start at 4.5s (pulse 2s), LHW 2.45G start at 2.9s, 4.6G from 4.6s (PCS ctrl); density 1.2; | 6.16s;                                     | not too bad.                                                 |
| 78792       | Repeat, increase density from 3.0s to 2.2 until 6.6s.        | 3.58s                                      | Seems MIMO ctrl has a bad  anti-interference                 |
| 78793       | Restore 78260, 4.0s disturb on PF7&8 to test $dz/dt$ calculation from vloop measurements | bad;density control bad?                   | Is this the reason?                                          |
| 78794       | Repeat, tune density ctrl                                    | bad                                        |                                                              |
| **78795**   | Restore 78260, no modification at all                        | Good.                                      | Are there some differences for these  shots? Calibration data problem? |
| **78796**   | Repeat, increase density from 2.9s (1.2) to 3.5s (2.0s) till ramp-down; After 4.0s call disturbance on PF7&8 for $dz/dt$ estimation by Vloop measurements | 5.0s. Good.                                |                                                              |
| **78797**   | Repeat，slow velocity distrubance on PF7&8 after 5.0s.       | 7.1s; Good                                 | Provide calibration data for vloop differential calculation (VDC) for z estimator |
| 78798       | Repeat, slow velocity disturbance same, with z estimator by vloop differential calculation on Ematrix 'rx1'; | 6.8s; not bad                              | The Z estimator by VDC is not consistent with lmsz & efit (zcur) |
| 78799       | Restore 78373, start Italy IP control from 2.2s (2.7s for 78373); PFC MIMO ctrl turns on from the beginning | 2.2s; bad. Seems bad PFC MIMO ctrl?        | MIMO test for Italy colleague                                |
| 78800       | Repeat, turn on PFC MIMO ctrl at 1.41s                       | 2.2s; Bad. Confirm the problem on PFC MIMO |                                                              |
| 78801       | Restore 78262, new Mmatrix with increased  weight (2 times) on X-points (Both Br&Bz) & reduced weight (0.3 times) on seg 2,4 & 5. | 3.1s, not good                             |                                                              |



## 2018/07/13 (Friday)

**Future shots:**

| Name     | 78289_uqsf_siso                                              | 78290_usn_siso                                               | 75693_78373                                                  |
| -------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Setting  | 1. Restore 78289; 2. using limitedcontrol whole shot (no newrz now); 3.restore siso M matrix from 78185 (reversed M matrix from 54265 which is an iter-like LSN shape) | 1. Restore 78290; 2. using limitedcontrol whole shot (no newrz now); 3.restore siso M matrix from 78185 (reversed M matrix from 54265 which is an iter-like LSN shape) | 10s discharge, based 75693 (lost control after switching to isoflux), calling 78373 Discharge->short start; Modified the efit start time to 2.7s (consistent with isoflux), PEFIT->Isoflux Sequence to 4 (UpperSNull), keep effective magnetic diagnostics same as 78926 in efit & petit both. Restore 78373 "ip control" & "isoflux" category. Turn off the ip feedback on "limitedcontrl" & "newrz" phase. |
| Comments | M matrix for 78289 is a MIMO matrix 'usnitaly'               | MIMO matrix 'usnitaly' for 78290                             | Feedforward isn't consistent between limitedcontrl & newrz, make it consistent. |

**Plan:**

- [x] PCS switch to new version for $dz/dt$ estimator by vloop measurements (before shot 78955)

- [x] UQSF MIMO ctrl for italy colleague, future shot: 75693_78373
  - [ ] can not repeat the shot, because of the newrz phase failed by $dz/dt$ estimator.
- [ ] $dz/dt$ Vloop estimator (wyh)
- [ ] gap control (hy)

**Shot lists:**

78955 - 56: Ohmic shot. Restore 78809. No breakdown. There are larger delay for plasma breakdown in 78955. Operators thought the PCS sytem update makes the breakdown failed. 

78957: tune gas injection. **Good** ohmic shot. Which confirmed their guess is wrong.

- [x] IC in voltage-driven mode

| shot number | setting                                                      | results                                                      | comments                                                     |
| ----------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 78958       | restore future shot 75693_78373; remove rx2 PID              | Lost control after switching to vs ctrl (newrz phase) at 2.1s, the dz/dt estimator may give a wrong value after updating the algorithm. **Bad** | new pcs version for $dz/dt$ estimator by vloop measurements  |
| 78959       | Repeat, remove the GP_rx2 in newrz phase. 4 Italy colleague  | Not bad. Lost control at 2.75s. Can get rid of the  VS algorithm. | Cycle time is wrong. Need pay more attention, because the stored segments error will be not correct. |
| 78960       | restore 78260, PF7&8 disturbance between 4s to 6s for $dz/dt$ calibration | breakdown, but failed to ramp-up                             | rtefit did not works                                         |
| 78961       | Repeat, tune gas injection at beginning                      | OK. 2.8s lost control. Did not reach the disturbance time window. Not works for calibration. |                                                              |
| **78962**   | Repeat, start rtefit at 2.7s.                                | 6.59s. Good.                                                 | rtefit works fine.                                           |
| 78963       | Repeat, using new $dz/dt$ estimator by vloop measurements with calibrated coefficients | 2.78s. Not good. Not too bad.                                | wyh's shot                                                   |
| **78964**   | Restore 78959, modify the cycle time: CPU1~7   100 500 4000 100 1000 100 500 | 3.04s. Not bad.                                              | 4 Italy colleague                                            |
| 78965       | restore 78957, gap ctrl test by hy & wyh                     | 1.0s. Not too bad..                                          | **1st Gap ctrl shot**.                                       |
|             |                                                              |                                                              |                                                              |

**Next week experiment plan meeting**

Location: 1st floor meeting, Division 7



## 2018/07/16 (Monday)

- [x] Meeting with CREATE group to discuss the MIMO control experiments 
  1. 1st floor meeting, 9:30AM - 
  2. show the results: EAST MIMO ctrl, VS ctrl, Vloop $dz/dt$ estimator
  3. discuss the experiment plan for this week
- [x] **Future shot:** USN shot: **78290_usn_qsfCom**: based on 78290, using new FF based on scenario file "pcs_ff_180701.00030"
- [x] **MIMO control**:

**IC in voltage-driven mode** now, IT = -9kA (~2.0T)

| shot number | setting                                                      | results                                         | comments                                                     |
| ----------- | ------------------------------------------------------------ | ----------------------------------------------- | ------------------------------------------------------------ |
| ~~79283~~   | Restore 78290,  using new M  matrix (usnitaly78290), using FF from futureshot :78290_usn_qsfCom | pcs watchdog                                    | 偶然事件？timeout; **USN**                                   |
| 79284       | Repeat,                                                      | Good. 7.16s                                     | oscillation may come from the strong SMBI3 injection; **USN** |
| 79285       | Repeat, tune the density FF to get rid of the SMBI3 strong injection | Good. 7.1s                                      | LHW (4.6G 1.2MW + 2.45G 0.4MW) may relieve the oscillation; **USN** |
| **79286**   | Repeat, turn off all LHW                                     | Good. 7.17s                                     | Smaller oscillation; **USN**                                 |
| 79287       | Repeat, change GI to 500 (from 10), TauI to 50 (from 1)      | Good. 7.33s                                     | Br & Bz, seg06 becomes better, but seg08 & 09 worse. **USN** |
| 79288       | Repeat， change GI from 500 to 1000， TauI from 50s to 100s  | Good. 7.4s                                      | Almost same with 79287; **USN**                              |
| **79289**   | Restore 78289 Discharge shape & ISOFLUX category, change the MIMO matrix with new one (usnitalyQSF289) | Good. 7.53s                                     | Perfect. No oscillation; **UQSF**                            |
| 79290       | Repeat, change GI to 1000 (from 10), TauI to 100 (from 1)    | Bad                                             | watch dog                                                    |
| 79291       | Repeat 79290                                                 | big oscillation after 3.4s, 4s plasma died      | We don't know the reason, before 3.4s are same with last shot. |
| 79292       | Repeat, change GI to 500 (from 1000), TauI to 50 (from 100)  | big oscillation 3.6s then lost ctrl after 4.23s | Still no ideal why?                                          |
| **79293**   | Restore 79289                                                | Good. 7.44s                                     | Repeatable; UQSF                                             |
| 79294       | Restore 78271, change M matrix (usnitalyQST78271)            | Good. 6.72s                                     | Repeatable ; UQSF 300kA                                      |
| **79295**   | Restore 79289, calling LHW from 2.9s, increase density from 3.0s to 3.3s from 1.2 to 2 | 3.27s                                           | UQSF 250kA, MIMO ctrl                                        |
|             |                                                              |                                                 |                                                              |

- [x] **3rd shift**:

| shot number | setting                                                      | results                 | comments                        |
| ----------- | ------------------------------------------------------------ | ----------------------- | ------------------------------- |
| 79296       | Restore 77140                                                | no effective            | wrong setting                   |
| 79297       | Repeat 77140,                                                | breakdown, but bad ctrl | IC still in voltage-driven mode |
| **79298**   | Repeat, tune the shot start, change IC to current-driven mode |                         | IC in current-driven mode now   |
|             |                                                              |                         |                                 |
|             | **Shot list can be found in LogBook.**                       |                         |                                 |

沈晗弘 -- Miss Shen Heather(海瑟)



## 2018/07/17 (Tuesday)

- [x] MIMO ctrl with IC in voltage-driven mode

| shot number | setting                                                      | results                                                      | comments                                     |
| ----------- | ------------------------------------------------------------ | ------------------------------------------------------------ | -------------------------------------------- |
| 79363       | Restore 79295, new FF at 3.0s & 6.0s; (LHW from 2.9s & increase density from 3.0s to 3.3s from 1.2 to 2) | Bad. 2.1s.  PID for RX2 need be zero with new PCS version (05_10.186) | Check the reliability of MIMO ctrl with UQSF |
| **79364**   | Repeat, Setting PID for RX2 in limitedcontrol to zero in this  new PCS version (05_10.186) | 3.5s. Oscillation too. Saturated voltage required            | UQSF                                         |
| 79365       | Repeat, switch to new M matrix (usnitatly UQSF79295) at 3.1s | 3.5s. Saturated voltage                                      |                                              |
| 79366       | Repeat pulse #79289 with MIMO-PFC and Ip controller with parameters (kp=-2e-5, Ki=-0.17, Kd=0; Tp=1e-4 s; Ti=100s) from 2.1s. Continue with MIMO-PFC and isoflux controller from 2.7s with a transition time on 0.5s (to 3.2s). | Bad. 2.1s. PID for RX2 need be zero  with new PCS version (05_10.186) |                                              |
| 79367       | Repeat                                                       |                                                              |                                              |



## 2018/07/19(Thursday)

- [x] Future shot for USN:

1. **78290_usn_siso_2**: retrive future shot setting from 78290_usn_siso, then reload the FF from future shot 78290_usn_qsfCom which is has new FF based on designed scenario from pcs_ff_180701.00030. Change IC to **current-driven mode**, using limitedcontrol for RZIp ctrl only, PID for limitedcontrol comes from 69888.

   ** 78290_usn_siso is based on voltage-driven IC. But I already switched the IC to current driven mode now. Should pay more attantion if we want to run IC in voltage-driven mode.

2. **79295_newFF**: based on 79295 (with LHW) and using new FF current for isoflux (Need change to RZIp ctrl too.) from Italy colleague with sheet 1 in file "IFF_79295_19_07.xlsx".

3. **79295_newFF2**: based on 79295 using new FF current with sheet 2 in file "IFF_79295_19_07.xlsx" (only move the FF at 3.0s to new FF at 3.2s)

   1. New Matrix from M_79295_17-July-2018_250kA_highBeta_UQSF.xls file are loaded into 79295_newFF2.

## 2018/07/20(Friday)

- [x] Shot lists:

| shot number | setting                                                      | results                                                      | comments                                              |
| ----------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------------------------------------- |
| 79549       | Gap ctrl test                                                | 4.74s                                                        |                                                       |
| 79550       | Gap ctrl test, tune GI for Gap                               | 4.71s                                                        |                                                       |
| 79551       | Gap ctrl test switch at 0.8s                                 | 1.06s                                                        |                                                       |
|             | **IC in voltage-driven mode**                                |                                                              |                                                       |
| ~~79604~~   | Restore future 79295_newFF, except the Density & gas injection; LHW 4.6G from 2.85s 2MW. Density increased from 1.2 at 3.0s to 2.0 at 3.2s till ramp-down | 3.47s; PS1 saturated too early (2.0s)                        | Too high density before reaching the MIMO phase; UQSF |
| 79605       | repeat, tune density.                                        | 3.57s; PS1 saturation becomes better                         | UQSF                                                  |
| **79606**   | Repeat, using FF from future shot: 79295_newFF2; extend the FF time to 3.2s. | 3.71s. No voltage saturation now, but oscillation killed the plasma. | UQSF                                                  |
| 79607       | Repeat, switch to new M matrix at 3.3s (may fail)            | 3.6s. Not bad. But the switcher seems too quiet.             | UQSF                                                  |

## 2018/07/21(Saturday)

- [x] Shot lists:

| shot number   | setting                                                      | results                                | comments                                                     |
| ------------- | ------------------------------------------------------------ | -------------------------------------- | ------------------------------------------------------------ |
| 79637         | Restore future shot: **78290_usn_siso_2**, ic in current-driven mode | 2.13s; VDE?; Why lost ctrl             | $\gamma \approx 100$                                         |
| ~~79638~~     | DAQ communication error. Abort                               | No gas injection.                      |                                                              |
| ~~79639~~     | Repeat                                                       | No gas injection                       |                                                              |
| ~~79640~~     | Repeat 79637,                                                | PCS watchdog                           |                                                              |
| **79641**     | Repeat 79637                                                 | 2.13s;                                 | same problem                                                 |
| 79642         | Repeat 79637, M value for ZX1 to 2 (from 1.5)                |                                        |                                                              |
| 79643         | Repeat, M_Zx1 = 1.5; Gd_Zx1 = -3e6 (from -1e6)               | 2.11s;                                 | limitedctrl里面Zp_GP在2.1s减小！！                           |
|               | **IC** switch to **voltage-driven** mode                     |                                        |                                                              |
| 79644         | Restore 79289,        trigger Vertical displacement for fix dz/dt signal from vloop | 2.39s; did not reach the setting phase |                                                              |
| 79645         | Restore 79289,                                               | 4.82s; big oscillation                 |                                                              |
| **79646**     | Repeat 79289, same setting.                                  | 7.51s                                  |                                                              |
| 79647         | Repeat,  use dz/dt from dvloop @2.1s                         | 2.47s;large oscillation                | wyh                                                          |
| **79648**     | Restore 79646, Increase LHW 4.6G from 0.6MW at 2.8s to 1.2MW at 3.4s; density from 1.2 at 3.0s to 1.8 at 3.5s | 3.45s                                  |                                                              |
| 79649         | Repeat 79647, Zx2_taup = 0.1ms                               | 2.26s                                  | wyh                                                          |
| 79650         | Repeat 79648, Tune FF in isousn                              | 3.34s                                  |                                                              |
| 79651         | Repeat, tune density target                                  | 3.65s                                  |                                                              |
| **79652**     | Restore **79606**, with 651's density, remove FF at 6.0s in isousn | 3.53s                                  | not good                                                     |
| **79653**     | Repeat, but switched to new Mmatrix at 3.3s in isousn (M_79607_21-Jul-2018_250kA_highBeta_UQSF_2.xls) | 4.26s                                  |                                                              |
| 79654         | restore 79647， K1->0.18                                     | 2.44                                   | wyh                                                          |
| ~~79655~~     | Restore 79653, move the M matrix switch time to 3.2s         | watch dog problem                      |                                                              |
| 79656         | Restore 79653, move the M matrix switch time to 3.2s         | 4.96s. Still with oscillation.         |                                                              |
|               | **IC** siwtch to **current-driven** mode                     |                                        | USN                                                          |
| 79657         | Restore 79641, remove PID changed for Z at 2.1               | 2.8s;                                  | Xpt ctrl is Br&Bz                                            |
| 79658         | Repeat, using Xpoint ctrl for Xpt                            | 2.8s;                                  |                                                              |
| 79659         | Repeat, increase M_Zx1 from 1e4 to 2e4                       | 2.88s; Better Zx ctrl                  |                                                              |
| **79660**     | Repeat, increase M_Zx1 from 2e4 to 4e4                       | 2.94s. Zx1 drift direction changed     |                                                              |
| 79661         | Repeat, reduce M_Zx1 from 4e4 to 3e4; using new basis shape from 79660@2.7s | 2.82s                                  | PS6&PS8 saturated                                            |
| 79662         | Repeat, M_zx1=1e4; calling PID in isousn from ==52465== (isosn) | 2.91s                                  | PS6&PS8 saturated                                            |
| 79663         | Repeat, tune seg02 & 05 PID to reduce the saturation on PS6&8 (GP from 1 to 0.13, remove GI) | 2.88s                                  | with LHW after 2.8s                                          |
| **79664**     | Repeat, remove M_seg05_PS10; Gp for seg02&05 to 0.5          | 6.94s; Good                            | with LHW                                                     |
| ==**79665**== | Repeat, add GI=5 for seg02&05                                | 7.18s; Good                            | with LHW                                                     |
| 79666         | Repeat, add more LHW                                         | 7.22s; Good                            |                                                              |
| ~~79667~~     | Repeat, call ECR (3.0s 1MW) in                               | 2.95s;                                 | 杂质爆发？                                                   |
| 79668         | Repeat,  ECR (3.0s 1MW); 2.45G LHW 4.0s 0.5MW                | 6.98s;                                 |                                                              |
| ~~79669~~     | Repeat, density target increased to 2.2;                     | Wrong setting. Protection              |                                                              |
| ~~79670~~     | Repeat, fixed density chord calculation.                     | 3.23s                                  |                                                              |
| 79671         | Repeat, tune the density (target & gas injection)            | 6.85s                                  |                                                              |
| ~~79672~~     | Repeat, more slow LHW 4.6 input, reduced gas injection; Modified GI for seg02 & 05 to 10 (from 5) | 3.44s                                  |                                                              |
| ~~79673~~     | Repeat, tune the gas                                         | No gas in                              |                                                              |
| 79674~79676   | Repeat                                                       | 3.45s/3.39s/3.87s                      | Bad                                                          |
| 79677         | Restore 79665                                                | 2.98s                                  | Bad                                                          |
|               | <u>Gap ctrl test</u>                                         |                                        | wyh, yh                                                      |
| ==79678==     | Restore 79636, 0.8s to gap ctrl                              | 8.06s                                  | Good                                                         |
| 79679         | Repeat                                                       | 9.03s                                  | Good                                                         |
| 79680         | Repeat, more LHW 4.6G to 2MW                                 | 9.39s                                  | Good                                                         |
| 79681         | Repeat, PFC MIMO started at beginning.                       | Bad                                    |                                                              |
| 79682         | Repeat, PFC MIMO started at 1.4s                             | bad. 1.71s                             |                                                              |
| 79683         | Repeat, Gap ctrl in ohmic shot                               | 8.18s                                  | Good                                                         |
| 79697         | Restore 79680, NBI ctrled by PCS test                        | watch dog                              |                                                              |
| 79698         | Repeat                                                       | 9.55s                                  | Good                                                         |
|               | <u>USN scenario with SISO ctrl</u>                           |                                        |                                                              |
| ~~79699~~     | restore 79665,                                               | watch dog                              |                                                              |
| 79700         | Restore 79665,                                               | 7.36s                                  | Good                                                         |
| 79701         | Repeat, fixed the density chord calculation problem; more LHW | 7.13s                                  | Good                                                         |
| ~~79702~~     | Repeat, increase density & LHW                               | Bad breakdown                          |                                                              |
| ~~79703~~     | Repeat                                                       | Bad breakdown                          |                                                              |
| ~~79704~~     | Repeat                                                       | watch dog                              |                                                              |
| 79705         | Repeat, increase density & LHW (2.2MW)                       | 7.28s                                  |                                                              |
| 79706         | Repeat, using POINT FB density                               | 7.28s                                  |                                                              |
| 79707         | Repeat,                                                      | 7.1s                                   |                                                              |
| 79708         | Repeat, start LHW earlier (2.6s)                             | 7.0s                                   |                                                              |
| 79709         | Repeat, start LHW earlier (2.5s), increase IP from 0.25MA at 4.0s to 0.35MA at 5.0s (6.5s ramp-down) | 3.16s; bad                             |                                                              |
| ==**79710**== | Repeat, start LHW 2.6s; 电流控制                             | 7.41s; Good                            | 升IP电流                                                     |
|               | ==<u>IC in voltage-driven mode</u>==                         |                                        | UQSF shape                                                   |
| ~~79711~~     | Restore  79289; fix the density chord calculation; PFC MIMO test from 4.0s to 5.0s; LHW from 2.7s | 2.1s because of Rx_2                   | Bad setting                                                  |
| 79712         | Restore  **79289**; fix the density chord calculation; PFC MIMO test from 4.0s to 5.0s; Remove LHW trigger | 4.94s. PFC MIMO problem                |                                                              |
| ~~79713~~     | Repeat, remove PFC MIMO; change the plasma shape (Rp) from 3.5s to 4.0s (0.5cm) | 0.81s                                  |                                                              |
| **79714**     | Repeat,                                                      | 5.23s; density too high                |                                                              |
| 79715         | Repeat, increase Rx2_Taup=10                                 | 2.45s;                                 | high frequency oscillation                                   |
| 79716         | Repeat, increase Rx2_Taup=20                                 | 2.31s                                  | HFO                                                          |
| 79717         | Restore 79708, but using voltage IC ctrl                     | watchdog                               |                                                              |
| **79718**     | Restore 79708, IC in voltage-driven mode                     | 6.74s                                  | Not bad;When IC in voltage-driven mode, the IC current pass over zero, the oscillation shows up |

