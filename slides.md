---
colorSchema: light
routerMode: hash
layout: cover
theme: neversink
neversink_slug: Goals in RL
mdc: true
---

# Toward Complex and Structured Goals in Reinforcement Learning

**Guy Davidson & Todd M. Gureckis**  
_New York University_
<Email v="guy.davidson@nyu.edu" />

---
layout: default
---
# Goals in Reinforcement Learning

<v-clicks depth="2">

- McCarthy's definition of intelligence and goals.
- Reward hypothesis.
- Goals as preferences over state-action histories \[Bowling et al., 2023].

</v-clicks>

---
layout: two-cols-title
---

:: title ::
# Straining these definitions of goals

::left::

<div class="flex flex-col justify-between" style="height: 75%;">
<div>
<div><v-click at="+1"><h3>Goals as intended behaviors</h3></v-click></div>
<div class="ns-c-tight"><v-clicks at="+2">

- Act safely
- Don't get stuck
- Avoid collisions
- Be efficient
- Don't run out of battery

</v-clicks></div> 
</div>     

<div>
    <div class="flex flex-row justify-center">
        <figure class="image is-square is-inline-block" v-click="+2">
            <img src="/images/roomba.webp" width="300">
        </figure>
    </div>
</div>

</div>



<!-- <div class="ns-c-tight">
    <v-clicks at="+2">

    - Act safely
    - Don't get stuck
    - Avoid collisions
    - Be efficient
    - Don't run out of battery

    </v-clicks>
</div> -->

<!-- <div class="has-text-centered"> -->
<!-- <div>
        <div class="is-flex is-justify-content-center">
        <figure class="image is-square is-inline-block" v-click="+2">
            <img src="/images/roomba.webp" width="300">
        </figure>
    </div> -->

::right::

<div class="flex flex-col justify-between" style="height: 75%;">
<div>
<div><v-click at="+1"><h3>Creativity, richness of human goals</h3></v-click></div>
<div class="ns-c-tight">
<ul>
<v-click at="+1"><li>Children (and adults) create playful goals</li></v-click>

<v-click at="12"><li>These goals help us learn how to structure problem spaces and find solutions
<span class="text-xs"><br>[Chu & Schulz, 2020; Molinaro & Collins, 2023; Chu et al., 2024]</span></li></v-click>
</ul>
</div> 
</div>     

<div>
    <div class="flex flex-row justify-center">
        <figure class="image is-square is-inline-block">
            <v-switch>
                <template #1><img src="/images/logan_truck.jpg" width="240"></template>
                <template #2><SlidevVideo width="320" controls>
                    <source src="/videos/jordan_bird_trimmed.mp4" type="video/mp4">
                </SlidevVideo></template>
            </v-switch>
        </figure>
    </div>
</div>

</div>
 

---
layout: side-title
align: rm-lm
---

:: title ::

## Core idea&nbsp;<mdi-lightbulb />

:: content ::

If we want to develop agents that accomplish diverse tasks across different environments, 
we need agents that can propose and pursue rich, complex, and creative goals.

<span class="text-xs">\[Ouedeyer et al., 2007; Colas et al., 2023]</span>

---

# Desiderata for Goal Representations

<v-clicks depth="2">

- Abstraction (abstract goals, abstracting goal components)
- Temporal extension
- Compositionality
- Grounding

</v-clicks>


---
layout: two-cols-header
---


# Surveyed Goal Representation Approaches

::left::

<div>
<v-clicks depth="2">

- Implicit (directly encoded as reward functions)
- Goal states (e.g. target manipulator positions)
- Image-based observations 
- Natural language-based goals
- Represented as programs? 

</v-clicks>
</div>
::right::

<div class="grid grid-cols-2 gap-2">
    <div><figure class="image is-square is-inline-block">
        <img src="/images/reward_function_grid.png" width="120" v-click="1">
    </figure></div>
    <div><figure class="image is-square is-inline-block" v-click="2">
        <img src="/images/goal_observation.png" width="120">
    </figure></div>
    <div class="col-span-2"><figure class="image is-inline-block">
        <img src="/images/vision_language_goals.png" width="300" v-click="4">
    </figure></div>
    <div class="col-span-2" v-click="5">
```lisp
(preference throwBalltoBin
(exists (?d - dodgeball ?h - hegagonal_bin)
(then
    (once (agent_holds ?d))
    (hold (and (not (agent_holds ?d)) (in_motion ?d)))
    (once (and (not (in_motion ?d)) (in ?h ?d)))
)))
```
    </div>
</div>

<!-- <div class="flex flex-col justify-between content-center" style="height: 75%;">
    <div><figure class="image is-square is-inline-block">
        <img src="/images/reward_function_grid.png" width="120">
    </figure></div>
    <div><figure class="image is-square is-inline-block">
        <img src="/images/goal_observation.png" width="120">
    </figure></div>
    <div><figure class="image is-inline-block">
        <img src="/images/vision_language_goals.png" width="300">
    </figure></div>
</div> -->

<style>
    .image img {
        display: block;
        margin-left: auto;
        margin-right: auto;
        margin-top: 0.5em;
    }
</style>
    

---
layout: side-title
align: rm-lm
---

:: title ::

## Key takeaway&nbsp;<mdi-food-takeout-box />

:: content ::

Prevalent non-language approaches facilitate grounding at the expense of other desiderata
Language (and programs) offer benefits at the cost of grounding complexity

---

# Example argument: compositionality
- **Reward functions:** Compose mathematically, not semantically
- **Observations:** Composing images to represent general properties is hard
- **Language:** Inherently compositional, but grounding is hard 
    - SuccessVQA near chance on held-out goals \[Du et al., 2023a]
    - Hill et al. \[2019] generalize to held-out objects, but not negations
- **Programs:** Compose by default, as defined by their grammar
    - The structured LTL-based approach of Leon et al. \[2022] composes negation succesfully 


---
layout: two-cols-title
---

:: left ::
# Takeaways&nbsp;<mdi-food-takeout-box />
<v-clicks depth="2">

- **Takeaway 1:** We need agents that can propose and pursue rich, complex, and creative goals.
- **Takeaway 2:** This requires richer goal representations and developing methods to ground them.
<br><br>

</v-clicks>
:: right ::

<v-clicks at="+1">

## Questions <mdi-chat-question />

- Where do goals (and their representations) fall on the agent-environment boundary?
- What important desiderata are we missing?
- How do temporally extended goals play with the Markov assumption?
- Can program-based goals scale to diverse environments?
- What can building agents that propose and pursue rich goals teach us about human goal-setting?

</v-clicks>
