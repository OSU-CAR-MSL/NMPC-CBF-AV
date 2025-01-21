NMPC_CBF_AV implementation

Abstract: The safety of Autonomous Vehicles (AVs) remains a key challenge for developers and stakeholders due to the dynamic environments in which they operate. From a control perspective, nonlinear model predictive control (MPC) is a powerful control strategy to operate in such dynamic environments. This paper evaluates the performance and compares the safety criteria for AV controllers designed using MPC and control barrier functions (CBFs) that ensure safety in obstacle avoidance through the principle of set invariance. With MPC, there are two design approaches: CBFs formulated as a discrete-time constraint (MPC-CBF) or as a quadratic program (MPC-CBF-QP). In addition to CBFs, a more straightforward approach for obstacle avoidance is to use the safe-Distance Constraints in the MPC formulation (MPC-DC). The results of these three nonlinear MPC control strategies: (I) MPC-DC,  (II) MPC-CBF-QP, and (III) MPC-CBF implemented on an actual vehicle in autonomous mode are discussed in detail. Their performance and safety conditions are compared in three common urban and highway driving scenarios: (i) avoiding static obstacles, (ii) sudden pedestrian interaction, and (iii) overtaking the lead vehicle (LV). Based on the experiments, it is observed that the MPC-CBF-QP is computationally efficient and guarantees safety in all considered scenarios, MPC-DC often fails to meet safety requirements in critical scenarios and MPC-CBF performance heavily depends on prediction, control, and CBF horizon.

The three scenarios considered in the paper are: 

(1) Avoiding static obstacles - Scenario

![Static Obstacle - GIF](https://github.com/user-attachments/assets/f1034199-e3f7-4d5f-b6a5-8e9a1a9bd224)

(1.1) MPC-DC controller performance in static obstacle scenario

![Static-MPC-DC GIF](https://github.com/user-attachments/assets/ec6c4aa2-c13c-4ee3-a73c-3c95dba786fb)

(1.2) MPC-CBF-QP controller performance in static obstacle scenario

![Static-MPC-CBF-QP GIF](https://github.com/user-attachments/assets/c44ddbb5-67e2-44c3-bb8c-1789271335b4)

(1.3) MPC-CBF controller performance in static obstacle scenario

![Static-MPC-CBF GIF](https://github.com/user-attachments/assets/831cbbcd-2bf9-43b2-8709-40161e5e900e)


(2) Scenario having a sudden pedestrian interaction -  A pedestrian, initially not in the AV's field of view (FOV), starts moving towards the AV at high speed within a 10-meter radius of the vehicle.

![Video Sudden Pedestrian GIF](https://github.com/user-attachments/assets/7cff3b7d-54f9-4db0-a61e-4c6f092ad3bc)

(2.1)  MPC-DC controller performance in sudden pedestrian interaction scenario

![ped MPC-DC](https://github.com/user-attachments/assets/57ec408c-c443-4f05-98f0-a176530b4400)

