<h2 align="center">Level controle</h2>
<p align="center"><img src=""></p>

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Built With](#built-with)
- [About The Project](#about-the-project)
  - [Features](#features)
  - [Project tree](#project-tree)
  - [HMI panel](#hmi-panel)
  - [Controller](#controller)
    - [On-Off](#on-off)
    - [PID](#pid)
    - [TSK](#tsk)
    - [NNARX](#nnarx)
- [How To Use](#how-to-use)
  - [Factory IO](#factory-io)
  - [TIA Portal](#tia-portal)
  - [Version Controle Interface](#version-controle-interface)
  - [ACT](#act)
    - [SIMATIC Automation Compare Tool](#simatic-automation-compare-tool)

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

### Features

 - [x] HMI panel
 - [x] On-Off Controller
 - [x] PID Controller
 - [x] Takagi-SugenoFuzzy-PI Controller
 - [x] Neural network NNARX Controller

### Project tree

### HMI panel

### Controller

#### On-Off

#### PID

#### TSK

#### NNARX

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

### ACT

#### SIMATIC Automation Compare Tool
You can view the functions and blocks in the .xml extension directly using the SIMATIC Automation Compare Tool software.