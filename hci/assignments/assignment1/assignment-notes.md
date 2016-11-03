# General notes

it may be better not to think of designing a system, or an artifact, but to think instead about designing interventions. The product of a design exercise 
is that we intervene to change the situation as it is; we hope, of course, changing it for the better.

# Goal of the research

The goal of the research is to inform the design of a mobile tourism application targeted at parks, botanical gardens and green spaces in general and how tourists (or local people) can find them in a city and interact with them.
The application will include specific events in various areas (food, music etc...), festivals, fun family days, events for children etc... Every aspect related to booking tickets, venues or equipment, guided tours and more will be handled by the application.
The interaction design is established for a new mobile application instead of analysing the design of pre-existing systems.
The efficiency of the application comes when people want to organise outdoor activities such as educational visits, family venue hire (e.g. weddings); therefore it might be limited for individual use.
Moreover people can build their own tours and share it with others.

Another goal of the system is to let users to apply for various memberships through the same application. A general membership for all green spaces in the designated city will be available.
For botanical gardens there will also be an online shop which sells items that can be collected from the garden itself or delivered.

On-field devices will allow virtual (if guides are not available) and walking/bike tours.
Another on-field device is the 360° camera which will be placed at panoramic views. This allows people to take group photos and save them to their mobile through the application and/or share them through social media (see Facebook 360° picture/video support).

The research will include insights on the advantages and disadvantages of pre-existing systems.
Before delving into the description of the various requirements gathering techniques, constraints and trade-offs of the systems will be outlined.

A 2-stage user identification process has been adopted:
1. Making clear which groups of users we are targeting through stakeholder analysis
2. User needs must be identified through the various requirements gathering techniques.

## Constraints

Following are the constraints that the development of such mobile application must consider:

- The actual development of the mobile application requires permission of data access from the city council.
- Permission is required to place devices used by the mobile application across the selected parks and gardens.
- Cost of the devices.
- Time of development of both the actual application and the infrastructure.
- For the membership feature, collaboration is needed between the development team, the city council and the green spaces associations (if not affiliated with the city council - such as many botanical gardens).

## Trade-offs

This section will outline which goals or constraints can be relaxed so that others can be met.

If the council does not allow the devices to be placed in the agreed spaces then the placement of 360° cameras can be cancelled or post-poned for a next release of the software.

However the development of virtual tours is of utmost importance since it will directly benefit tourists (the primary users).
Therefore more time must be allocated for the agreement between the two parties and the placement and risk assessment of such devices.

Memberships play an important role in the application since they enable local people to interact directly with the various green spaces.

## Stakeholder analysis

As [user_req_analysis.pdf] states, stakeholder analysis identifies all the users and stakeholders who may influence or be impacted by the system.
This helps ensure that the needs of all those involved are taken into account. The user groups for this mobile application are:

- Primary users: tourists, local people and school teachers
- Secondary users: city council, schools, botanical gardens associations or companies

The research will focus on tourists and school teachers since elements that may arise from local people are included in those that arise from school teachers.

For each stakeholder group we will identify their main roles, responsibilities and task goals in relation to the system.

### Tourists

The main roles of tourists is to collaboratively book guided tours (preferrably not virtual) and check parks equipment.
Their tasks involve:

- Collaborative planning of tours and share them with others in the same area (which can be rated by the latter).
- Check and book park equipment.
- Find walking/bike tours.

### Local people

The main roles of local people in regards to the mobile app is to collaboratively plan tours or activities with other families or between themselves.
Their tasks involve:

- Collaborative planning of tours and sharing of the latter.
- Booking tickets for events/festivals.
- Booking venues for family fun or weddings.
- Buy from botanical gardens.
- Apply for memberships.

### School teachers

School teachers may be part of the local people user group, however they require additional tasks including organisation of school trips which in turn contains all documents and administration aspects of organising a trip.

# Requirements gathering techniques and their impact on the goal

In this section we are going to explore the different requirements gathering techniques, how they can be used efficiently and for which aspect of the research they are useful.

The research wants to get insights on the important aspects of interactions with green spaces:

- what are the current practices to plan outdoor activities?
- what are the difficulties of such planning phase?
- is the prospect of having a unified and focussed (in terms of area, e.g. Birmingham and information availability) app appealing?

