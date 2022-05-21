[[2022-05-17]] | [[Tamturbo]]
#meeting/tamturbo

#### Participants

<u>Tamturbo</u>
 Liro Hjerppe : purchasing engineer for 3months
 Brecht Vanlee : in charge of commercial in AC before
 Igor Nagaev: CEO since oct 2021
 Juha Lammi : technical
 Perttu Pitkaniityy: sourcing manager


<u>Tamturbo (remote)</u>
Kari :  in charge of the design
Mihail : head of turbodesign & thermo

<u>SKF</u>
Ramdane, François, Jean-Charles, moi

#### Notes

<u>Projet TT265 :</u>
Jean-Charles partage son planning
![[Pasted image 20220517105641.png]]

Main risk for JC : availability of FSE in August. It could
They are acquiring the parts (impeller is a challenge)

<u>Juha presents TT265</u>
- TT265 design selected
	Motor 1 : AB75 pressure ratio 2.35
	Motor 2 : AB150 2nd & 3rd stage
	using the patent of AC (to make the motor 1 single stage, motor 2 with stages 2&3, and making it more flexible)
- For Juha : 5 to 9bars is medium pressure
- I asked *risk of not having sales if no references*, for Igor the existing references are enough to propose this variation

*Decision :* Jean-Charles will add the 3 stages shown by Juha in his planning

<u>Juha presents TT265 - prototype stage 1:</u>
The less cooling allows having less parts, and improve the reliability.
They do *energy recover* with the heat exchangers which is part of their offer.
![[Pasted image 20220517112158.png]]

<u>Juha presents TT265 - prototype stage 2:</u>
TT3 is using 2 AB150
Heat exchangers & cooling are expensive, total cost is 20% of total cost for the TT3
Efficiency lost of heat exchangers is xx.
Heat exchangers heat recovered is a significant part of the offer.
10% to 12% is going for losses, 90% if for heat exchangers
![[Pasted image 20220517112833.png]]


<u>Note </u>
Atlas Copco & Ingersoll rand are using service factor up to 1.20 to 1.25 to present their motors

*Important :* They ask what is the IE efficiency of our motors for Brecht

- [ ] For *Igor* : they need a *white paper* of our PM motors vs alternative motors AC (customers have technical skills to understand like in Nestle) / #ramdane_lateb 
	*Important criterias for the customer accordint to Brett* : Selection IP rating, efficienccy class, internal vibrations of our magnetic bearings
	For Brett, it takes the exemple of our solution for subsea to confirm our reliability
- [ ] Confirm the arguments needed / #brett ?

<u>Présentation MBx et Cronos</u>
links : [[MBx]] | [[Cronos]]

We talked on our path to calculate our CO2 impact and we want to reach the carbon neutrality, and MBx will be included in that roadmap.
For Cronos, some data we are getting could help Tamturbo to improve their solution (how close to the surge, etc ). *Igor* emphasized on that, and he would like to be involved as much as possible.

Brett said the surge line distance is a major sales argument.
Yuha mentionned they are the application specialist, eg the pollution of the impeller weight for the pollution.

- [ ] Organize a common review of the functionnalities once we are more ready on cronos #eduin / #jean-charles in #june

<u>Cronos review PM </u>

Ambiant of 55°C for *Igor* would be better than 40°C (not a clear need of Tamturbo but he thinks it would be better for us).
For Juha, most of the US need to have an ambiant of +55°C.

Eduin said both horizontal and vertical integration are planned

*Igor* suggests dynamic sempling of the data in case of close to surge


<u>Discussion with Frederic</u>

Online business discussion in 3 weeks.
Frederic needs to present magnetic, we could organize a video with quesitions and answers with them here.
The video will be taken by Charles tomorrow AM.

From 3PM to 4PM, Frederic will be with us
and Frederic will be with us tomorrow AM.


<u>Finalization of the discussion of MB80</u>

Jean-Charles explained that the magnetic bearing will have an interface, and rotor will be changed.
So the rotor dynamic will have to be done once more.
Jean-Charles said we could this remotely, or it could be done in Vernon in static and the dynamic remotely.


<u>AC150</u>
link : [[AC150]]

Unbalance found at 30000rpm.
So we are rebuilding new rotors for June.

Ramdane asked if removing the LC filter would be interested for the same cost ?

Our 2 solutions for the drives :
a. SIC solution of [[Phase]] with LC
b. Solution of [[Sieb and Meyer]] that should work without LC filter

For the problem of AC150 the solutions we plan are :
a. keep the actual design
b. modify the rotor with a compromise on speed and/or power
Jean-Charles said we should have this feedback within 3 weeks

Igor said their assumption was that the machine would be at 60000rpm.
Juha said the customer is looking for €/kW.

*Igor* said 80% is energy after 5 to 10years.
He said there are selling the most efficient compressor. If we make the power less, then the kW/m3 used is increasing and that's an important factor.

