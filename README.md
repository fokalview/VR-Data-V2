# VR Data Visualization Project  
A multidataset breakdown of VR engagement, comfort, and user patterns

---

## Abstract
This project pulls together several independent VR datasets and turns them into a connected visualization system that helps explain how real people experience virtual reality. Instead of treating demographic data, headset usage, immersion scores, and assistive technology availability as separate stories, I combined them into one interactive environment using D3.js.

The goal is simple. Understand what makes VR comfortable, what makes it uncomfortable, and how those factors shift depending on who you are and what you are using. The project uses scatter plots, radar charts, icon based filters, and responsive tooltips to create a clear picture of VR usage patterns across multiple populations. This work is both a technical demonstration and a practical exploration of how design and data can work together to support better VR decisions.

---

## Introduction
VR is growing fast in entertainment, education, and training, but not everyone experiences it the same way. Some people get immersed. Others get sick. Some groups stay in VR longer and feel more comfortable. Some regions have strong access to assistive technology. Others barely have any.

This project started because I wanted to make sense of all these differences in one place. I imported multiple CSVs, cleaned them, and built out a workflow that connects headset type, gender, age, session duration, motion sickness, immersion, and educational access. From there, I built interactive charts that let me filter, compare, and break down patterns that are not obvious when looking at each dataset alone.

The entire visualization is designed around exploration. You can switch between datasets, filter the visuals by gender or headset, and highlight sections to understand exactly how different groups behave in VR. This project is part research, part portfolio work, and part personal curiosity about how VR affects people differently.

---

## Project Overview

This project examines how different groups of people experience virtual reality depending on their demographics, hardware choices, and behavioral tendencies.  
Instead of relying on a single dataset, the analysis synthesizes insights from multiple Kaggle sources covering VR usage, headset adoption, emotional response, consumer behaviors, immersion scores, and accessibility conditions.

The central goal is to understand **what factors predict comfort, discomfort, and overall immersion** in VR systems.  
The project uses both descriptive visualizations and predictive modeling to uncover meaningful patterns that shape VR user experience.

---

## Data
`1`
### 1. Virtual Reality in Education Impact  
Tracks student age, gender, hours per week, engagement level, learning improvements, and instructor proficiency.  
Helps explain how VR functions inside classrooms.

### 2. Modified VR in Education Dataset  
Adds stress levels, access to equipment, and collaboration indicators.  
Useful for comparing educational environments.

### 3. Assistive Technology Dataset  
Global dataset from WHO regions that shows training availability across different assistive technology categories.  
Gives clear geographic context for accessibility gaps.

### 4. VR Experiences Dataset  
Focuses on headset type, session duration, motion sickness, and immersion.  
This dataset is the backbone for the interactive charts.

### 5. Student Math and Portuguese Performance  
Standard demographic and academic data for multiple schools.  
Used for comparisons and additional modeling opportunities.

All data sources came from Kaggle.

The data I propose to visualize for my project is ... found ih the following locations: 
 - https://www.kaggle.com/datasets/lumaatabbaa/vr-eyes-emotions-dataset-vreed
 - https://www.kaggle.com/datasets/yapwh1208/availability-of-education-for-assistive-technology
 - https://www.kaggle.com/datasets/yapwh1208/availability-of-education-for-assistive-technology
 - https://www.kaggle.com/datasets/leetheoiv/steam-virtual-reality-vr-video-games-dataset
 - https://www.kaggle.com/datasets/szhao2020/vr-gaming-network-traffic
 - https://www.kaggle.com/datasets/programmer3/emotion-recognition-in-mobile-vr-films
 - https://www.kaggle.com/datasets/ilokabenneth/augmented-reality-consumer-behaviour-consumer-enga



## Methodology

### Data Cleaning and Integration
I standardized columns like engagement levels, gender labels, and headset names. Then I pulled the datasets together into a shared D3 structure so I could filter them consistently. The most challenging part was dealing with different scales and sample sizes, especially for gender groups with fewer entries.

### Visual Architecture
I used the same filtering logic across all visuals. This keeps user interactions predictable.

The main components include:  
• Scatter plot showing engagement vs hours of usage  
• Radar chart showing immersion, duration, motion sickness, and average age grouped by gender  
• Headset filters that update the visuals instantly  
• Gender filters that change the shape of the radar and scatter plot  
• Hover interactions that highlight sections and dim the rest  
• Icons that sit outside the main chart area for clarity

### Predictive Thinking
While the final project is visualization focused, the structure supports future modeling. Features like gender, duration, age, headset type, and immersion are already aligned for regression work.


## Questions & Tasks

## Key Questions & Findings  
*(Descriptive + Predictive)*

