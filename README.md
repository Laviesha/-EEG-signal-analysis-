# -EEG-signal-analysis-
EEG Signal Analysis Documentation of Our Approach
1)Abstract
This study investigates neural oscillatory dynamics across four experimental paradigms—Oddball, Stroop, Task-Switching, and Dual-Task—using electroencephalography (EEG). The analysis aimed to uncover the neural correlates of attention, cognitive control, task flexibility, and divided attention by focusing on specific frequency bands (alpha, theta, beta, and gamma). Data from 24 healthy participants were recorded using an 8-channel EEG system and analysed through preprocessing, spectral filtering, and topographical mapping.
Results revealed significant modulation of neural activity: enhanced alpha suppression and gamma activation during target detection in the Oddball Paradigm, increased theta power during conflict resolution in the Stroop Task, elevated frontal theta activity during task switching, and beta band differences reflecting multitasking costs in the Dual-Task Paradigm. These findings highlight EEG’s capability to capture task-specific neural mechanisms and its potential as a biomarker for cognitive load monitoring and brain-computer interfaces.

2)Introduction
Electroencephalography (EEG) is a non-invasive neuroimaging technique used to record electrical activity in the brain. This report presents the analysis of EEG data collected during four experimental paradigms: the Oddball Paradigm, the Stroop Task, the Task-Switching Paradigm, and the Dual-Task Paradigm. Each task evaluates different cognitive functions, such as attention, cognitive control, and divided attention. By focusing on specific frequency bands (e.g., alpha, theta, beta, and gamma), this report investigates neural oscillatory dynamics and their associations with task-specific processes. The analysis involves preprocessing steps, spectral filtering, statistical evaluations, and topographical visualizations.
3)Explanation of Experimental Paradigms 
3.1 Oddball Paradigm
The Oddball Paradigm assesses focused attention and neural responses to infrequent or target stimuli. Participants press a key when presented with a rare red circle while ignoring frequent blue circles. This task highlights neural markers such as P300 and alpha suppression, reflecting attention and background activity reduction. Gamma oscillations are analysed for their role in sensory processing and cognitive engagement.
3.2 Stroop Task
The Stroop Task measures selective attention and cognitive control. Participants respond when the colour of a displayed word matches its text (e.g., "RED" in red). Conflict between automatic reading and controlled colour identification activates neural markers like N2 (conflict detection) and P300 (attention and decision-making). Theta and alpha band analyses reveal neural mechanisms underlying these processes.
3.3 Task-Switching Paradigm
The Task-Switching Paradigm evaluates cognitive flexibility by alternating between two rules: pressing a key for even numbers and numbers greater than five. This paradigm examines neural correlates of task switching, including theta oscillations (cognitive control) and P3b amplitudes (working memory updates).
3.4 Dual-Task Paradigm
The Dual-Task Paradigm explores divided attention by requiring responses to two concurrent tasks: visual stimuli (red circle) and auditory stimuli (target sound). Beta activity reflects sensorimotor control and task engagement, while P300 amplitudes assess cognitive resource allocation. This paradigm evaluates the cost of multitasking on neural resources.
4)Dataset Details
4.1 Format and Structure
The dataset comprises EEG recordings collected from 24 healthy subjects aged 20 to 50 years, using an 8-channel dry EEG system (Brain Product). Data was sampled at 250 Hz, ensuring sufficient temporal resolution for analysing frequency bands of interest. Each subject's data includes:
Subject Folders: Each subject has a dedicated folder (e.g., Subject_1, Subject_2, ..., Subject_24).
EEG Files: Contain the raw brain signals recorded during the task in .csv format.
Marker Files: Include timestamps for task-specific events (e.g., when a red circle appears).
Paradigms: Oddball, Stroop Task, Task-Switching, and Dual-Task, with each paradigm comprising 100 trials lasting 1 minute each.
4.2 Baseline Recordings
Each subject’s dataset includes baseline recordings:
Eyes Open: Subjects focus on a fixed point for 30 seconds.
Eyes Closed: Subjects maintain a relaxed state with closed eyes for 30 seconds. These baselines serve as reference data for analysing task-related neural activity and for noise normalization.
4.3 EEG Channels
 The EEG was recorded using eight channels: Fp1, Fp2, F3, Fz, F4, Cz, Pz, and Oz. This configuration captures activity from frontal, central, and occipital regions, relevant for studying attention and cognitive control.
