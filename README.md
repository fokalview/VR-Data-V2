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

This project examines how different groups of people experience virtual reality depending on their demographics, hardware choices, and behavioral tendencies. Instead of relying on a single dataset, the analysis synthesizes insights from multiple Kaggle sources covering VR usage, headset adoption, emotional response, consumer behaviors, immersion scores, and accessibility conditions.

The central goal is to understand what factors predict comfort, discomfort, and overall immersion in VR systems. The project uses descriptive visualizations and a structure that can support predictive modeling in later versions to uncover meaningful patterns that shape VR user experience.

---

## Headsets Tracked

The core VR experience dataset focuses on three mainstream headsets:

1. **PlayStation VR**  
2. **HTC Vive**  
3. **Oculus Rift**

These three devices appear consistently in the tree views, headset comparison panels, and radar based visuals.

---

## Research Questions

This project is guided by a set of practical questions:

1. How do the three headsets differ in user demographics, comfort, and immersion?  
2. Do age or gender influence motion sickness, immersion, or session duration?  
3. What behavioral factors like duration or usage patterns shape comfort and immersion?  
4. Are there geographic differences in assistive technology training and access?  
5. Which features best predict a positive or negative VR experience if we move into modeling?  
6. Which headset type appears most often in the dataset?  
7. Are there meaningful gender based differences in VR outcomes?  
8. Are there noticeable spatial or regional patterns when comparing datasets?  
9. How do user counts shift across demographic categories such as age group or education level?  
10. How does the United States compare to other regions in assistive technology access?  
11. How many students in the education datasets actively use VR in education?  
12. What patterns point to higher discomfort or risk in VR use?  
13. Does headset model correlate with comfort, immersion, or session duration?

The visualizations and interactions in this project are designed to make these questions easier to explore.

---

## Data

### Core Project Datasets

These are the main datasets that drive the current visualizations:

1. **Virtual_Reality_in_Education_Impact.csv**  
   Student level VR usage and outcome data.  
   - Student_ID  
   - Age  
   - Gender  
   - EducationLevel / Grade_Level  
   - Usage_of_VR_in_Education (Yes/No)  
   - Hours_of_VR_Usage_Per_Week  
   - Engagement_Level (1 to 5)  
   - Improvement_in_Learning_Outcomes (Yes/No)  
   - Instructor_VR_Proficiency  
   - Region  

2. **Modified_Virtual_Reality_in_Education_Dataset.csv**  
   Education context and VR implementation details.  
   - Age  
   - EducationLevel  
   - Usage_of_VR_in_Education  
   - Hours_of_VR_Usage_Per_Week  
   - Engagement_Level  
   - Improvement_in_Learning_Outcomes  
   - Instructor_VR_Proficiency  
   - Access_to_VR_Equipment  
   - Stress_Level_with_VR_Usage  
   - Collab (collaboration indicator)  

3. **Assistive technology.csv**  
   Global assistive technology training availability.  
   - ParentLocation (region)  
   - Location (country)  
   - Dim1 (training category)  
   - Period (year)  
   - Value (availability indicator)  

4. **Virtual Reality Experiences.csv**  
   User experience metrics for the three VR headsets.  
   - UserID  
   - Age  
   - Gender (Male, Female, Other)  
   - VRHeadset (PlayStation VR, HTC Vive, Oculus Rift)  
   - Duration (minutes)  
   - MotionSickness (1 to 10)  
   - ImmersionLevel (1 to 5)  

5. **Student math and Portuguese datasets**  
   Standard student demographic and academic performance for comparison.  
   - student_id  
   - sex  
   - age  
   - family and study context  
   - failures and scores  

These datasets are the ones directly used in the views that ship with this project.

### Additional Reference Datasets Considered

The project also draws on ideas from other Kaggle datasets, even if not all of them are wired into the current version:

- https://www.kaggle.com/datasets/lumaatabbaa/vr-eyes-emotions-dataset-vreed  
- https://www.kaggle.com/datasets/yapwh1208/availability-of-education-for-assistive-technology  
- https://www.kaggle.com/datasets/leetheoiv/steam-virtual-reality-vr-video-games-dataset  
- https://www.kaggle.com/datasets/szhao2020/vr-gaming-network-traffic  
- https://www.kaggle.com/datasets/programmer3/emotion-recognition-in-mobile-vr-films  
- https://www.kaggle.com/datasets/ilokabenneth/augmented-reality-consumer-behaviour-consumer-enga  

All datasets are sourced from Kaggle.

---

## Methodology

### Data Cleaning and Integration

I standardized columns like engagement level, gender labels, and headset names so the datasets could be combined or compared without confusion. I converted numeric fields where needed, handled Yes/No flags, and aligned scales for hours, engagement, and immersion.

Once the data was cleaned, I pulled it into a shared D3 based structure so filters and interactions could work the same way across multiple views. The main challenge was dealing with different sample sizes, especially for the "Other" gender group and for regions with fewer assistive technology records.

### Visual Architecture

I used the same filtering logic across all visuals so user interactions feel consistent. The main components include:

- Scatter plots showing engagement versus hours of VR usage  
- Grouped bar charts to show user distribution across age and education levels  
- Radar charts showing immersion, duration, motion sickness, and average age grouped by gender  
- Headset filters that update the visuals instantly  
- Gender filters that change the shape of the radar and scatter plots  
- Hover interactions that highlight specific elements and dim the rest  
- Icons and legends that sit in clear whitespace outside the main chart area

The visual system is intentionally modular so it can be extended or reused with new datasets.

### Predictive Thinking

While the final project is visualization focused, the structure is ready for future modeling. Features like gender, duration, age, headset type, engagement, and immersion are aligned so they can feed into regression or classification models that predict comfort or risk levels.

---

## Visualizations

### Engagement View

An interactive scatter plot that analyzes the relationship between engagement level and weekly VR usage hours.

- X-axis: Engagement Level (1 to 5)  
- Y-axis: Hours of VR Usage Per Week  
- Color: Dataset source (Impact vs Modified Education)  
- Fill: VR users vs non-users  
- Interactions:  
  - Toggle datasets on and off  
  - Option to show only VR users  
  - Hover tooltips with detailed student level information  

This view connects directly to questions about how usage relates to engagement and which groups cluster at certain engagement levels.

---

### Users View

A grouped bar chart that visualizes user distribution across age ranges and education levels.

- X-axis: Age groups in 5 year bands  
- Y-axis: Count of users  
- Color: Education level (High School, Undergraduate, Postgraduate)  
- Interactions:  
  - Filter by education level  
  - Hover to display exact counts  
  - Compare bars within each age group  

This supports questions about how user demographics shift as age and education level change.

---

### Headset Comparison Panels

A three panel spread for the three tracked headsets:

1. PlayStation VR  
2. HTC Vive  
3. Oculus Rift  

Each panel shows how users of that headset differ by:

- Motion sickness  
- Immersion level  
- Session duration  
- Demographic patterns  

The trees and supporting visuals make it easier to compare comfort and usage across headsets without losing context.

---

### Radar Chart

A radar chart that compares average metrics by gender:

- Metrics: Average Age, Motion Sickness, Duration, Immersion  
- Genders: Male, Female, Other  

Interactions:

- Toggle gender categories on or off  
- Hover on each point to see metric name and exact value  
- Hover near the center to show a summary across all visible genders  

This plays directly into questions about demographic differences and how various groups experience VR.

---

### Assistive Technology View

A view built from the assistive technology dataset that focuses on regional access and training availability.

- Displays which regions and countries report available training for different assistive technology categories  
- Highlights gaps and uneven distribution across regions  
- Helps answer questions about geographic patterns and equity in access

---

### Impact and Education Charts

This set of visuals ties VR adoption to improvements in learning outcomes:

- Compares VR users and non-users on engagement and outcomes  
- Looks at patterns by education level and region  
- Shows which combinations appear to benefit most from VR usage  

---

## Key Findings

### Comfort and Discomfort Patterns

