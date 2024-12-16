---
layout: simple
title: Submission / HTML Format
description: This is the submission
---

### Abstract
An emerging space in interface research is wearable devices that closely couple their sensing and actuation abilities. A well-known example is MetaLimbs \cite{metalimbs}, where sensed movements of the foot are directly mapped to the actuation of supernumerary robotic limbs. These systems are different from wearables focused on sensing, such as fitness trackers, or wearables focused on actuation, such as VR headsets. They are characterized by tight coupling between the user's action and the resulting digital feedback from the device, in time, space, and mode. The properties of this coupling are critical for the user's experience, including the user's sense of agency, body ownership, and experience of the surrounding world. Understanding such systems is an open challenge, which requires knowledge not only of computer science and HCI, but also Psychology, Physiology, Design, Engineering, Cognitive Neuroscience, and Control Theory. This workshop aims to foster discussion between these diverse disciplines and to identify links and synergies in their work, ultimately developing a common understanding of future research directions for systems that intrinsically couple sensing and action.

# 1. Background
Wearable technology is maturing at an accelerated pace due to technological advances such as further miniaturization of electrical components and developments of soft electrically functional materials. With less effort required for understanding \textit{how} to build wearable technologies, we are witnessing a shift towards exploring \textit{what} opportunities arise from having technology so conveniently close to the body.


Currently, most wearables focus on a specific functions. They can be roughly be classified as either sensing devices, such as fitness trackers which sample information \textit{from} the user, or as actuation or display devices, such as a wristwatch or other wearable displays, which provide information \textit{to} the user. Many devices, such as smartwatches, combine sensing and actuating mechanisms. However, even in these devices, the actuation and sensing modalities are decoupled in time (e.g., there is a delay between input and output), location (e.g., input and output are not co-located), or mode (e.g., touch input vs. visual output). 

In contrast, an emerging research direction is the design of wearable systems in which \textit{sensing and actuation are closely coupled}. In other words, sensing and actuation are synchronous, co-located, of the same mode, and with a temporal behavior enabling integration with the user's sensory and motor abilities. A striking example is MetaLimbs, a wearable system that provides users with an additional pair of arms \cite{metalimbs}. Here, the user's foot movement is sensed in real-time and directly mapped to the movements of the robotic arm. Sensing and actuation are coupled and cannot be separated without removing the function of the system. Such systems have been used to provide augmented haptic realities \cite{bARefoot, pulseTrains, vARitouch}, change our perception of our bodies \cite{As_Light_as, arm_dimensions, Soniband, BodyTransformation, MotionlessMovement}, or influence the perceived agency over our actions \cite{preemptive, footPedals}. The trend towards such systems is both driven by technological opportunity and by an increasingly sophisticated understanding of the sensorimotor processes underlying our daily experiences.

## 1.1 Coupling of Sensing and Actuation
With respect to technological opportunity, one can see a clear trajectory in wearables research starting in the 90s and persisting to this day. Early explorations of wearable systems in HCI focused largely on designing input mechanisms; well-known examples are the soft devices by Orth et al. \cite{Orth_fabric_computing, musical_jacket}. This was followed by explorations of actuators and output devices, such as the actuated fashion by Berzowska et al. \cite{berzowska_skoprions}. When sensing and actuation came together, this typically was done in wearable systems which closely mirrored the functions of traditional desktop computing and enabled input and output pairings for devices such as handheld keyboards or heads-up displays \cite{Starner_lookingglass, twiddler_lyons}. In all these cases, input and output, sensing and actuation, are clearly distinct.

