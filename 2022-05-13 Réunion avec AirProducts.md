[[2022-05-13]] | [[Airproducts]]
#meeting/airproducts

#### introduction
<u>Participants</u>
Ethan Eiswerth, Tang Genglin

#### compte-rendu de la réunion
- #2022-05-13 de #askar_gubaidelin : [Air Products SKF - solutions and roadmap for LH2](file:///C%3A%5CUsers%5CBOUCULAT%5COneDrive%20-%20SKF%5CDocuments%5C2022%5CTravail%5C31%20Customers%5CAir%20Products%5CAir%20Products%20SKF%20-%20solutions%20and%20roadmap%20for%20LH2.pptx)
- #2022-05-13 de #mark_hinckley : [[SKF Material - April 25 2022.pdf]]

#### Notes
Revue du plan d'actions préparé par Mark
Revue des slides préparées par Askar

<u>Existing AC150</u>

Speed :
We assume that speed 60000rpm +10% it is a trip signal. Fine for Ethan.
He said the alarm around 63000 rpm.
But between alarm and shut down it could be slighty above 63000rpm.
Good for us

Max power :
Definition it will have to be sustained
The max power+10%  is a margin for short period of time but not continuously (1 min to 1 hr timeframe)
For Ramdane, he doesn't think it is a problem but it will have to be confirmed during the spec review

Impeller :
Mass is around 170g while we wanted to be 130g
We will come back on this subject later

Max static thrust load :
400 N
Can they design laby seals
Ethan asked Genglin to check with ...
Still to be checked by Airproducts

Speed sensor :
Askar explained we analyse the speed signal through LEM sensors, so we cannot provide 3 sensors. So not possible to measure 2 or 3 overspeed detection.
Askar said braking resistance is a need to be discussed with power electronics.
For Ethan it is due to regulations.
For Ethan as long as we provide clean power, it should not be an issue.

Real machine & coupling :
We plan to test it in back to back in generator.
For the coupling it will be fixed with a tie bolt.
And Askar said we plan to expect to do our test in July before sharing the coupling data.
Ethan, they have an alternative solution, and so he is fine to have our tests are done.
The coupling will be used only on 1 side.

Rotor dynamics :
Askar showed the rotor dynamic theoretical model
![[Pasted image 20220513143051.png]]
We will confirm if the calculation is correct or not in the beginning of June or July
Ethan : the extension & weight we have given (130g & 30mm overhang) is according to what we gave to them
Ethan : how often the model vs the reality is close to difference. Askar said that for TEX, there are absolutely no differences. For motors, it is different.
Ethan : could it performs better ? Askar said it can be better or worse
Ethan confirms this timing is matching with their need for the project.
Askar said that for him the challenge will be on their side to reach 30mm laby seals, he thinks it may be 50mm
Askar said also the insert may need to be in 17-4PH to widthstand the cryo temperature.

Shaft extension
Ethan : Does it have to be magnetic or not ?
Askar said no problem

<u>New designs </u>

Présentation par Ramdane :
![[Pasted image 20220513144807.png]]
Ethan : their cycle needs 60000rpm, if back 45000rpm the impact would be large on the efficiency
Ramdane said the only way is by flexible coupling to reach this higher speed, or we need to manage the first critical mode

Ethan : if we agree not to have the 20% margin, could our machine reach their need
For Ramdane, maybe 230kW with light impeller, it could be possible, but it may outstands the standards

Ramdane said is they said the impeller, then we can have a look to see how difficult it is
Ethan ok with the approach, he will send a first estimate

Timeline :
It is expected for an order to be placed in 2024, and delivery in 2026. They may need it faster.

Forecast qty :
10 to 15 units for a first order
6 and 18 units per opportunity after
It could make their equipment to be invested down with such equipment


#### plan d'actions
- [ ] #genglin : Send draft impeller parameters for the 60000rpm 250kW machine

#### decisions


#### My comments
I have the feeling is interested by the AC design, but Genglin is not convinced he will be able to reach our constraint (thrust, weight of impeller)