4.4 Preprocessing
4.4.1 General Steps
File Loading: EEG and marker files were loaded for each subject. The markers were parsed and synchronized with the EEG timestamps.
Filtering: A bandpass filter (0.02–35 Hz) was applied to remove low-frequency drifts and high-frequency noise. For some tasks, additional filtering was performed to extract specific frequency bands.
Notch Filtering: A notch filter was applied at 50 Hz to remove AC powerline noise during gamma band analysis.
Epoching: Data was segmented into epochs based on event markers for target and non-target stimuli, with a time window of -200 ms to 800 ms relative to stimulus onset.

4.4.2 Oddball Paradigm
Bandpass Filter: Applied between 0.02 Hz and 35 Hz to clean the signal.
Alpha Band Extraction: Filtered the alpha band (8–13 Hz) and plotted topographical maps for target and non-target conditions.
Gamma Band Analysis: Applied a bandpass filter (30–50 Hz) to extract gamma oscillations. FFT plots were generated before and after applying a notch filter (50–100 Hz) to remove AC noise. Topographical maps were plotted for target and non-target conditions using gamma band data.
Epoching: Data was segmented into epochs to analyse event-related responses.
Grand Average: Calculated and plotted grand averages for gamma and alpha bands across all subjects. Statistical differences between target and non-target conditions were evaluated.

4.4.3 Stroop Task
Bandpass Filter: Applied between 0.02 Hz and 35 Hz to clean the raw data.
Alpha and Theta Bands: Extracted alpha (8–13 Hz) and theta (4–8 Hz) bands for analysis. Topographical maps were generated for both bands comparing target and non-target conditions.
Epoching: Data was segmented into epochs to analyse target and non-target responses.
Grand Average: Calculated and plotted grand averages for alpha and theta bands across all subjects. Statistical differences between target and non-target conditions were evaluated.
4.4.4 Task-Switching Paradigm
Bandpass Filter: Applied between 0.02 Hz and 35 Hz to clean the raw data.
Theta Band Extraction: Filtered the theta band (4–8 Hz) and plotted topographical maps for target and non-target conditions.
Epoching: Data was segmented into epochs to compare event-related responses.
Grand Average: Calculated and plotted grand averages for the theta band across all subjects. Statistical differences between target and non-target conditions were evaluated.
4.4.5 Dual-Task Paradigm
Bandpass Filter: Applied between 0.02 Hz and 35 Hz to clean the raw data.
Beta Band Analysis: Extracted beta band (13–30 Hz) data and plotted topographical maps for target and non-target conditions. Specific markers for different subjects were considered to handle marker inconsistencies.
Epoching: Data was segmented into epochs for analysing beta activity in target and non-target conditions.
Grand Average: Calculated and plotted grand averages for beta band activity across all subjects. Statistical differences between target and non-target conditions were evaluated.
5)Methodology
5.1 Oddball Paradigm
Event-Related Potential (ERP) Analysis:
Epochs were averaged to extract the P300 component for target and non-target conditions.
Alpha suppression and gamma oscillations were analyzed for their roles in attention and sensory processing.
Topographical Mapping:
Topographical maps for alpha and gamma bands were plotted for each subject.
Grand averages for all subjects were calculated, and statistical differences between target and non-target conditions were evaluated using paired t-tests.
5.2 Stroop Task
Event-Related Analysis:
Epochs were analysed to study N2 and P300 components for congruent and incongruent conditions.
Theta and alpha oscillations were compared across conditions.
Statistical Analysis:
Grand averages for alpha and theta bands were computed.
Paired t-tests assessed statistical differences between conditions.
5.3 Task-Switching Paradigm
Theta Band Analysis:
Epochs were averaged to extract theta oscillations linked to cognitive control.
Topographical maps were generated for target and non-target conditions.
Grand Averages and Statistics:
Grand averages for theta band activity were plotted.
Statistical tests compared target and non-target conditions across all subjects.
5.4 Dual-Task Paradigm
Beta Band Analysis:
Topographical maps for beta activity were plotted for target and non-target conditions.
Marker-specific analyses accounted for differences across subjects.
Grand Averages and Statistics:
Grand averages were calculated for beta band activity.
Statistical comparisons highlighted the effects of multitasking on neural resources.
6)Result
6.1 Oddball Paradigm
a) Alpha Band(8-13Hz) Topo-Plot:
The analysis of alpha band activity (8–13 Hz) for the oddball paradigm shows distinct topographical differences between target and non-target conditions, with additional insights from the statistical difference plot.
 Active Regions: The parietal and occipital regions exhibit the highest activity, indicated by purple and blue hues. These regions show suppressed alpha activity, which is typically associated with increased cognitive and sensory engagement during target stimulus processing.