We are currently, however, witnessing a blurring of these distinctions as designers turn their focus toward materiality, the human body, and the human experience. A simple example of coupling sensing and actuation is the Snap-Snap T-Shirt \cite{snap_tshirt}. In this work, magnetic elements snap together or disconnect based on the wearer's movements. This provides the wearer feedback on their pose. There is no discrete sensing, or actuation mechanism. Rather, both mechanisms are combined in a singel device: magnetic snaps. More complex examples of such bidirectional systems include combined sensing and actuation devices, such as MagnetIO \cite{magnetio} and HapSense \cite{hapsense} which take advantage of the properties of magnetic silicone and electroactive polymers, respectively. 



While these examples merge sensing and actuation in a closed loop technological system, other approaches integrate human as a central element of such a closed loop system. For example, Monarch by Hartman et al. \cite{Hartman:monarchwings} enables control over robotic wings. In this system, flexing of the biceps is mapped to the movement of wearable "wings", providing an intuitive control scheme that becomes close to second nature for the wearer. Electromyography (EMG) for sensing and electrical muscle stimulation (EMS) for actuation, enable systems such as Proprioceptive Interaction \cite{propioceptiveIO}, which overlap between the digital system and the human body, as sensing and actuation both happen through the same human limb. Similarly, systems like Stereo-Smell \cite{stereo-smell} and Augmented Breathing \cite{augmented-breathing} place breath sensors and actuators (electrotactile or thermal) within the nose, synchronizing respiration with altered breath perception.



Moving beyond discrete mappings, we also find a breadth of continuous mappings such as in MetaLimbs \cite{metalimbs}. For the control of MetaLimbs, Sasaki et al. provide continuous coupling between movements of the feet and of the corresponding supernumerary limbs. This tight coupling supports creating new sensorimotor contingencies, enabling us to not only control the supernumerary limbs but also experience agency over the actions of the robotic system. Such systems might also electrically integrate with the body. Reed et al. designed wearables for sonified EMG in closed-loop interaction, providing vocalists with information about their conscious and unconscious movements while singing \cite{Reed:sEMGVocalists}. This coupling allowed for the examination of embodied techniques and control dynamics between human intention and physiological action. In a similar vein, Ley-Flores et al. designed a wearable device called SoniBand, which sonifies body movement using material metaphors \cite{Soniband}. The aim was to link sounds (e.g., water) to body perceptions (e.g., feeling fluid and moving faster) and study the effects on body perception, movement, and emotion. This work explored the potential of materials to facilitate body transformation experiences and support health and behavior change, as also discussed in a recent related CHI workshop on material-enabled, body-based multisensory experiences \cite{tajadura2024body}.

The common denominator of these technological trends is that they support creating both (1) closed-loop interaction systems and (2) interactive systems where the time between sensing user action and providing corresponding output is shorter than our conscious perception (i.e., within microseconds).

## 1.2 Sensorimotor Loops and Micro-Timescales
While there is a technological trend toward coupling sensors and actuators, a parallel shift in our understanding of perceptive processes highlights the importance of these couplings. This is more evident when considering the unit of analysis in HCI. According to Newell \cite{Newell1994}, human behavior unfolds across multiple time scales, which he categorizes into four bands: biological, cognitive, rational, and social (see \autoref{fig:sensint}). In his seminal CHI textbook, published in 2012, Scott MacKenzie uses these bands to describe the domain of HCI \cite{MacKenzie2012}. Reflecting on his description offers a clear picture of how considerations of the temporal dimension in HCI have evolved over the past ten years.

Ten years ago, MacKenzie argued that "traditional" HCI research is focused on analyzing interaction at the level of \textit{deliberate acts}, to the design of specific \textit{tasks}. This included examining issues ranging from the time required to move a cursor between targets, as in a typical Fitts' Law experiment \cite{fitts_2d}, to designing workflows that enable users to complete meaningful tasks. MacKenzie also noted that by 2012, contemporary HCI had broadened its scope to consider the context of these interactions, including social interactions that might develop over weeks, months, or even years \cite{MacKenzie2012} (see \autoref{fig:sensint}). Today, we are witnessing researchers expanding the scope of HCI even further, zooming in more closely on specific interactions. A growing body of work explores the intersection of the Biological and Cognitive bands. In this work, designers and researchers focus on the fine details of interactions, specifically examining how pre-reflective sensorimotor states or \textit{perceptive acts} are embedded within larger deliberate actions and reflections on actions \cite{Ahissar2016, sensorimotorContingenciesVision} (see also \autoref{fig:loops}).





