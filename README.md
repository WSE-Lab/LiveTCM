# LiveTCM:  A Tool with Restricted Natural Language and Model-based Adaptive Test Generation for Autonomous Driving

- [LiveTCM:  A Tool with Restricted Natural Language and Model-based Adaptive Test Generation for Autonomous Driving](#livetcm--a-tool-with-restricted-natural-language-and-model-based-adaptive-test-generation-for-autonomous-driving)
  - [1. Contribution](#1-contribution)
  - [2. Introduction](#2-introduction)
  - [3. Features of LiveTCM Tool](#3-features-of-livetcm-tool)
      - [1. Model Tree](#1-model-tree)
      - [2. TestSetup](#2-testsetup)
      - [3. TestCaseSpecification & Reference](#3-testcasespecification--reference)
      - [4. Auto-Completion](#4-auto-completion)
      - [5. Alternative Flows](#5-alternative-flows)
        - [oracle verification flow](#oracle-verification-flow)
        - [global verification flow](#global-verification-flow)
      - [6. Dynamic generation](#6-dynamic-generation)
      - [7. Reply execution](#7-reply-execution)
      - [8. Switch Mode & Pause and Stop execution](#8-switch-mode--pause-and-stop-execution)


## 1. Contribution
This work has the following contributions: 1) proposed a web-based and executable TCS editor with the features of manually specifying TCSs, displaying generated TCSs and execution logs, and highlighting executing steps at runtime; 2) proposed test and TCS generators, which together with an execution engine, supports fifive application contexts, such as step-wise or automatically executing already specifified TCSs, and generating TCSs while execution, by interacting with the SUT and its operating environment via plugged-in REST APIs; and 3)implemented an integrated and extensible framework for supporting automated testing of ADSs.

## 2. Introduction

To support automated testing of continuously evolving ADSs, we propose a novel methodology, named LiveTCM, to automatically execute and generate test case specififications (TCSs) by interacting with an ADS under test and its environment. LiveTCM is evaluated with an open-source case study (i.e., Apollo Open Platform). LiveTCM is based on RTCM. However, RTCM is not effective for testing ADSs since it statically generates executable test cases from test case specifications (TCSs), similar to use case specifications.

An overview of LiveTCM is shown here. It supports the full life cycle testing of evolving systems. LiveTCM is equipped with two types of TCS editors. One is for manually specifying TCSs (i.e., the TCS Editor) and the other is for dynamically completing TCSs (i.e., the Executable TCS Editor).

<img src="./figures/overview.png" alt="overview" width="500" align="bottom" />

## 3. Features of LiveTCM Tool

Here, we show the features of LiveTCM and screenshots.

#### 1. Model Tree

LiveTCM provides a model tree to create elements. Here, Tester can create or delete elements pre-defined in metamodel, such as Test Setup, TestCaseSpecification, Tester, UseCase and so on.

![Alt Text](./figures/ModelTree.gif)

#### 2. TestSetup

Tester can specify Test Setup in Test Setup model view. It includes basic information and a flow. Tester can do some initialization work for the test in the flow.

![Alt Text](./figures/TestSetup.gif)

#### 3. TestCaseSpecification & Reference

Tester can specify TestCaseSpecification in TestCaseSpecification model view and refer to a test setup, then the view will import the test setup.

![Alt Text](./figures/Reference.gif)

![Alt Text](./figures/TestCaseSpecification.gif)

#### 4. Auto-Completion

The figure shows the function of auto completion for API.

![Alt Text](./figures/AutoCompletion.gif)

#### 5. Alternative Flows

##### oracle verification flow

Tester can create oracle verfication flow by the down arrow and make reference to the corresponding step in basic flow.

![Alt Text](./figures/oracleflow.gif)

##### global verification flow

Global verification flow can be reused by the function of copy and paste.

![Alt Text](./figures/globalflow.gif)

#### 6. Dynamic generation

LiveTCM automatically generates basic flow instead of manual specifying.

![Alt Text](./figures/dynamic.gif)

#### 7. Reply execution

LiveTCM can reply the execution by statically execute model.

![Alt Text](./figures/reply.gif)

#### 8. Switch Mode & Pause and Stop execution

The tester can switch the dynamic mode and static mode between execution by right-clicking the prepend of step and switch mode. The figure also shows the functions of debugger: Pause and Stop.

![Alt Text](./figures/switch.gif)