### 1. How do VR headsets differ across demographics, comfort levels, and immersion scores?  
**Finding:**  
PlayStation VR has the largest user base. HTC users tend to have longer sessions and lower motion sickness. Oculus users fall between the two.

---


## Visualizations

### Engagement Scatter Plot  
Shows how VR engagement shifts by device and demographic group. The filters allow you to compare different headsets and see where sickness or comfort trends start forming.

### Radar Chart  
Each gender group is represented with the same four metrics:  
• Average Age  
• Motion Sickness  
• Duration  
• Immersion  

Users can cycle through male, female, and other to see how their profiles shift. Hovering highlights each section with clear tooltips.

### Headset Comparison Panels  
PlayStation VR, HTC, and Oculus each show different comfort and immersion behaviors.  
HTC users have longer sessions.  
PlayStation has the most users.  
Oculus sits in the middle for both duration and sickness.

### Assistive Technology View  
Breaks down global access to technology training by region.  
Regions with higher funding have stronger adoption.  
Regions with limited support show clear gaps.

### Impact and Education Charts  
Links student engagement and VR adoption.  
Shows which groups improve academically when VR is available.

Screenshots of these visuals are included throughout the project.


## Key Findings

### Comfort and Discomfort Patterns  
Younger male users show higher motion sickness.  
Female users stay longer and report smoother experiences.  
Other gender groups show the widest range due to sample size.

### Headset Behavior Differences  
HTC supports longer sessions with lower sickness.  
PlayStation dominates in user count.  
Oculus trends toward balanced outcomes.

### Immersion vs Duration  
Longer sessions raise both immersion and discomfort.  
Frequent users adapt over time.

### Geographic Accessibility  
Assistive technology training is uneven globally.  
Regions with stronger infrastructure support VR adoption more effectively.



### 2. What demographic factors predict comfort or discomfort in VR?  
**Finding:**  
- Younger male users tend to experience more sickness  
- Female users show lower sickness and stay longer in VR  
- Other-gender populations show the greatest variability due to sample size  

Demographics clearly influence comfort outcomes.

---

### 3. What behavioral factors contribute to immersion or discomfort?  
**Finding:**  
- Long sessions increase immersion and discomfort simultaneously  
- Frequent users adapt faster and show lower sickness  
- Multi-device users report the highest comfort and engagement  

Predictive modeling will quantify which factors matter most.

---

### 4. Are there geographic differences in VR or assistive technology adoption?  
**Finding:**  
Countries with higher educational and technological funding show greater adoption. Under-resourced regions lag significantly.

---

### 5. What combinations of factors best predict a positive or negative VR experience?  
**Approach:**  
Using regression or classification models with:  
- Age  
- Gender  
- Headset  
- Session duration  
- Experience level  

Outputs include comfort score, immersion rating, and risk probability.


 * (insert your question or task here) What is the most ocmmon mainstream headset X vary over time?
 * (insert your question or task here) Is there any correlation between Gender?
 * (insert your question or task here) Are there interesting spatial patterns in the data?
 * (insert your question or task here) How many X are there across different Y?
 * (insert your question or task here) Where does the US rank in Assistive Technolgoy?
 * (insert your question or task here) How many schools have adopted VR Usage?
 * (insert your question or task here) What are the risk factors of VR Usage?
 * (insert your question or task here)  Is there any correlation between Model Type?



---
## Sketches

### Risk Factor Tree  
Hierarchy showing: All users → Device → Gender → Comfort Risk.

### Comfort Severity Heatmap  
A grid showing discomfort intensity across headsets, demographics, and behaviors.

### Predictive Model Flow Diagram  
Visualizing relationships between user traits and VR outcomes.

---

## Project Goals

- Identify what makes VR comfortable or uncomfortable  
- Compare major headset demographics and behavioral patterns  
- Understand consumer behavior and its relationship to VR outcomes  
- Develop predictive models for comfort, immersion, and user engagement  
- Produce clear, interpretable visualization prototypes  

---

## Why This Project Matters

VR is rapidly entering entertainment, education, therapy, and accessibility.  
Understanding user comfort and risk factors is critical for:

- broader adoption  
- safer user experiences  
- better hardware design  
- enhanced accessibility  
- informed decision-making by developers and researchers  

These results can influence future VR safety guidelines and consumer experience design.

---


## Prototypes

I’ve created a proof of concept visualization of this data. The visiualiatios range from stater plot, to data trees. 