In this regard we are going to explore the 3 different methods of requirements gathering: questionnaires, interviews and observation methods.

## Questionnaires

Questionnaires involve administering a set of written questions to a sample population of users. They can help determine the needs of users, current work practices and attitudes to new system ideas. [user-req-analysis.pdf]
When using questionnaires it is possible to target a large sample of people. This is useful to gather data on a wide variety of topics, quickly and cheaply. Questionnaires are more efficient when they mainly provide
quantitative data (although nothing prevents from qualitative data to be used). However questionnaires are not useful in situations when possible new insights might be captured by follow-up (flexible) questions which
are not included in the questionnaire. Moreover participants may rush the questionnaire or give inaccurate answers. Interpretation of the questions may vary from individual to individual if the query is not correctly formulated. This leads us to the analysis of interviews.

## Interviews

As [user-req-analysis.pdf] states, interviewing is a commonly used technique where users, stakeholders and domain experts are questioned to gain information about their needs or requirements in relation to the new system. Interviews are usually semi-structured based on a series of fixed questions with scope for the user to expand on their responses.

This technique can obtain private aspects of behaviour and collect detailed qualitative data. When dealing with different groups of stakeholders a semi-structured approach must be taken: start with structured/base questions
and, towards the end, try to uncover additional information not planned in the questions.

The advantage of using interviews instead of questionnaires is that new ideas may arise during the conversation that could not be captured by a questionnaire. This gives an in-depth look at each participant. 

However the questions may be biased; this will lead the participant to give answers that will satisfy the goals of the research.

## Observation

Observational methods involve an investigator viewing users as they work in a field study, and taking notes on the activity that takes place. [www.usabilitynet.org/tools/userobservation.htm]
A benefit of this method is that it allows the observer to view what users actually do in context.
It should be noted that observation can be obtrusive and subjects may alter their behaviour due to the presence of an observer. Another problem is the length of the process since the interaction design research must look at 3 different groups of users.

# Method

The method chosen to gather user requirements is interviews. Firstly, a mixed approach (questionnaires + interviews) was intended; however, as noted in [http://pareonline.net/getvn.asp?v=15&n=1], problems may arise when aligning data from the two 
different  methods.

Questionnaires are a relatively quick method of determining preferences of large user groups, however they do not capture in depth comments and may not permit follow-up.

Because of the one-to-one nature of the interview process, what is talked about can directly address the informant's individual concerns. Mistakes and misunderstandings can be quickly identified and cleared up (aspect not possible
in questionnaires).

On the other hand, observational techniques are very useful to relate users with the environment they are involved in. In fact with the other two methods it is not possible to capture aspects that related to the working context. However drawbacks of observational techniques are their obtrusive nature, limited applicability and time. Limited applicability means that for some use cases their use does not lead to efficient requirement gathering. In fact they are very useful in industrial or work settings rather than assessing leisure activities.

In this use case interviews are the best tool in the sense that if correctly planned they lead to accurate and in-depth results with additional information being gathered. Moreover we can achieve the same qualitative and quantitative balance that questionnaires offer (although more qualitative-inclined).

# Planning and study

Following is how to run the interviews:

1. The planning phase involves the preparation of an 'interview schedule'. This is a set of topics which group the questions to be asked. For each topic, there will be an explanation.
2. The information will be recorded using written notes and tape recorder.
3. A trial run of the interview will be executed in order to practice and be fluent.
4. A document of confidentiality and consent will be presented to the participants. The participants can choose anonimity.
5. At this point a brief background of the study will be presented to the participants. This helps contextualise the focus of the questions and their responses.

After this, it is useful to consider the interview in five main stages as defined in [oro-req-gathering.pdf]:

1. Background: obtain the subjects' background details, such as their experience with previous planning applications and experience in general.
2. Letting off steam: asking general question about the topic to allow the building of a relationship between interviewer and participant.
3. Core session: where questions are asked (may allow insight from users and follow up questions).
4. Addressing issues: any issues that have not naturally been dealt with through (3) should now be introduced.
5. Debriefing/conclusion: here there will be a reaffirmation that the info will be dealt with in the strictest confidence. If the participant wants to raise additional discussion points this is the time to deal with them.

The selected participants are 1 school teacher and 1 EU citizen (recently moved to the UK - kind of tourist).

