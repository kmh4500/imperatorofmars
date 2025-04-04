# SoulFiction: Imperator of Mars - A Logic-Driven Narrative World

## 1. Project Overview

This project aims to create a world experienced by a unique character, the **"Imperator of Mars,"** and to unfold that story as a narrative named **"SoulFiction."** What makes this story unique is that its background, the world of Mars, is based on a rigorous **logical world model** constructed using **First-Order Logic (FOL)** and **Situation Calculus (SC)**.

In essence, we are not simply writing a story. First, we leverage a Large Language Model (LLM) to build a **formal world model** that defines the physical laws of Mars, object states, causality of actions, and more. Then, upon this logical foundation, we generate the SoulFiction narrative, ensuring the journey and experiences of the "Imperator of Mars" unfold without contradiction.

**The Ultimate Goal:** To create a logically consistent and dynamic world, explore how the story of the "Imperator of Mars" can develop within that world, and investigate the potential of combining logic and narrative through this process.

## 2. World Model: The Logical Foundation of SoulFiction

The world inhabited by the "Imperator of Mars" is not mere fantasy; it is governed by clear rules and logic. This world model ensures the **consistency** of the SoulFiction narrative, enables **reasoning** about character actions and world changes, and ultimately serves as the **engine for narrative generation**.

### 2.1. Phase 1: Building the Static World (FOL)

* **Methodology:** Using an LLM based on user requirements to define axioms and facts based on First-Order Logic (FOL).
* **Components:**
    * **Constants:** Defining `Mars` (the setting planet), `ImperatorOfMars` (the main character or their proxy), `Perseverance`, `Curiosity` (exploration rovers potentially perceived or used by the Imperator), `OlympusMons`, `JezeroCrater` (key geological features), `WaterIce`, `RockTypeA` (substances and objects), etc.
    * **Predicates:** Defining object types (`IsPlanet`, `IsRover`), states (`IsFrozen`), locations (`LocatedOn`, `LocatedIn`), relationships (`Controls(ImperatorOfMars, Perseverance)`), etc.
    * **Facts:** Specifying unchanging facts at the start of the story, such as `IsPlanet(Mars)`, `LocatedOn(OlympusMons, Mars)`, etc. These form the initial background setting for SoulFiction.

### 2.2. Phase 2: Extending to a Dynamic World (Situation Calculus)