Cognitive Interpretation: The suppression of alpha oscillations reflects heightened attention and neural processing associated with target recognition in the Oddball Paradigm.
Non-Target Condition:
Active Regions: In the non-target condition, the frontal and occipital regions display comparatively higher activity (yellow to light green areas), indicating reduced alpha suppression.
Cognitive Interpretation: This pattern reflects lesser cognitive engagement and sensory processing during frequent, non-salient non-target stimuli.
Statistical Differences (p < 0.05):
Top-Central Region (Light Blue): Indicates less alpha suppression for non-target stimuli compared to targets.
Bottom Region (Light Red): Suggests stronger alpha suppression for target stimuli, indicating a significant increase in neural engagement for target recognition.
Comparison:
The target condition is characterized by stronger alpha suppression, primarily in parietal and occipital regions, which corresponds to heightened cognitive activity.
The non-target condition exhibits higher overall alpha activity, indicating a less engaged neural state.
Statistical differences validate these observations, showing significant suppression of alpha oscillations in target-related regions compared to non-targets.
Plots:  

b) Gamma Band (30–50 Hz) Topo-Plot:
The analysis of gamma band activity (30–50 Hz) for the oddball paradigm highlights distinct topographical differences between target and non-target conditions, as well as significant statistical differences.
Target Condition:
Active Regions: The frontal and central regions display the strongest gamma activity, as evidenced by the prominent yellow/green areas.
Cognitive Interpretation: This heightened gamma power reflects increased attention and cognitive engagement during target stimulus processing. It is likely associated with sensory processing, decision-making, and motor preparation, typical of the Oddball Paradigm.
Non-Target Condition:
Active Regions: Gamma activity in the bottom-central regions is more pronounced compared to other areas, while the frontal and central regions show reduced activity.
Cognitive Interpretation: This reduced gamma synchronization aligns with habituation or decreased neural engagement when processing frequent and less significant non-target stimuli.
Statistical Differences (p < 0.05):
Frontal Regions (Red Areas): Significantly higher gamma activation is observed for targets compared to non-targets, suggesting enhanced attentional focus and cognitive processing during target trials.
Parietal Regions (Blue Areas): Reduced gamma activity for non-target stimuli reflects suppression or habituation to repetitive stimuli.
Comparison:
The target condition shows a concentrated and stronger gamma response in the frontal and central regions, while the non-target condition demonstrates relatively lower and more distributed activity, with prominent suppression in parietal regions.
Statistical differences validate that the observed activation patterns between target and non-target stimuli are significant and align with the expected neural responses in the Oddball Paradigm.
Plots:  
6.2 Stroop-Task
a) Theta Band(4-8Hz) Topo-Plot:
Target (Congruent):
The grand average topographic map for the congruent condition reveals theta band (4–8 Hz) activity predominantly localized in the midline frontal and central scalp regions. This pattern suggests engagement of attentional and executive networks typically involved in processing less cognitively demanding congruent trials.
Non-Target (Incongruent):
The grand average topographic map for the incongruent condition demonstrates theta band activity with a similar distribution across the frontal and central regions. However, the magnitude of activity appears enhanced compared to the congruent condition, reflecting the additional cognitive effort required for conflict resolution during incongruent trials.
Statistical Difference (p < 0.05):
The statistical topographic map highlights significant differences in theta band power between the two conditions. Red regions indicate higher activity in the incongruent condition, while blue regions signify greater activity in the congruent condition. These differences are most pronounced in the frontal and central regions, aligning with areas associated with cognitive control and conflict monitoring.
Comparison:
Comparing the congruent and incongruent conditions, the results suggest that the incongruent condition elicits higher theta band activity, particularly in frontal-central areas. This supports the hypothesis that the incongruent condition demands greater cognitive control mechanisms, as reflected by enhanced theta power. The significant statistical differences underscore the robust neural response to task difficulty.
Plots:  
b) Alpha Band(8-13Hz) Topo-Plot:
Target (Congruent):
The grand average topographic map for the congruent condition shows alpha band (8–13 Hz) activity predominantly over posterior scalp regions. This pattern is characteristic of decreased task-related alpha suppression, indicating a relaxed but attentive state during congruent trials that require less cognitive load.
Non-Target (Incongruent):
The grand average topographic map for the incongruent condition displays similar posterior alpha band activity, but with noticeable differences in magnitude and spatial distribution. Enhanced alpha desynchronization is evident, reflecting greater neural engagement and cognitive control required to process incongruent trials.
Statistical Difference (p < 0.05):
The statistical topographic map reveals significant differences in alpha band power between congruent and incongruent conditions. Blue regions indicate higher alpha activity in the congruent condition, while red regions signify greater alpha suppression in the incongruent condition. These differences are prominent in posterior and parietal regions, consistent with areas involved in visual processing and attentional reallocation.
Comparison:
Comparing the congruent and incongruent conditions, the results suggest that incongruent trials elicit stronger alpha suppression, indicative of increased cognitive demands and conflict resolution mechanisms. The significant statistical differences underscore the modulation of alpha band activity as a function of task difficulty.
Plots:  
6.3 Task-Switching Paradigm
a)Theta Band(4-8Hz) Topo-Plot:
Target:
The grand average topographic map for the target condition in the task-switching paradigm highlights theta band (4–8 Hz) activity prominently in frontal and midline regions. This elevated frontal theta activity is associated with cognitive control and task monitoring processes, which are critical during target detection and execution.
Non-Target:
The grand average topographic map for the non-target condition shows a similar spatial distribution of theta band activity but with reduced intensity compared to the target condition. This reflects lesser cognitive engagement and control demands in non-target trials, where task-switching and attentional reallocation are less prominent.
Statistical Difference (p < 0.05):
The statistical topographic map reveals significant differences in theta band power between target and non-target conditions. Red regions indicate higher theta power in the target condition, particularly in frontal and midline regions, while blue areas signify stronger theta activity in non-target trials. These statistical differences emphasize the task-specific modulation of theta band activity.
Comparison:
Comparing target and non-target conditions, the results indicate that target trials elicit greater frontal theta power, aligning with the increased cognitive load, executive control, and task-switching demands required for effective target processing. The observed statistical differences validate the neural distinctions between task types within the theta band.
Plots:  
6.4 Dual-Task Paradigm
a)Beta Band(13-30Hz) Topo-Plot:
Markers considered: Subject-specific markers for Subject 1, 4, 8, 16, 21, 24. Events include timestamped paradigms, target (Red Circle), and non-target (Blue Circle) trials with associated responses.
Target:
The grand average topographic map for the target condition in the dual-task paradigm highlights beta band (13–30 Hz) activity. Strong activity is observed in the central and parietal regions, reflecting the engagement of sensorimotor and attentional networks during target identification and response.
Non-Target:
The grand average topographic map for the non-target condition shows a similar spatial pattern but with notably reduced beta band power compared to the target condition. This reduced activity is consistent with less cognitive engagement during non-target processing.
Statistical Difference (p < 0.05):
The statistical difference map reveals significant differences between target and non-target conditions in the beta band. Red areas indicate increased beta activity for target trials, particularly in central-parietal regions, while blue areas highlight greater non-target beta activity, possibly due to task-switching or preparatory mechanisms.
Comparison:
The beta band results demonstrate clear modulation by task type, with enhanced activity during target trials indicating higher cognitive and motor engagement. Non-target trials elicit comparatively lower beta power, reflecting reduced task relevance and cognitive load. Statistical differences validate these patterns, emphasizing the role of beta oscillations in dual-task processing.
Plots:  
Markers considered: Subject-specific markers for Subject 2, 3, 5, ... 23. Events include timestamped paradigms, visual target (Red Circle), visual non-target (Blue Circle), audio target (Sound), and audio non-target (Sound) trials.
Visual Target: 
Observed strong activation in the central and occipital regions of the scalp, as evident in the topo-plot for "Visual Target."
Visual Non-Target: 
Subtle activations primarily in the central regions, with a weaker distribution compared to the target response.  
Visual Statistical Difference: 
Significant differences observed in the central-parietal areas when comparing targets and non-targets. 
Key regions: Increased responses in occipital and parietal regions for targets.  
Audio Target:
Activation primarily focused in the temporal areas, reflecting auditory stimulus processing.  
Audio Non-Target:
Minimal activation in temporal areas, reflecting lower engagement compared to target auditory tasks. 
Audio Statistical Difference:
Clear differences observed between targets and non-targets in the temporal-parietal regions, showing stronger activations for auditory targets.
Comparison:
1.Visual vs Audio Tasks
Visual Targets induced broader scalp-wide activations compared to Audio Targets, which were more focused in the temporal regions.  
Non-target responses were generally weaker in both modalities, but the visual non-targets showed a wider spatial distribution compared to audio non-targets.
2. Statistical Differences
Visual tasks showed larger differences in the occipital-parietal regions.  
Audio tasks had more focused differences in temporal areas.  
Plots:  
7)Discussion
The study provided valuable insights into the neural mechanisms underpinning cognitive processes across various tasks. By focusing on frequency bands, the results aligned with existing literature, reaffirming the roles of:
Alpha Oscillations: Suppression during attention-demanding tasks, reflecting neural disengagement from background activity.
Theta Oscillations: Prominent in tasks requiring conflict resolution and cognitive flexibility, indicating engagement of executive control networks.
Beta Oscillations: Modulated by sensorimotor and attentional processes, particularly during multitasking scenarios.
Gamma Oscillations: Associated with sensory processing and decision-making, especially in tasks involving target detection.
The statistical analyses and topographical visualizations highlighted region-specific neural activations, such as heightened frontal theta activity during task switching and increased occipital gamma power during visual processing. These findings demonstrate the specificity of EEG as a tool for understanding cognitive functions and its potential to act as a biomarker for mental workload and performance.