- Younger male users show higher motion sickness.  
- Female users tend to stay longer in VR and report smoother experiences.  
- Other gender groups show the widest range in values, which is partly due to smaller sample size.  

These patterns suggest that comfort is not evenly distributed across demographic groups.

---

### Headset Behavior Differences

- HTC Vive supports longer sessions with lower average sickness.  
- PlayStation VR has the largest user count in the dataset.  
- Oculus Rift tends to sit in the middle for both duration and sickness.  

This answers the question of how headsets differ in comfort and usage behavior.

---

### Immersion vs Duration

- Longer sessions raise both immersion and discomfort at the same time.  
- Frequent users appear to adapt more quickly and report lower sickness over time.  

This supports the idea that behavior and exposure patterns shape how comfortable VR feels.

---

### Geographic Accessibility

- Assistive technology training is uneven globally.  
- Regions with stronger infrastructure and funding report more consistent training availability.  
- Under resourced regions show clear gaps in access.  

This connects directly to the questions about spatial patterns and how different regions compare, including the United States.

---

### Summary of Question Coverage

- Headset differences, gender impact, and behavioral factors are covered in the VR Experience and tree based visuals.  
- Geographic and regional questions are covered through the assistive technology view.  
- Student adoption and engagement are explored in the education based scatter plots and bar charts.  
- Risk factors are inferred from combinations of age, duration, sickness, and headset type, with modeling left as future work.

---

## Sketches

Before building the final visuals, I sketched out several structures.

### Risk Factor Tree

A hierarchy that shows:

- All users  
- Device  
- Gender  
- Comfort risk level  

This helped shape the tree layout used in the VR Experience views.

### Comfort Severity Heatmap

A grid concept where rows represented headsets and columns represented demographics or behaviors. Each cell encoded average discomfort. This idea informed the way I think about combining metrics, even if the final design moved toward trees and radar charts.

### Predictive Model Flow Diagram

A simple flow from input features:

- Age  
- Gender  
- Headset  
- Session duration  
- Experience level  

Into outputs such as:

- Comfort score  
- Immersion rating  
- Risk probability  

This is not fully implemented yet, but the diagram guided how I structured the data.

---

## Project Goals

- Identify what makes VR comfortable or uncomfortable  
- Compare major headset demographics and behavioral patterns  
- Understand consumer and student behavior and how it relates to VR outcomes  
- Prepare the data and structure for predictive models of comfort, immersion, and engagement  
- Produce clear, interpretable visualization prototypes that support exploration and decision making  

---

## Why This Project Matters

VR is rapidly entering entertainment, education, therapy, and accessibility spaces. Understanding user comfort and risk factors is not optional if we care about long term adoption.

This project matters because it:

- Surfaces hidden patterns in how different people experience VR  
- Helps developers think about comfort and risk in a structured way  
- Gives educators insight into which groups benefit most from VR  
- Highlights geographic and accessibility gaps that need attention  

At the same time, the project shows how multidataset visualizations can tell a bigger story than any single dataset on its own.

---

## Prototypes

I have created a set of proof of concept visualizations for this data. These range from scatter plots to hierarchical trees and radar charts.

