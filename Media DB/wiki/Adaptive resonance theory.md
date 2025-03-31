---
type: wiki
subType: ""
title: Adaptive resonance theory
englishTitle: Adaptive resonance theory
year: ""
dataSource: Wikipedia API
url: https://en.wikipedia.org/wiki/Adaptive_resonance_theory
id: 3056879
wikiUrl: https://en.wikipedia.org/wiki/Adaptive_resonance_theory
lastUpdated: 2025/March/10
length: 16612
tags: mediaDB/wiki
---
> **Adaptive resonance theory** (ART) is a theory developed by Stephen Grossberg and Gail Carpenter on aspects of how the brain processes information. It describes a number of artificial neural network models which use supervised and unsupervised learning methods, and address problems such as pattern recognition and prediction.
>
> The primary intuition behind the ART model is that object identification and recognition generally occur as a result of the interaction of 'top-down' observer expectations with 'bottom-up' sensory information. The model postulates that 'top-down' expectations take the form of a memory template or prototype that is then compared with the actual features of an object as detected by the senses. This comparison gives rise to a measure of category belongingness. As long as this difference between sensation and expectation does not exceed a set threshold called the 'vigilance parameter', the sensed object will be considered a member of the expected class. The system thus offers a solution to the 'plasticity/stability' problem, i.e. the problem of acquiring new knowledge without disrupting existing knowledge that is also called incremental learning.
>
> [Wikipedia](https://en.wikipedia.org/wiki/Adaptive%20resonance%20theory)

**Adaptive resonance theory** (**ART**) is a theory developed by [Stephen Grossberg](https://en.wikipedia.org/wiki/Stephen_Grossberg "Stephen Grossberg") and [Gail Carpenter](https://en.wikipedia.org/wiki/Gail_Carpenter "Gail Carpenter") on aspects of how the brain [processes information](https://en.wikipedia.org/wiki/Information_processing_theory "Information processing theory"). It describes a number of [artificial neural network](https://en.wikipedia.org/wiki/Artificial_neural_network "Artificial neural network") models which use [supervised](https://en.wikipedia.org/wiki/Supervised_learning "Supervised learning") and [unsupervised learning](https://en.wikipedia.org/wiki/Unsupervised_learning "Unsupervised learning") methods, and address problems such as [pattern recognition](https://en.wikipedia.org/wiki/Pattern_recognition "Pattern recognition") and prediction.

The primary intuition behind the ART model is that [object identification and recognition](https://en.wikipedia.org/wiki/Visual_object_recognition "Visual object recognition") generally occur as a result of the interaction of 'top-down' observer expectations with 'bottom-up' [sensory information](https://en.wikipedia.org/wiki/Sensory_information "Sensory information"). The model postulates that 'top-down' expectations take the form of a memory template or [prototype](https://en.wikipedia.org/wiki/Prototype "Prototype") that is then compared with the actual features of an object as detected by the senses. This comparison gives rise to a measure of category belongingness. As long as this difference between sensation and expectation does not exceed a set threshold called the 'vigilance parameter', the sensed object will be considered a member of the expected class. The system thus offers a solution to the 'plasticity/stability' problem, i.e. the problem of acquiring new knowledge without disrupting existing knowledge that is also called [incremental learning](https://en.wikipedia.org/wiki/Incremental_learning "Incremental learning").

## Learning model

[[edit](https://en.wikipedia.org/w/index.php?title=Adaptive_resonance_theory&action=edit&section=1 "Edit section: Learning model")]

[![](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f1/ART.png/220px-ART.png)](https://en.wikipedia.org/wiki/File:ART.png)

Basic ART structure

The basic ART system is an [unsupervised learning](https://en.wikipedia.org/wiki/Unsupervised_learning "Unsupervised learning") model. It typically consists of a _comparison field_ and a _recognition field_ composed of [neurons](https://en.wikipedia.org/wiki/Artificial_neuron "Artificial neuron"), a _vigilance parameter_ (threshold of recognition), and a _reset module_.

- The comparison field takes an _input vector_ (a one-dimensional array of values) and transfers it to its best match in the recognition field.
    - Its best match is the single neuron whose set of weights (weight vector) most closely matches the input vector.
- Each recognition field neuron outputs a negative signal (proportional to that neuron's quality of match to the input vector) to each of the other recognition field neurons and thus inhibits their output.
    - In this way the recognition field exhibits [lateral inhibition](https://en.wikipedia.org/wiki/Lateral_inhibition "Lateral inhibition"), allowing each neuron in it to represent a category to which input vectors are classified.

- After the input vector is classified, the reset module compares the strength of the recognition match to the vigilance parameter.
    - If the vigilance parameter is overcome (i.e. the input vector is within the normal range seen on previous input vectors), then training commences:
        - The weights of the winning recognition neuron are adjusted towards the features of the input vector
    - Otherwise, if the match level is below the vigilance parameter (i.e. the input vector's match is outside the normal expected range for that neuron) the winning recognition neuron is inhibited and a search procedure is carried out.
        - In this search procedure, recognition neurons are disabled one by one by the reset function until the vigilance parameter is overcome by a recognition match.
            - In particular, at each cycle of the search procedure the most active recognition neuron is selected and then switched off, if its activation is below the vigilance parameter
            - (note that it thus releases the remaining recognition neurons from its inhibition).
    - If no committed recognition neuron's match overcomes the vigilance parameter, then an uncommitted neuron is committed and its weights are adjusted towards matching the input vector.
- The vigilance parameter has considerable influence on the system: higher vigilance produces highly detailed memories (many, fine-grained categories), while lower vigilance results in more general memories (fewer, more-general categories).