[![image](https://github.com/fokalview/VR-Data/blob/master/3panel.png)](https://vizhub.com/fokalview/f2e723cc55194e98ab325c524371c4e4)

<div align="center">

### **PlayStation VR**  
### **A 3 Panel Spread of PlayStation VR, HTC, and Oculus**

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/PlaystationVR.png)](https://vizhub.com/fokalview/0cc21ddd8b9c403b856b1dbe925a4ab5)

<div align="center">

### **PlayStation VR**

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/HTC.png)](https://vizhub.com/fokalview/16bb6b65f8894e7383ba5840939508d5)

<div align="center">

### **HTC**

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/oculus.png)](https://vizhub.com/fokalview/02c750bd8dea4c309fd682feb4ce7470)

<div align="center">

### **Oculus**

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/Assitivetech.png)](https://vizhub.com/fokalview/5325ee30f3aa4482bba707138034e637)

<div align="center">

### **Assistive Technology**

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/VRExp.png)](https://vizhub.com/fokalview/0b4d4f422e2f4721b963b242b6388e84)

<div align="center">

### **VR Experience**

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/Immerion%20SCore.png)](https://vizhub.com/fokalview/772e7b2285d643cbaab3892a6d7d9300)

<div align="center">

### **Impact on Score**

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/Engagment.png)](https://vizhub.com/fokalview/634ce52577aa4d509d022628e38526c3)

<div align="center">

### **Engagement**

</div>

---
[Source – 3 Panel Spread](https://vizhub.com/fokalview/f2e723cc55194e98ab325c524371c4e4)

[Source – PlayStation VR](https://vizhub.com/fokalview/0cc21ddd8b9c403b856b1dbe925a4ab5)

[Source – HTC Vive](https://vizhub.com/fokalview/16bb6b65f8894e7383ba5840939508d5)

[Source – Oculus](https://vizhub.com/fokalview/02c750bd8dea4c309fd682feb4ce7470)

[Source – Assistive Tech](https://vizhub.com/fokalview/5325ee30f3aa4482bba707138034e637)

[Source – VR Experience](https://vizhub.com/fokalview/0b4d4f422e2f4721b963b242b6388e84)

[Source – Impact on Score](https://vizhub.com/fokalview/772e7b2285d643cbaab3892a6d7d9300)

[Source – Engagement](https://vizhub.com/fokalview/634ce52577aa4d509d022628e38526c3)


## Open Questions

I am not sure that I am going ot do this correctly but i am going to do my best to try. Here are a few views that i am not sure about: 

https://vizhub.com/fokalview/5e0d145e049d46a9ac27ba580bd3d589
https://vizhub.com/fokalview/c849b29a34cd452abb20fe62bfea0d9d
https://vizhub.com/fokalview/2f7d8ea52aa549028a94af36c2b17d41
https://vizhub.com/fokalview/3c0b21fb8d3e435a9f4dcaadc9b2bf2e



## Milestones

I have made a scatter plot
I was able to finlally import the docutmetns!
I was able to start iterateing the scater pl;ot and data into something abiut more unique and suited toward the data that i have. 

## Key Findings

### Comfort and Discomfort Patterns  
Younger male users show higher motion sickness.  
Female users stay longer and report smoother experiences.  
Other gender groups show the widest range due to sample size.

### Headset Behavior Differences  
HTC supports longer sessions with lower sickness.  
PlayStation dominates in user count.  
Oculus trends toward balanced outcomes.

### Immersion vs Duration  
Longer sessions raise both immersion and discomfort.  
Frequent users adapt over time.

### Geographic Accessibility  
Assistive technology training is uneven globally.  
Regions with stronger infrastructure support VR adoption more effectively.


## Why This Project Matters
VR design needs to be based on how people actually experience it, not how we hope they experience it. This project makes those patterns clear. Developers can use these insights to build safer and more immersive environments. Educators can see how VR affects learning. Policy makers can identify where support is missing.

At the same time, the project shows how multidataset visualizations can tell a bigger story than any single dataset can.


## Future Work

• Build a predictive comfort model using regression  
• Add session frequency to the scatter plot  
• Expand the radar chart to include new variables  
• Develop a full dashboard for VR decision makers  
• Compare VR data with AR datasets  
• Add time series analysis for headset adoption trends  

The architecture is already set up for expansion.


## Project Links

### VizHub Projects  
Insert URLs here

### GitHub Repository  
https://github.com/fokalview/VR-Data


## Conclusion
After combining all these datasets and building out the visuals, the patterns became clear. VR is not a one size fits all experience. Different headsets, demographics, and educational contexts all shape user outcomes.

This project helped me understand those patterns in a structured way and strengthened my skills in D3, JavaScript, data cleaning, and visual architecture. It also proved how interactive data work can reveal insights that static charts never will.

This is version one. There is more I want to build, but the foundation is solid and the insights are real.