The question set can be found in Appendix A.
Appendix B contains the transcripts (raw interview data).

# Analysis and results

An interpretation session has been conducted on the transcripts to produce the key elements relevant to the study. These are grouped into notes for later affinity diagramming.

[Figure here]

-- Thematic analysis has been conducted on the transcripts (raw interview data) to highlight themes/codes to ...

Affinity diagramming has been used as a first step to group user's insights into themes. The affinity is built bottom up, by raising common issues and/or themes out of the individual
notes captured during the interpretation session.

[Figure here]

The output of affinity diagramming will serve the project manager in order to allocate resources to the various teams and managing communication/workflow between them.

# Considerations

# References

# Appendices

# Appendix A

Following are the fixed set of questions that have been asked to each participant. Then for each participant there will be the additional follow up questions marked as [FQ] with the original question number.

## Fixed set of questions

### 1. Background

1. What is your profession?
2. Are you a UK citizen? If not how many years have you spent in the UK?
3. Which activity do you usually do in your free time, when you're outside?
4. How often do you go to the following places (Never, Sometimes, Usually, Often):
	- Public parks/green spaces
	- Botanic gardens
	- Forests
5. What kind of activities do you practice in each place (not answered with 'Never')?
6. Do you attend public events in the places you indicated above?
6.1 If yes, how would you find about these events?
6.2 And which system do you use for booking tickets?

### 2. Issues with current systems

1. In general, how is the experience with the above mentioned system(s)?
	- Very bad
	- Bad
	- Good
	- Very good
1.1 If you answered bad or very bad what is the aspect that you don't like about it?
2. Did you find yourself in a situation where no online information was available for an outdoor event?

### 3. Open/exploratory questions

1. Outline your routine when you go to green spaces such as a public park or botanic gardens.
2. [For school teacher] If you are given the task to organise a local outdoor school trip what would the process be?
3. [For tourist] Would it be a nice idea to have all information regarding events and other activities in all public parks/forests/botanic gardens be available in one place?
4. What do you think forests (small or medium sized) lack in terms of equipment and activities here in Birmingham?

### 4. Collaborative planning

1. Imagine you and your family want to organise a day out. How would you go for that? Outline the whole process.
2. Is the idea of having a remote collaboration tool that enables families to organise outdoor trips appealing?

### 5. Additional features (memberships, online shops & in-place 360° photos/videos)

1. If you usually go to botanical gardens and public parks (with bookable equipment and/or frequent events), would you be interested in memberships?
1.1 If yes, is the idea of having individual memberships of all green spaces in Birmingham appealing? What about a general membership/discount set up by the city council?
2. The system will have 360° cameras placed at each park/botanical garden in Birmingham. Using the mobile app people can connect to one of these by activating the location option and waiting for the application to locate the camera. Afterwards every picture or video taken by the camera will be sent to the application which can be later shared. What is your opinion on such system?
3. Do you frequently buy online? What about botanical products, flowers etc...?

# Appendix B

- I: interviewer
- P: participant

## Participant 1

