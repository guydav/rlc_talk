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

<v-click at="+2"><li>These goals help us learn how to search and solve problems
<span class="text-xs">[Chu & Schulz, 2020; Chu et al., 2024]</span></li></v-click>
</ul>
</div> 
</div>     

<div>
    <div class="flex flex-row justify-center">
        <figure class="image is-square is-inline-block">
            <v-click at="[10, 11]"><img src="/images/logan_truck.jpg" width="160"></v-click>
        </figure>
        <figure class="image is-square is-inline-block">
            <v-click at="[11, 12]"><video width="240"controls>
                <source src="/videos/jordan_bird_trimmed.mp4" type="video/mp4">
            </video></v-click>
        </figure>
    </div>
</div>

</div>



<v-click at="+1"><h3></h3></v-click>
<div class="ns-c-tight">
<v-clicks at="+2">



</v-clicks>
</div>


<!-- ::left::

- Specifying goals as intended behaviors:

:::right:::

- Children's ability to propose goals in play.  -->