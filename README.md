<h2 align="center">Level controle</h2>
<p align="center"><img src="Documentation\images\level-controle.gif"></p>
  <p align="center">
    Project code in TIA Portal and modeled in FacotryIO
    <br />
    <a href="https://plc-programme-viewer.000webhostapp.com/">View project tree</a>
    ·
    <a href="https://github.com/tentypcic/level-controle-factoryIO/issues">Report Bug</a>
  </p>

## Table of Contents
- [Built With](#built-with)
- [About The Project](#about-the-project)
  - [Features](#features)
  - [Project tree](#project-tree)
  - [HMI panel](#hmi-panel)
  - [Controller](#controller)
- [How To Use](#how-to-use)
  - [Factory IO](#factory-io)
  - [TIA Portal](#tia-portal)
  - [Version Controle Interface](#version-controle-interface)
  - [SIMATIC Automation Compare Tool](#simatic-automation-compare-tool)
- [License](#license)

## Built With
This project was bult using these technologies:
 - [Factory I/O](https://factoryio.com/)
 - [ Siemens TIA Portal V17](https://support.industry.siemens.com/cs/document/109784440/simatic-step-7-incl-safety-s7-plcsim-and-wincc-v17-trial-download?dti=0&lc=en-PL) 
 - [SIMATIC S7-PLCSIM](https://support.industry.siemens.com/cs/document/109795016/simatic-s7-plcsim-advanced-v4-0-trial-download?dti=0&lc=en-PL)
 - [SIMATIC Automation Compare Tool](https://support.industry.siemens.com/cs/document/109797235/simatic-automation-compare-tool-?dti=0&lc=en-DO) 
 - [GIT](https://git-scm.com/)
 
 ## About The Project

This is a PLC programme for level controle.
Code in TIA Portal V17. The tank has been modelled in Factory IO 3D simulation software.

The project includes a simple automation system, a liquid tank with two pumps and a liquid level sensor. From the HMI, we can select the type of controller, its settings and view its operation on the graph.

### Features

 - [x] HMI panel
 - [x] On-Off Controller
 - [x] PID Controller
 - [x] Takagi-SugenoFuzzy-PI Controller
 - [x] Neural network NARX Controller
 - [x] Disturbance

### Project tree
<p align="center"><img src="Documentation\images\project_tree.png"></p>

The programme is structured in four layers. The structure of the programme is similat to the concepts of oop. Each layer is responsible for one main task.

### HMI panel
<p align="center"><img src="Documentation\images\hmi_panel.gif"></p>

The HMI displays basic tank level control information. It shows pump status, sensor status, operating mode, controller selection and includes a waveform graph. From the HMI we can change the default controller settings.

### Controller

The programme includes controllers written in scl and lad.

### Ramp
<p align="center"><img src="Documentation\images\ramp.png"></p>

In automation systems, ramp functions are commonly used as input signals for controllers or actuators, and as a means to smoothly start, stop or regulate the speed of a mechanical system. A ramp is a mathematical function that describes a gradual increase or decrease in the value of a signal over time.

### On-Off
<p align="center"><img src="Documentation\images\on-off.png"></p>

An on-off controller with hysteresis, also known as a hysteresis controller, is a type of control system used in automation and process control. It is a simple and cost-effective way of controlling a system by turning it on and off based on a set of threshold values, while also introducing a small amount of hysteresis to prevent rapid switching between on and off states.

### PID
<p align="center"><img src="Documentation\images\pid.png"></p>

The incremental PID algorithm is a variation of the classic PID control algorithm used for feedback control systems. It is a form of PID control that calculates the output of the controller based on the change or increment in the input rather than the absolute value of the input. In the incremental PID algorithm, the controller calculates the output by considering the difference between the current input and the previous input, as well as the difference between the current error and the previous error. By taking these differences, the controller calculates the incremental change in the output needed to adjust the system and achieve the desired setpoint.

### TS
<p align="center"><img src="Documentation\images\ts.png"></p>

The Takagi-Sugeno (TS) fuzzy PI controller is a type of controller that uses fuzzy logic to adjust the proportional and integral gains of a PI controller based on the current operating conditions of the system. The TS fuzzy PI controller is a variation of the classical PI controller that is commonly used in industrial control systems.

The TS fuzzy PI controller works by first defining a set of fuzzy rules based on expert knowledge or experimental data about the system being controlled. These fuzzy rules describe the relationship between the system's inputs and outputs and are expressed in terms of linguistic variables, such as "low," "medium," or "high." These rules are then used to construct a fuzzy inference system, which determines the appropriate proportional and integral gains for the PI controller based on the current values of the system's inputs.

#### NARX

NARX (Nonlinear Autoregressive with eXogenous inputs) neural control is a type of neural network-based control system used for modeling and controlling nonlinear dynamical systems. It is a variation of the classical NARX model, which is commonly used for time-series prediction and system identification.

<p align="center"><img src="Documentation\images\narx.png"></p>

The NARX neural control system uses a feedforward neural network to model the behavior of the system being controlled. The neural network takes as input the current and past values of the system's inputs and outputs, as well as any exogenous inputs, and uses them to predict the future output of the system. The network is trained using a set of input/output data collected from the system, and the weights of the network are adjusted using a backpropagation algorithm to minimize the difference between the predicted and actual outputs.

<p align="center"><img src="Documentation\images\imc-pid.png"></p>

Once the neural network is trained, it is used as a controller to regulate the behavior of the system being controlled. The controller takes as input the current and past values of the system's inputs and outputs, as well as any exogenous inputs, and uses the neural network to predict the future output of the system. The difference between the predicted and desired outputs is used to adjust the control signals sent to the system to bring it into the desired state.

## How To Use

To clone and run this application, you'll need FactoryIO and TIA Portal (v16 and later) installed in your computer. 

### Factory IO

Download the scene for factory io and move it to the default folder in the `C:\Users\username\Documents\Factory IO\My Scenes`

### TIA Portal

On TIA v17 and later: 
Download an archaised version of the programme and open in TIA

### Version Controle Interface

On TIA v16 and later:
 Download template of the programme and open in TIA
 
    # Clone this repository into your worksapce
    
    $ git clone https://github.com/tentypcic/sorting-by-weight-factoryIO
    
    # Use the Version Control Interface (VCI) in TIA to synchronise programme

<p align="center">
  <img src="https://www.dmcinfo.com/Portals/0/Siemens-VCI-image-2.png">
</p>

### SIMATIC Automation Compare Tool
You can view the functions and blocks in the .xml extension directly using the SIMATIC Automation Compare Tool software.

<p align="center">
  <img src="Documentation\images\act.png">
</p>

## License

Distributed under the MIT License. See `LICENSE` for more information.