- I: What is your profession?
- P: Currently I'm a primary school teacher in Coventry.
- I: Are you a UK citizen?
- P: Yes, moved here from Malta 13 years ago and got citizenship.
- I: Which activity do you usually do in your free time, when you're outside?
- P: Mmm... Usually a picnic or bike riding with my family.. I have a husband and three daughters. We go to Coombe Country Park. Yeah, that's it.
- I: How often do you go to each of the following places: public parks, botanic gardens, forests? (Never, Sometimes, Usually, Often)
- P: Well... we go to parks almost every weekend. We sometimes go to the Moseley Bog in , it's really cool there.
- I: What about botanic gardens?
- P: Ah yes, I don't usually go with family but with the school. In fact we organised 2 botanical gardens trips for the year, one in the Pleasure Gardens and the other to the Tropical House in Birmingham.
- I: So, do you attend public events and/or festivals in parks - in Birmingham or Coventry?
- P: Yeah the kids love CircusMASH in Birmingham! We also went several times to the Castle Bromwich Hall Gardens for a Family Fun Programme.
- I: How do you find about such events?
- P: Well to be fair I get told about them by colleagues. Sometimes I want to search on Google but I end up getting lost... it's just too much scattered information. I can't focus, well can't select exactly what I want, when, the prices and yeah.
- I: Ok, so you think the current system for booking events/tickets and finding info in general is not working?
- P: Yes, it's just about the level of detail and how scattered is the current information.
- I: Imagine a mobile application that has all parks/forests/botanical gardens information in one place. The app will also let you manage bookings, tours and creation of events. Is something you would frequently use?
- P: Absolutely! As I said, every weekend we go to these parks in Birmingham, well sometimes in Coventry as well, where we have family events and circus stuff. I would love something to ease the whole thing.
- I: So what exactly are the aspects that you don't like about the current systems?
- P: There's quite few things actually. Firstly is the scattered information I told you about. Then is the process of organising trips. Awful, fill in forms, you have to print them then scan them, wait for weeks.
- I: So, if the process was all done using one app and all the info was there would it be easier?
- P: Definitely, it would at least ease my part of organising. As for waiting weeks that has to be done.
- I: You said you oranised a school trip. Can you please detail the process?
- P: Alright... I need to fill in a risk assessment form which details generic, site specific and on-going risks. These are prepared by the council and sent to schools. Next I need to produce forms for parental consent, allocate a certain number of supervisors, contacting the transport agency, insurance and other minor stuff related to food. All this is very tedious and takes time.
- I: Ok, so something that would bring all these documents in one place and automating some parts -those that can be of course- of the process would be helpful?
- P: I'd love something like that! Mmm, actually wait, what if I want more flexibility? Say I want to drive a minibus instead of arranging with a transport company?
- I: Easy you just skip the transport section and carry on with the other documents. Now let's move to 'forests', I think you said you went to the Moseley Bog in Birmingham?
- P: Yes, it was a while ago. It was really just a walk, nothing exceptional.
- I: Would you like more activities to be available?
- P: Few years ago, I went with my husband to Italy, to the 'I suoni delle Dolomiti' (sounds of the Dolomites) event in Trentino Alto-Adige region in the North. This is a music festival usually held in forests in the Dolomites. The way up to the acutal event had various wood artwork as well as wooden physical activities - these were actually meant for runners.
- I: Moving to the collaborative aspect of the mobile application. Imagine you are planning a day-out with another family. How would you go for that?
- P: ...
- I: Is the idea of having a remote collaboration tool that enables families to organise outdoor trips appealing?
- P: ...
- I: Let's move to the additional features of the mobile application. So, you usually go to botanical gardens and public parks (with bookable equipment and/or frequent events), would you be interested in memberships?
- P: I'm actually signed up for a membership in Birmingham City Council Parks that organise seasonal programmes including fun events for families, craft activities and guided walks.
- I: What about a general/unified membership that will benefit mainly in terms of discount?
- P: That would be amazing although I might not use it frequently. But yeah a base membership would be helpful not only for the members but also for the city council. You see, this application you have in mind is actually benefitting the city council.
- I: That's interesting... The next feature is the 360° cameras placed in each park/botanical garden that will allow you to take photos or videos and save them directly to your mobile app or share them with friends - depending on what option you choose.
- P: Yes I saw some really nice pictures on Facebook where you can see the whole scenery. I wondered how I could do that with my smartphone.
- I: Yeah you can use Facebook to do them but then you have to manually do it yourself and ensure that the scenery is somewhat static. What we are trying to do is place appropriate 360° cameras across most (if not all) parks in Birmingham and you can connect to one of them with the mobile app.
- P: That's actually really nice especially for family photos! I'm not into selfies like my eldest daughter!
- I: Do you frequently buy online? What about botanical products, flowers etc...?
- P: Yes I buy lots of clothes and devices online. Sometimes I also do food shopping online. It's so easy and without effort. As for botanical gardens I bought some flowers from the Birmingham botanical gardens website. However I had to search in various botanical garden websites.. I think it was the Mediterranean and Arid houses. So yeah, before actually getting the indoor geranium I wanted I had to look for a while.

## Participant 2