[![image](https://github.com/fokalview/VR-Data/blob/master/3panel.png)](https://vizhub.com/fokalview/f2e723cc55194e98ab325c524371c4e4)

<div align="center">

### PlayStation VR, HTC Vive, and Oculus Rift 3 Panel Spread

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/PlaystationVR.png)](https://vizhub.com/fokalview/0cc21ddd8b9c403b856b1dbe925a4ab5)

<div align="center">

### PlayStation VR

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/HTC.png)](https://vizhub.com/fokalview/16bb6b65f8894e7383ba5840939508d5)

<div align="center">

### HTC Vive

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/oculus.png)](https://vizhub.com/fokalview/02c750bd8dea4c309fd682feb4ce7470)

<div align="center">

### Oculus Rift

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/Assitivetech.png)](https://vizhub.com/fokalview/5325ee30f3aa4482bba707138034e637)

<div align="center">

### Assistive Technology

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/VRExp.png)](https://vizhub.com/fokalview/0b4d4f422e2f4721b963b242b6388e84)

<div align="center">

### VR Experience

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/Immerion%20SCore.png)](https://vizhub.com/fokalview/772e7b2285d643cbaab3892a6d7d9300)

<div align="center">

### Impact on Score

</div>

---

[![image](https://github.com/fokalview/VR-Data/blob/master/Engagment.png)](https://vizhub.com/fokalview/634ce52577aa4d509d022628e38526c3)

<div align="center">

### Engagement

</div>

---

**Sources**

- [Source – 3 Panel Spread](https://vizhub.com/fokalview/f2e723cc55194e98ab325c524371c4e4)  
- [Source – PlayStation VR](https://vizhub.com/fokalview/0cc21ddd8b9c403b856b1dbe925a4ab5)  
- [Source – HTC Vive](https://vizhub.com/fokalview/16bb6b65f8894e7383ba5840939508d5)  
- [Source – Oculus](https://vizhub.com/fokalview/02c750bd8dea4c309fd682feb4ce7470)  
- [Source – Assistive Tech](https://vizhub.com/fokalview/5325ee30f3aa4482bba707138034e637)  
- [Source – VR Experience](https://vizhub.com/fokalview/0b4d4f422e2f4721b963b242b6388e84)  
- [Source – Impact on Score](https://vizhub.com/fokalview/772e7b2285d643cbaab3892a6d7d9300)  
- [Source – Engagement](https://vizhub.com/fokalview/634ce52577aa4d509d022628e38526c3)  

---

## Open Questions

There are still a few views and ideas that I am experimenting with. Some of these may become part of a future version of the project.

- https://vizhub.com/fokalview/5e0d145e049d46a9ac27ba580bd3d589  
- https://vizhub.com/fokalview/c849b29a34cd452abb20fe62bfea0d9d  
- https://vizhub.com/fokalview/2f7d8ea52aa549028a94af36c2b17d41  
- https://vizhub.com/fokalview/3c0b21fb8d3e435a9f4dcaadc9b2bf2e  

These represent alternate ways to encode similar information or early tests of new ideas.

---

## Milestones

- Built the first scatter plot visual.  
- Successfully imported and cleaned multiple CSV documents.  
- Iterated the scatter plot into a more meaningful layout tied directly to engagement.  
- Designed and implemented the three headset comparison views.  
- Added the radar chart and connected it to gender and headset filters.  
- Integrated the assistive technology view for regional context.

---

## Why This Project Matters

VR design needs to be based on how people actually experience it, not how we hope they experience it. This project makes those patterns clearer and more visual. Developers can use these insights to build safer and more immersive environments. Educators can see how VR affects learning. Policy makers can identify where support is missing and how access is distributed.

At the same time, this project shows how multidataset visualizations can tell a bigger and more honest story than any single dataset can.

---

## Future Work

- Build a predictive comfort model using regression or classification.  
- Add session frequency and experience level into the main views.  
- Expand the radar chart to include more variables such as stress or familiarity.  
- Develop a full dashboard that combines all views into one interface for decision makers.  
- Compare VR data with AR datasets for a more complete picture.  
- Add time based analysis where datasets support it, especially for adoption trends.  

The architecture is already set up for expansion. The next step is deeper modeling and more refined interaction design.

---

## Project Links

### VizHub Projects  

Replace with your final list of URLs or keep the links listed above in the Prototypes and Open Questions sections.

### GitHub Repository  

https://github.com/fokalview/VR-Data

---

## Conclusion

After combining all these datasets and building out the visuals, the patterns became clear. VR is not a one size fits all experience. Different headsets, demographics, and educational contexts all shape how people feel in virtual environments.

This project helped me understand those patterns in a structured way and strengthened my skills in D3, JavaScript, data cleaning, and visual architecture. It also proved that interactive data work can reveal insights that static charts will always miss.

This is version one. There is more I want to build, but the foundation is solid and the insights are real.