8)Conclusion
The analysis of EEG data across the four experimental paradigms—Oddball Paradigm, Stroop Task, Task-Switching Paradigm, and Dual-Task Paradigm—has provided critical insights into the neural mechanisms underlying attention, cognitive control, task switching, and multitasking.
The topographical analyses and statistical evaluations across frequency bands revealed distinct neural dynamics specific to each paradigm. Key findings include the modulation of alpha and gamma oscillations during target detection in the Oddball Paradigm, enhanced theta activity reflecting conflict resolution in the Stroop Task, task-switching demands evident in frontal theta power, and beta oscillatory differences highlighting multitasking costs in the Dual-Task Paradigm.
These results underscore the ability of EEG to capture task-specific neural activity and offer valuable implications for understanding cognitive processes. They also demonstrate the potential for EEG-based biomarkers in applications such as cognitive load monitoring, neurofeedback, and brain-computer interfaces. 
9)References
L. A. Farwell and E. Donchin, "Talking off the top of your head: Toward a mental prosthesis utilizing event-related brain potentials," Electroencephalography and Clinical Neurophysiology, vol. 70, no. 6, pp. 510–523, 1988.


Student Name: Lavisha Kapoor
Professor Name: Dr. Tharun Kumar Reddy Bollu 









 



 





