- I: What is your profession?
- P: I work as a nanny here in Birmingham, near Moseley.
- I: Are you a UK citizen?
- P: No, no I'm Italian, from Rovereto a small city in the North of Italy.
- I: That's interesting, so how long have you been in the UK?
- P: Almost 2 years now... I spent 5 months in Derby then moved to Birmingham in 2015.
- I: You left Italy to come to the UK? How come?
- P: Yeah a lot of people ask me the same question! I came here to finish my studies in social sciences. I'm doing part-time, since I'm a single mother with 2 children... so yeah I have to work to keep up with the costs.
- I: Have you every visited the UK before coming here to study/work?
- P: Yes I have been a couple of times in London and Birmingham. This was about 3 or 4 years ago. I was here with a friend from France... It was a nice experience, in particual London!
- I: So, did you attend events, festivals and other activities in parks or open spaces when you first came here to Birmingham?
- P: Yes, I went to lots of parks here, because I used to go out with family a lot back in Italy. We have lots of forests and guided walks. Basically I went to Cannon Hill Park, Winterbourne, Swanhurst Park, Kings Heath Park... yeah and the one I usually bring the children to, Sheldon.
- I: Oh that's nice, what kind of activities do you practice in these places?
- P: I always go for events or festivals like the Outdoor Leadership Centre, Kids Run Free in Kings Heath Park and Walking Meditation in Cannon Hill Park near the cricket ground. I like to run a lot, it's rewarding and keeps the stress away... I go often now, to these events, since I know Birmingham very well. Back in Italy there are more forests than big public parks, since I live near the alps I usually go up to mountains such as Montalbano di Mori, Monte Zugna and many others.
- I: So how do you find out about these events?
- P: I just check online with my phone. I usually find quickly the information there, but mostly it's just my friend that tells me about them.
- I: You said that you usually find quickly the info you want. I assume that sometimes you can't find the information right?
- P: Yeah especially when some sites are under construction or there is a page not found. This happens quite a lot actually. All the parks are accessible from the Visit Birmingham website which is really nice and straightforward. From there all links bring you to different websites, which is very unpleasent. I don't like it, especially when the website is bad, the colours are awful.
- I: So your concern is about the sparse information?
- P: Yeah you can't.. you have to click and go here and there just to find something. I don't like it at all; when I first came here [...]
- I: Would it be a nice idea to have all information regarding events and other activities in all public parks/forests/botanic gardens be available in one place? Like in map and text format. Big events will be highlighted and recommendation/reviews from users will be enabled. Ticket and all administrative concerns will be included in the application.
- P: That would be fantastic... [...]
- I: Earlier you said back in Italy you were into forests and mountains. What do you think forests (small or medium sized) lack in terms of equipment and activities here in Birmingham?
- P: I think Birmingham has great green spaces and open spaces in general. But I haven't seen big activities or festivals in forests. In terms of events I'd like to see music festivals, and for activities a kind of street workout but in the forest would be great; I remember this from a place in London where me and some family friends went to. 
- I: The mobile app will feature a route planner (walk, run or bike ride) which you can collaboratively build with other people. What's your opinion on this?
- P: Mmm... I honestly don't see the point in it. I would love to use it for myself but not with other people remotely; we can just text each other.
- I: Wouldn't it be fraustrating to text or even to call? I mean in collaboration, through map highlighting and video calls, you can quicly decide where to go and what to do.
- P: Yeah, I mean I can try it just to test a different setup maybe.
- I: I see that you are involved into the leisures activities in Birmingham's public parks. Would you be interested in a general membership of all parks? Through the mobile app you can also apply for individual ones.
- P: Amazing, currently I have memberships for events in Swanhurst and Cannon Hill parks. I'm signed up to their newsletters so I really would like a general membership for all Birmingham parks; see, even if I don't go to some the mere fact I get event information via email is great!
- I: Now let's move to the 360° cameras feature. The system will have 360° cameras placed at each park/botanical garden in Birmingham. Using the mobile app people can connect to one of these by activating the location option and waiting for the application to locate the camera. Afterwards every picture or video taken by the camera will be sent to the application which can be later shared. What is your opinion on such system?
- P: I use Facebook a lot so that would be great. I set up a FB group with Italian friends where me - in the UK - and others in France and Germany post pictures, so I would definitely use it.
- I: Nice, do you frequently buy online?
- P: I just recently started to buy online, to be honest. In Italy this practice is not very popular; this is because most people don't have that attachment to technology for everything. This is also influenced by the state. In fact lots of administrative stuff is still done using paper, whereas here in the UK there are a lot of online services. That's why people in the UK are more inclined to online solutions compared to Italians.