Such work explores the details of a simple deliberate act, such as moving a mouse to move a cursor to a target, and unfolds these details in their full complexity. A micro-phenomenological exploration might investigate how the experience of moving the mouse unfolds both in diachronic and synchronic dimensions in pre-reflective experience \cite{Petitmengin2018:structuresofexperience, Reed:MPforNIME}. From a psychophysical point of view, we might analyze how we dynamically adapt the force with which we push the mouse based on the deformation of our fingertip (see also Johansson et al.'s account of lifting an object \cite{Johansson2009}) or how the vibration of the mouse activates Pacinian cells that allow an experience of texture and material of mouse and its underlying surface to emerge \cite{Bensmaia2009}. Both methodologies reveal complementary information about these continuously embedded perceptive acts. While micro-phenomenology provides access to how they subjectively unfold, psychophysics and cognitive neuroscience provide ways of quantifying them.


Recognizing the importance of such sensorimotor coupling, we currently observe a recurrence of interest in interaction design focused on micro-timescales and closed-loop mappings between input behaviors and outputs. For example, the importance of small time-scale latency is observed in studies of agency \cite{preemptive, IReallyDidThat, Menzer2010, footPedals, Didion2024Who} and body ownership \cite{disembodiment}. Or, changes to the transfer function between user action and its corresponding tactile feedback have been used to modulate how we experience the world \cite{bARefoot, pseudobend, 3dPress, Fingerpad_Softness, vARitouch}. Similarly, small shifts in sensory feedback have been used to induce changes in motor behavior \cite{Gomez-Andres_sensorimotorLearning, MotionlessMovement}. Finally, manipulating sensory feedback, including visual \cite{Botvinick1998}, tactile \cite{Tajadura-Jimenez2020}, acoustic \cite{arm_dimensions, Soniband}, gustatory, and olfactory feedback \cite{Giada_scent}, can also be used to change the experience of our own bodies \cite{homuncular_flexibility, Tajadura_Jim_nez_2017, TajaduraJimenez2022}. All these experiences and systems are based around designs that use either (1) closed-loop sensing and actuation or (2) sensing and actuation systems with carefully designed timing (i.e., faster than what we consciously perceive).

Engagement with micro-timescales and input/output mappings has always been central to HCI (e.g., work by Zhai et al. on comparing elastic, isotonic, and isometric input devices \cite{zhai_3dINput}). However, for the systems discussed in this proposal, the focus of interest has shifted. While traditional HCI has been interested in, for example, how a change in mapping affects targeting performance, this new interest in this area is concerned with how the experience of executing such actions can be manipulated. Research questions in earlier explorations of input/output mappings might include "How efficient can the action be performed". Whereas, the research question central to this new generation of wearable devices shifts to "What is it like to perform this action".

## 1.3 Opportunities, Themes, & Research Questions
We identify four areas with new design postulates:

- Agency: Tight temporal coupling between actions and corresponding feedback results in increased subjective agency over the interaction. Questions: \textit{What are the different agents acting in these systems (e.g., human, machine, body, material)? How do their roles change as the (de)coupling changes? How can feedback and changes to coupling convey different agencies or perception thereof?}
- Experience of Self and (3) of Others and the World: Our sensory access to the world is of bidirectional nature. A given stimulus can only reasonably be interpreted within the context of the current motor activity; our motor activity is a consequence of sensory stimulation. This sensory feedback can change the experience we have of our body and, in turn, our actions. Questions: \textit{How can sensory feedback change the experience we have of our body, and in turn, our actions? How can we facilitate sensorimotor learning through such changes? How does (de)coupling between actions and feedback in mediated environments lead to (dis)embodiment?}
- Control: Careful design of the agency and experience of an interaction can be used to modulate the control the user has over a computer-mediated action. This might, for example, be used for designing prostheses or supernumerary limbs that feel like true extensions of the body. Questions: \textit{How do sensations of control change with dynamic changes to (de)coupling? Which body-oriented parameters provide the greatest sense of control? When does the system no longer feel separate, but rather an extension of the body?}
 
## 1.4 Objectives & Outcomes
- Create a coherent outline of relevant artifacts, systems, and interfaces that instantiate a close coupling between sensing and actuation, documenting these examples in an online collection like Haptipedia \cite{Haptipedia}.
- Identify common elements of experience, agency and control, and comprehensive understanding of the opportunities opened up by coupling sensing and action to augment the bodily experience.
- Generate a set of open research questions to be addressed in future work, creating research opportunities within a 5- and 50-year horizon
- Share theoretical methodological grounding between multi- and inter-disciplinary work, drawing on the diverse backgrounds of the community to outline a shared "success" criteria.
- Solidify a community, involving the creation of a special interest group, around sensorimotor devices to support researchers at various points in their careers in pursuing and contextualizing this work.

# Organizers
#### Paul Strohmeier, leads the Sensorimotor Interaction group (senSInt)
at the Max Planck Institute for Informatics (MPI-INF). His PhD work was honored with the SIGCHI Outstanding Dissertation Award. He has recently received an ERC Starting Grant for conducting research 
on kinesthetic perception, sensory augmentation, and
on-body systems. Paul has co-hosted 8 events at ACM conferences (Workshops, Studios and SIGs) many of which are directly related to this proposal. Paul has also been instrumental in ensuring that such events have tangible outcomes, for example in the form of follow up workshops \cite{schneider2022sustainable}, magazine publications \cite{light2017special}, and academic papers \cite{wittchen2022tactjam, HInt}.  \vspace{0.3em}

#### Laia Turmo Vidal is a Digital Futures Research Fellow at KTH Royal Institute of Technology, Sweden.
Laia's work explores sensorimotor transformations facilitated by wearables and bio-responsive technologies, with the aim to create interactive experiences that are conducive to individual and collective care, health and wellbeing. Laia has facilitated body- and movement-centered design workshops at recent CHI (e.g. ~\cite{petreca}), DIS (e.g. ~\cite{vanrheden}), and IEEE World Haptics ~\cite{seifi_exploring_2023}. \vspace{0.3em}

#### Gabriela Vega is a research assistant in the Sensorimotor Interaction Group at the MPI-INF,
where her research focuses on developing wearables for Tactile AR~\cite{vARitouch} and texture design. She is interested in human-computer interaction, haptics, AR, and tangibles for human augmentation and well-being.

#### Courtney N. Reed is a musician, performer, and assistant professor in the Institute for Digital Technologies, Loughborough University London, London, United Kingdom.
Her work explores the dynamics of agency and control between human and body through vocal performance. She designs biosignal-based wearables for augmented singing and is interested in first-person methodologies and micro-phenomenology.\vspace{0.3em}

#### Alex Mazursky is a PhD student in the Department of Computer Science at the University of Chicago,
where he designs wearable devices that provide tactile feedback, transforming otherwise passive objects and surfaces into interactive experiences. He engineers haptic actuators from the ground up, integrating actuators into custom devices that create diverse sensations—such as vibration, friction, pressure, and temperature—to augment physical and virtual spaces. \vspace{0.3em}

#### Easa AliAbbasi is a postdoctoral researcher in the Sensorimotor Interaction Group at MPI-INF,
where his research focuses on understanding human tactile perception and developing tactile displays to convey sensory information. During his PhD studies, he investigated the electro-mechanical interactions between human fingers and voltage-induced touchscreens under electroadhesion.\vspace{0.3em}

#### Ana Tajadura-Jiménez is an Associate Professor in the DEI Interactive Systems Group at Universidad Carlos III de Madrid, and an Honorary Research Fellow at the University College London Interaction Center.
She leads the i_mBODY lab, which focuses on interactive multisensory body-centered experiences at the intersection of HCI and neuroscience. She is the PI of the ERC-funded BODYinTRANSIT project, which explores the design of sensory technologies to alter body perceptions and promote positive changes in emotional and physical health in populations with body-related concerns. She has organized workshops in this space ~\cite{petreca, seifi_exploring_2023}.\vspace{0.3em}

#### Jürgen Steimle is a Professor at Saarland University where he leads the Human-Computer Interaction Lab.
Previously he was Senior Researcher at the MPI-INF and Visiting Assistant Professor at the MIT Media Lab. He holds a PhD in Computer Science from TU Darmstadt. Jürgen specializes in body-based interfaces that are soft and deformable, to offer novel opportunities for rich and expressive multi-sensory interaction. He is recipient of an ERC Starting Grant and his work on body-based interfaces has received Best Paper Awards at CHI and UIST. 

# Pre-Workshop
The workshop's Call for Participation will be shared via mailing lists (e.g., ACM SIGCHI, UIST, Augmented Humans, NIME, etc.) to researchers in HCI, engineering, psychology, and related areas. Moreover, the organizers will leverage their extensive networks of experts to ensure that people in key communities are made aware of it. All workshop information will be easily accessible via our workshop's website (\url{https://sensorimotordevices.github.io}), which will also include the complete program and accepted submissions as well as notes, sketches, and takeaways after the workshop.

 We aim to draw attendance from diverse backgrounds (HCI, psychology, engineering, etc.) to facilitate discussion that identifies links across disciplines. Potential participants will be invited to
submit a position paper (2-4 pages, following the ACM Template), in which they will describe one or multiple technologies, experiences, or experiments that explore closely coupled sensing and actuation; and 1-2 discussion points in relation to the four topic areas we propose. Submissions will be reviewed by the workshop organizing committee. A total of up to 15-20 participants will be invited to participate in the workshop based on their submissions. 

Prior to the workshop, participants and organizers will arrange each accepted submission together on a Miro board, where submissions will be clustered according to the topic themes (we anticipate themes of Agency, Self-Experience, World-Experience, and Control, among others that may emerge through discourse). We will form interest groups around these themes, which we will use for breakout discussions during the workshop. We will distribute the papers among participants and publicly on the workshop website. We will ask participants to familiarize themselves with all the papers and encourage them to add to the Miro board even before the workshop. 

# Workshop
#### Introduction \& Speed Conversing.
The in person workshop will open with a brief introduction from the organizers, reiterating the goals and research questions to be addressed. This is followed by "speed conversing" to encourage attendees to connect with each other and exchange information. Attendees will give 60-second elevator pitches of their research and goals for the workshop to other randomly selected attendees and swap groups periodically. The goal is to foster 1 on 1 discussions amongst participants.

#### Focus Groups (Session 1)
In smaller groups, attendees will discuss each of the one four topic areas identified above, according to their interest: agency, experience of self, experience of others and the world, and control. The objective of this activity is to allow attendees to discuss shared and divergent methodological and theoretical grounding, and identify important challenges and opportunities regarding the future of sensorimotor interactions in relation to the topic area (for example, articulating research questions to be addressed in a 5-year horizon, or visions of how they would like to see the area progress in a 50-year horizon).

#### Demo Session
A demo session will provide new inputs to these discussions in the middle of the day. Participants and organizers will be invited to bring physical demos which relate to the workshop topic. We will discuss the implementation and interaction experience as well as how agency, including self-attribution and control are negotiated in these interactions.

#### Focus Groups (Session 2) & Closing.
The workshop will conclude in a shared discussion, where the groups come back together to share their findings, incorporating themes from the Demo Session, and to identify commonalities and differences between groups. An approximate schedule for the workshop is as follows:

| Time            | Event                       |  
|---------------------|-------------------------------|  
| **09:00–09:15**    | Introduction & Welcome        |  
| **09:15–09:45**    | Speed Conversing              |  
| **09:45–10:30**    | Focus Groups (Session 1)      |  
| **10:30–11:00**    | Coffee Break ☕               |  
| **11:00–12:30**    | Demo Session 🎛               |  
| **12:30–14:00**    | Lunch Break 🍴                |  
| **14:00–15:30**    | Focus Groups (Session 2)      |  
| **15:30–16:00**    | Coffee Break ☕               |  
| **16:00–17:00**    | Closing Discussion            |  

# Post Workshop
We are planning for three types of workshop follow-ups. The first is an online collection, inspired by websites such as Haptipedia \cite{Seifi20-CHI-Experts}, Sensorwiki (sensorwiki.org/doku.php) or Kobakant (kobakant.at/DIY). We will publish a curated set of Systems, Experiments, and Experiences relevant to researchers interested in this topic on our website.

The outcome of the workshop will be documented to share either in the form of a blog post (e.g. at ACM interactions) or an academic publication to reach researchers and practitioners beyond the CHI attendees. The purpose of this publication will be to define the field in a way that helps junior researchers identify relevant research problems, and more senior researchers contextualize and position their work for grant writing or similar activities, for example by articulating \textit{grand challenges} \cite{grandChallenge_shapeChanging} and \textit{opportunities} \cite{HInt} for sensorimotor interaction.

We also intend the workshop to support creating a community of researchers interested in sensorimotor interaction that extends beyond the workshop itself. For this purpose a proposal for a SIG will be submitted to CHI 2025. To foster community beyond the conference, we will create a dedicated online space (e.g., Discord community or Slack group) open to those who wish to participate, with the aim of having a shared space where discussions and collaborations can continue beyond the workshop and flourish. Finally, should we find interest from the broader community, we intend to follow up with a dedicated Dagstuhl Seminar\footnote{https://www.dagstuhl.de/de/seminars/dagstuhl-seminars}. 

# Call for Participation
An emerging research direction is wearable systems in which sensing and actuation are synchronous, co-located, of the same mode, and with a temporal behavior, enabling integration with the user’s sensory and motor abilities. Such coupling opens exciting new opportunities for user experience, agency, and body ownership. 

This one-day workshop offers an interdisciplinary forum for academics and practitioners to discuss opportunities, challenges, and long-term visions in this space. We intend to identify:
\begin{itemize}
\item Artifacts, systems, and interfaces that closely couple sensing and actuation to augment bodily experience (e.g., wearables, haptics, tangibles, e-textiles)
% \item Share methodological and theoretical grounding, as well as recognizing where these differ.
\item Shared grounding across disciplines, including methods and metrics for validating "success"
\item Opportunities and insights in this area, aiming to support researchers at various career stages.
\end{itemize}

We invite potential participants to share 1-3 relevant technologies or experiences (to be discussed in pre-workshop brainstorming). Each should be presented in a self-contained manner, together with a description of its relevance. Examples by other researchers should be appropriately cited and contextualized with thoughtful commentary. Please also indicate the possibility of bringing chosen examples as physical demos to the workshop, and a short biography of the participant(s). Submissions should be 2-5 pages long (excluding references) using the CHI Extended Abstracts format and submitted as non-anonymized PDF. The deadline for submission is February 13, 2025, midnight AoE. Quality submissions will be selected by the workshop team to ensure a diversity of disciplines, backgrounds, and career stages. We will notify applicants by March 10, 2025. For more information and updates about the workshop, see \url{https://sensorimotordevices.github.io}

[back](./)
