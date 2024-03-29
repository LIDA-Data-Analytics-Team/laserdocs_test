---
layout: default
title: Data Risk Classification
parent: Mermaid
nav_order: 2
---

<head>
  <script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js">
  <script>mermaid.initialize({startOnLoad:true});</script>
</head>

# Data Risk Classification Flow

![image of data risk flowchart](../../images/mermaid/data_risk_flow.png)

Scroll down and zoom in...

<div class="mermaid">
flowchart TD;
	Start[Start] --> Generate{"Will the research generate (including by <br/> selecting, sorting or combining) any <br/> personal data"};
	Generate --> |No| Input{Will any project input be personal data};
	Generate --> |Yes| Threat{Would disclosure pose <br/> a substantial threat to the <br/> personal safety, health or <br/> security of the data subjects?};
	Input --> |No| Commercial_1{"Will you be working with <br/> commercial-in-confidence information <br/> or private third party intellectual property <br/> or legally or politically sensitive data?"};
	Input --> |Yes| Public{"Is that personal data legally accessible by <br/> the gerneral public with no restrictions on <br/> use?"};
	Commercial_1 --> |No| Advantage{Will releasing any of the datasets or results <br/> impact on the competitive advantage <br/> of the research team?};
	Commercial_1 --> |Yes| LowConsequence_1{Do you have <br/> high confidence that the commercial, legal <br/> reputational or political consequences of <br/>unauthorised disclosure of this data <br/> will be low?};
	LowConsequence_1 --> |No| LikelyAttackers;
	LowConsequence_1 --> |Yes| TrivialConsequence{Do you have <br/> high confidence that the commercial, legal <br/> reputational or political consequences of <br/>unauthorised disclosure of this data <br/> will be trivial?};
	Advantage --> |No| Tier0[Tier 0];
	Advantage --> |Yes| Tier1[Tier 1];
	Threat --> |No| Tier3[Tier 3];
	Threat --> |Yes| Tier4[Tier 4];
	Public --> |No| Pseudonymised{Is that personal data <br/> pseudonymised?};
	Public --> |Yes| Commercial_1;
	Pseudonymised --> |No| Threat;
	Pseudonymised --> |Yes| AbsoluteConfidence{Do you have absolute confidence <br/> that it is not possible to identify individuals <br/> from the data, either at the point of entry <br/> or as a result of analysis that <br/> may be carried out?};
	AbsoluteConfidence --> |No| StrongConfidence{Do you have strong confidence <br/> that it is not possible to identify individuals <br/> from the data, either at the point of entry <br/> or as a result of analysis that <br/> may be carried out?};
	AbsoluteConfidence --> |Yes| Commercial_1;
	StrongConfidence --> |No| LikelyAttackers{Do likely attackers include sophisticated, <br/> well resourced and determined threats, such as <br/> highly capable serious organised <br/> crime groups and state actors?};
	StrongConfidence --> |Yes| Commercial_2{"Will you be working with <br/> commercial-in-confidence information <br/> or private third party intellectual property <br/> or legally or politically sensitive data?"};
	Commercial_2 --> |No| Tier2[Tier 2];
	Commercial_2 --> |Yes| LowConsequence_2{Do you have <br/> high confidence that the commercial, legal <br/> reputational or political consequences of <br/>unauthorised disclosure of this data <br/> will be low?};
	LikelyAttackers --> |No| Tier3;
	LikelyAttackers --> |Yes| Tier4;
	LowConsequence_2 --> |No| LikelyAttackers;
	LowConsequence_2 --> |Yes| Tier2;
	TrivialConsequence --> |No| Tier2;
	TrivialConsequence --> |Yes| Tier1;
</div>

