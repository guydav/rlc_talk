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

- McCarthy's definition of intelligence and goals.
- Reward hypothesis.
- Goals as preferences over state-action histories [Bowling et al., 2023].

---
layout: two-cols-header
---
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
layout: fact
---

## Core idea:
<br>
If we want to develop agents that accomplish diverse tasks across different environments, 

we need agents that can propose and pursue rich, complex, and creative goals.
<br>
<br>
<br>
<span class="text-xs">\[Ouedeyer et al., 2007; Colas et al., 2023]</span>

---

# Desiderata for Goal Representations
- Abstraction (abstract goals, abstracting goal components)
- Temporal extension
- Compositionality
- Grounding
<br><br><br>
- These properties likely neither necessary nor sufficient

---

# Surveyed Goal Representation Approaches
<v-clicks depth="2">

- Implicit (directly encoded as reward functions)
- Goal states (e.g. target manipulator positions)
- Image-based observations 
- Natural language:
    - Environment-provided
    - Procedurally generated from minimal grammars
    - Language-based exploration
    - Multimodal models
- Represented as programs? 

</v-clicks>

<!-- <div class="text-xl absolute top-1/2 bg-slate-200 border-2 border-black py-6" v-click>
Prevalent non-language approaches facilitate grounding at the expense of other desiderata
<br><br>
Language (and programs) offer benefits at the cost of grounding complexity
</div> -->
    

---
layout: fact
---

## Key takeaway:
<br>
Prevalent non-language approaches facilitate grounding at the expense of other desiderata
<br><br>
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
# Takeaways
<v-clicks depth="2">

- **Takeaway 1:** We need agents that can propose and pursue rich, complex, and creative goals.
- **Takeaway 2:** This requires richer goal representations and developing methods to ground them.
<br><br>

## Questions

- Where do goals (and their representations) fall on the agent-environment boundary?
- What important desiderata are we missing?
- How do temporally extended goals play with the Markov assumption?
- Can program-based goals scale to diverse environments?
- What can building agents that propose and pursue rich goals teach us about human goal-setting?


</v-clicks>