Juha said for the smaller range, the cost is the key driver (so the TT1). So reducing the power will make it more expansive. If going for TT1 with 3 stages, it would make it expansive for the heat exchanger.

*Igor* :
==TT1 should be at same level of efficiency than dry screw when they start. But the dry screw is having wear over time which degrades over time. And screw needs to be paid every 6 years of overhaul (you pay at least 2 or 3 times over the full life).==
For the biggest machines, efficiency in favor of magnetic bearing is even more

Brecht : The market they are today is only 10% of where they could be with the TT1

The TT1 is starting at 90kW.
For Igor, 60000rpm is key to reach the efficiency.

They will not propose heat recovery for 90kW, the payback is not enough.

We need the heaviest impeller to use the AC150.
- 0.6kg for the AC for TT1 on 1 side, other is half.
- impeller diameter depends of rotation speed, pressure ratio. If they will be the same, then the weight will be the same. 
- first stage pressure ratio will be about 4 here, 60000rpm => diam = 115mm
- if the pressure ratio is decreasing (since we will go from 2 stages to 3 stages), diameter is decreasing
- [ ] heaviest impeller to TT3 / #juha 

 linear approx from Mina : radius x rotation speed need to be constant (tip speed)
 
Jean-Charles is asking if we could lower axial load. Mina said between rotationnal speed is more important than the axial load.

<u>Review the AC150 from Juha</u>

![[Pasted image 20220517152446.png]]

*Note* : The pressure ratio of the TT1 (2 stages) of 3.6 and 2.8 is the optimum in terms of efficiency. I asked if possible to balance the impellers weight to have a better rotor dynamic, but it would create a lower efficiency
The TT1 would allow 22m3 at 135kW if I have well understood => 6.13kW/m3


Frederic said we need a quick fix like (rotor in 1 part)

*Igor* said he want a compressor of 80 to 90m3/min, so it could be 4 compressors instead of 8 AC150.

<u>Efficiency vs speed for the 2 stages of TT1</u>
TT1 is the orange curve below. Calculation below around 150KW.

![[Pasted image 20220517155001.png]]

![[Pasted image 20220517155709.png]]



60000rpm would be sold 200K€ by machine for Brett

<u>Bigger power compressor </u>

![[Pasted image 20220517162230.png]]

TT145 with TT2 has low efficiency
TT1 can go up to 21m3
TT265 from 38m3 to TT285 42m3 max
TT305 & TT325 in teh wider range currently (51m3 and 55m3 max)

Options :
TT3 TT345 using 2 AB150.
TT4 Bigger power range compressor
They would like a 250kW motor according Jean-Charles (I didn't catched it)

*Ygor* explained *they can adjust the diffuser to match the average consumption of the customer*

They use CFTurbo pour tester leurs machines

![[Pasted image 20220517163840.png]]
For the TT3, if we could push the AC150 to 170kW we could replace the AB150 even with slightly lower speed (confirmed by Juha).
Juha said the speed of AB150 is quite ok for the efficiency, but not for TT4 and TT5.

![[Pasted image 20220517165016.png]]

AB350bis is a 250kW which is 2 stages
![[Pasted image 20220517165302.png]]
We would be on the blue line above so we need to be at least at 50000rpm to 55000rpm

Oil free screw compressors 2 stages are limited to 10bars.
If we can go to 13 bars it could be a unique offer of Tamturbo (eg like for *nitrogen market*)
So the TT2 could run little bit slower to go higher in pressure.
*Ygor* said the *nitrogen market* is half the market of oil free market.

![[Pasted image 20220517170403.png]]
AC350 they need 230kW for the motor 1 at 20000rpm (80% efficiency). But we should target better than to beat the competition. So we need 30000 to 35000rpm.
The second motor cannot be the AC150 because of the torque according to François. We need to reduce the speed linear to the power to keep the torque constant. So ti would be only 100kW on the third stage.

*Ygor* : Glass, big food compressor, the size of 80m3 to 200m2 is constant. And the competition is using 3 compressors.
- [ ] Provide the figures for the business case of such larger compressor #ygor
The need is in 2 years after the change of the existing design (TT1,TT2, and TT3).

*Idea :* si on prend un moteur à induction est-ce que le torque n'est pas constant ce qui peut être intéressant dans certains cas ?

*Ygor* said with the AI, we could propose an alternative diffuser to get a better efficiency. ==Idea for Cronos==

*Decision:* No need to have an AC75 as a priority

<u>AMB cables and optimized MBC </u>
They want to take the cables in their scope of supply
They want to integrate the TT speed sensing board ?

#### MY summary

<u>Their roadmap</u>
First they will use AC150 everywhere
Then they could go to 13bars with the AC150 and probably using the TT2 frame
Then on our side the larger size AC350 would be the next step
We don't need the AC75.
- [x] #me : Faire une roadmap produit de ce que l'on a compris qu'ils vont faire





