* **Methodology:** Adding Situation Calculus (SC) to the FOL model via LLM to model actions and change.
* **Purpose:** To formally define how the actions of the "Imperator of Mars" or its proxy rovers affect the world, and how states change over time, thereby providing dynamism to the narrative.
* **Core Concepts:**
    * `Situation (s, S0)`: A snapshot of the world state at a specific point in time.
    * `Action (a)`: An act that changes the state (moving, drilling, observing, commanding, etc.).
    * `Fluent (f)`: A property that can change over time (rover location, rock status, Imperator's knowledge state, etc.).
    * `Holds(f, s)`: Fluent `f` is true in situation `s`.
    * `Result(a, s)`: The situation resulting from performing action `a` in situation `s`.
    * `Poss(a, s)`: Action `a` is possible in situation `s`.
* **Defined Fluents (Examples):**
    * `At(object, location)`: Location of an object.
    * `HasSample(rover, sample_id)`: Whether a rover possesses a sample.
    * `IsDrilled(rock)`: Status of a rock being drilled.
    * `IsAnalyzed(sample_id)`: Status of a sample being analyzed.
    * `AwareOf(ImperatorOfMars, fact)`: Imperator's awareness state (potential extension).
* **Defined Actions (Examples):**
    * `Move(rover, location)`: Rover movement.
    * `Drill(rover, rock)`: Drilling a rock.
    * `CollectSample(rover, rock, sample_id)`: Collecting a sample.
    * `Analyze(rover, sample_id)`: Analyzing a sample.
    * `Observe(ImperatorOfMars, object)`: Imperator's act of observation (potential extension).
    * `Command(ImperatorOfMars, rover, action)`: Imperator's act of commanding (potential extension).
* **Core Axioms:**
    * **Initial State Axioms (`Holds(f, S0)`):** Define the state of the world at the beginning (S0) of the SoulFiction story.
    * **Action Precondition Axioms (`Poss(a, s)`):** Define the conditions under which specific actions are possible. This determines the scope of actions the character can take in the story.
    * **Successor State Axioms (`Holds(f, Result(a, s))`):** Define the results of actions, representing the rules (physical laws, causality) of how the world changes. They solve the frame problem to fully describe state transitions.

## 3. SoulFiction: Generating Narrative from Logic

Once the world model is established, the next step is to weave the fabric of **"SoulFiction"** upon this logical skeleton. This is not merely data conversion but a creative process constrained by logical rules.

* **Narrative Engine:** The core component that interprets the logical model and generates the story flow. It works by assessing the current situation (`s`), identifying possible actions (`Poss(a, s)`), selecting the next event (`a` based on plot, goals, etc.), and describing the new situation (`Result(a, s)`) that follows.
* **Mapping Logic to Narrative:**
    * **Constants:** Become characters ("Imperator of Mars," "Perseverance"), settings ("Jezero Crater"), and plot devices ("RockOmega").
    * **Static Predicates:** Provide background descriptions, character introductions, and environmental information, grounding the story. ("Olympus Mons pierced the Martian sky...")
    * **`Holds(Fluent, s)`:** Translates into descriptions of the character's state, emotions (inferentially), or the surrounding environment at a specific moment `s`. ("At moment S0, the Imperator gazed across the Jezero horizon...")
    * **`Poss(Action, s)`:** Used to create suspense, present choices for the character, or foreshadow future events. ("If commanded now, Perseverance could advance towards that unknown rock...")
    * **`Action` & `Result(a, s)`:** Form the core events (plot points) and scene transitions of the story. The process and outcome of actions are vividly described. ("As the Imperator's command registered, Perseverance's drill began to bite into the rock's surface...")
* **Natural Language Generation (NLG):** Transforms logical state changes into human-readable, natural language. Techniques can range from simple templates and synonym dictionaries to more advanced NLG models. **Critically, all generated text must remain consistent with the world model's logic at that point in the narrative.**
* **HTML Output:** Structures the generated narrative (paragraphs, dialogue, descriptions) using appropriate HTML tags (`<p>`, `<blockquote>`, `<em>`, etc.) and styles it with CSS for readability and immersion. Different situations or major events can be demarcated as separate sections (`<div>`, `<section>`) or chapters.

### Conceptual Narrative Example (HTML Snippet)

```html
<div class="chapter" id="situation-S0">
    <h2>Chapter 1: The Commander of the Red Planet</h2>
    <p>Imperator of Mars. On this red planet, where only nameless winds whispered, it was the sole commander. Its consciousness was linked to the exploration rover, Perseverance, traversing the planetary surface. At this moment, Perseverance stood still in the center of Jezero Crater, where traces of an ancient lake lay dormant.</p>
    <p>Within the Imperator's view (relayed through Perseverance), lay an intriguing rock designated 'RockOmega'. The data indicated this rock remained untouched, pristine, within reach of Perseverance's drill, and that drilling was currently possible.</p>
    <blockquote>"A stone holding the secrets of time? Or merely a common fragment of Mars..."</blockquote>
    <p>The Imperator had to make a decision. Command Perseverance to delve into RockOmega, or pursue a different path of exploration. Its choice would turn the next page of the story.</p>
     <div class="actions">
        <button data-action="Command(ImperatorOfMars, Perseverance, Drill(Perseverance, RockOmega))">Order: Drill RockOmega</button>
        <button data-action="Command(ImperatorOfMars, Perseverance, Move(Perseverance, SectorGamma))">Order: Move to Sector Gamma</button>
    </div>
</div>