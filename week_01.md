# Week 1, the theory of inference

### Goals of week 1:
1. Understand the motivation behind inference.
2. Appreciate the similarities and differences between Frequentist and Bayesian approaches to inference.
3. Know how to manipulate probability distributions.

### Materials for week 1:
1. Chapters 2 and 3 of _Student's Guide to Bayesian Statistics_
2. Lambert's _Lecture 1_ slides.
3. **Bonus** Video lecture on the [_Bayes' Rule: The Theory That Would Not Die_](https://youtu.be/2o-_BGqYM5U) by Sharon McGrayne, first 45 minutes of the video.

### Setting the Stage

#### Big World
* Consider an observable characteristic we are trying to explain, for example the heights of 5 randomly chosen individuals.
* Assume that there exists a true process $T$ that generates the heights of all individuals in our sample.
* There is variability in the observables outputted by $T$; this can either be **ontological**, due to the inherent variability of the system, or **epistemological**, for example, because we lack knowledge of the genetics and environmental factors that affect growth.
* Imagine a set of all conceivable processes that could result in our sample of height observations, which we call the “Big World”.

#### How can we reason about the big world?

**Motivation**: we want to update our knowledge of $T$ in light of data, and use the updated knowledge to estimate quantities of interest. In our height example we might want to estimate the mean height of the entire population having witnessed our sample of 5 individuals.

**How to update our knowledge?**: Find areas of the Big World that are closest to T; ideally we would find T itself! Then estimate quantities of interest using these subsets of the Small World.

#### By constructing a small world

The infinity of the Big World is too large to be useful. Instead we first consider a subset of possible data generating processes which we call the “Small World”, or $\Theta$. The Small World corresponds to a single probability model framework; in our height example we might suppose that $H \sim N(\mu, \sigma)$, where $\mu$ is the mean height, and $\sigma$ is their standard deviation. By varying our parameters $\theta = (\mu, \sigma)$ we get different data generating processes. The collection of probability distributions we get by varying $\theta \elem \Theta$ in the Small World is known as the Likelihood.

#### Prior
The Small World is still too big for our purposes. We usually have some knowledge about which areas of the
Small World are nearest to T . For example we don’t believe that μ = 100m and μ = 1.5m are equally probable. As such, in Bayesian inference we define a prior probability density that gives a weighting to all θ ∈ Θ reflecting our beliefs. Frequentist inference does not require us to specify a prior.

#### Data
Inference is the process of updating our prior knowledge in light of data. In Bayesian inference with a likelihood and our prior knowledge explicitly stated we use Bayes’ rule to find our posterior probability density over θ ∈ Θ. The lack of a prior means that in Frequentist inference we generate posterior weightings approximately using rules of thumb.

### A first take on the steps of Bayesian inference
Watch Lambert's YouTube lecture on [the intuition of Bayes' rule](https://youtu.be/yvWlpwnT1nw), 8 minutes.

1. Define the observables, ie the Big World, ie [Big Sky](https://youtu.be/zOusKPeH7nU) by the Kinks.
2. Specify a likelihood.
3. Specify a prior.
4. Input the data.

#### Example, frequency of lift malfunctioning
_Material: slides 130 to 233 of Lecture 1_

Imagine we want to create a model for the frequency a lift (elevator) breaks down in a given year, X . This model will be used to plan expenditure on lift repairs over the following few years.

An aside: [how to survive a falling lift](https://www.npr.org/sections/krulwich/2010/09/17/129934849/how-to-survive-when-your-elevator-plunges)

1. Assume a range of unpredictable and uncorrelated factors (temperature, lift usage, etc.) affect the functioning of the lift, so we say X ∼ Poisson(θ), where θ is the mean number of times the lift breaks in one year.
2. By specifying that X is Poisson-distributed we define the boundaries of the Small World.
3. _Important_: we don’t a priori know the true value of θ therefore our model defines collection of probability models; one for each value of θ. We call this collection of models the Likelihood.

By specifying a model framework X ∼ Poisson(θ) we defined the boundaries of the “Small World”. The Small World contains a collection of probability distributions known as the Likelihood.

Assume we find that the lift broke down 8 times in the past year. Our likelihood gives us an infinite number of possible ways in which this could have come about. Each of these ways corresponds to a unique value of θ.

We know that any of these models, each corresponding to different values of θ, could generate the data.
In inference we want to use our prior knowledge and data to help us choose which of these models make most sense. Essentially we want to run the process in reverse.

Both Frequentists and Bayesians essentially invert: p(X |θ) → p(θ|X ). This amounts to going from an ’effect’ back to a ’cause’. Their methods of inversion are different.

### Different Worlds More Formally

#### Statistical Inference, Bayesian versus Frequentist worlds
_Material: Sections 2.3, 2.4, 2.5, 2.6, 2.7 of Students' Guide_

1. Bayes' rule allows us to go from effect back to its cause.
2. Statistical inference is the logical framework which we can use to trial our beliefs about the noisy world against data.
3. Frequentists assume the data is random and results from sampling from a fixed and defined population.
4. Bayesians assume that we are witnesses to the data, which is fixed, and probabilities are an expression of subjective beliefs that can be updated in light of new data.
5. For Bayesians parameters are seen as varying or our knowledge about them is imperfect, while frequentists assume parameters are constant and represent a long run average.

#### Frequentist and Bayesian Inference
_Material: Sections 2.8, 2.9 of Students' Guide_

1. Bayesian inference is the only logical and consistent way to modify our beliefs to account for new data.
2. Frequentists use inverse probability as evidence for a given hypothesis and compute the probability of obtaining a sample as extreme as or more than the one actually obtained assuming a hypothesis is true.
3. Bayes' forumla circumvents the problem of generating fictious samples by inverting the Frequentist probability to obtain the probability of the hypothesis given the data we obtained.
4. Examples: murder trials, radio control towers, coin flipping, ...
5. Inference via Bayes' rule: parameters, probability distribubtions, likelihoods, priors, denominator, posterior.

### Probability Distributions
_Material:_
* _Chapter 3 of Students' Guide_
* _Slides 239 to 285 from Lecture 1_
* _Lambert's YouTube lecture on [random variables and probability distributions](https://youtu.be/pvkhK03aFDM), 7 minutes.
* _Lambert's YouTube lecture on [continuous distributions](https://youtu.be/s87mffcX0xU), 8 minutes._
* _Lambert's YouTube lecture on [discrete distributions](https://youtu.be/4Ghtj_iTSpI), 6 minutes._

#### Why is this important?
Bayesian inference quantifies uncertainty through probability distributions.

#### Discrete Distributions


#### Continuous Distributions


### Two-dimensional probability distributions
_Material:_
* _Sections 3.3.4, 3.3.5 of Students' Guide_
* _Slides 286 to 285 from Lecture 1_



### Conditional distributions
_Material:_
* _Sections 3.3.4, 3.3.5 of Students' Guide_
* _Slides 286 to 285 from Lecture 1_








#### Aside on ontonology and epistemology
From [Clément Renaud, intermittent hack philosopher](https://www.quora.com/What-is-the-difference-between-ontology-and-epistemology):
> Ontology and epistemology are both important elements of the philosophy of knowledge. If they often overlap, they have clear distinction : epistemology is about the way we know things when ontology is about what things are.
>
> Epistemology is a field of science that tends to describe the many approaches we can chose to understand our world. It is by definition the science of knowledge and consequently is often understood as a meta-science : the science of defining what is the "scientific way". Mostly, it studies the fundamental choices or givens you take into account when you attempt to know something.
>
>For example, cybernetics use the model of a system as an epistemological approach to explain facts and phenomenons. Derived from it, science today use widely the network model as a premise to understand various things, for instance cities. When we say: "Ok, let's try to understand the structure of modern cities as a network" this is epistemology in practice - to chose a bias.
>
>Then start the ontological debate : "But modern cities are actually structured as networks !" Now that is it : we are all set up for a boring egg and chicken debate, one saying : "It is like this" and the other saying "It is just because you look at it that way". This happens all the time.
>
>Ontology is about describing things and their relationships to answer the question "What is it?" while epistemology's personal concern is to investigate the ways that leads you to think that.
>
>Imagine the ontology saying "This is that", then the epistemology will answer : "How can you be so sure of what it is if you don't even know how you know it?"
>
>Let's take a famous quote from Wittgenstein's Tractatus Logico-Philosophicus : "The world is the totality of facts, not of things" .This is an ontological assertion - it challenges the nature of the world (what it is) - then it leads us to an epistemological consideration - to reconsider how we have looked at the world before.
>