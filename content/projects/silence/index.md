---
title: "Silence"
date: 2023-07-01T21:13:41+02:00
draft: false
---


{{< lead >}}
Together with a friend, take on the role of an agent and a hacker who must stop a military company from launching a dangerous combat robot.
{{< /lead >}}

## Overview

**Silence** is a cooperative stealth game created over the span of 4 months by a team of 6 students from the [FTIMS](https://ftims.p.lodz.pl/en) university.

It was made for the ZTGK 2023 contest and got to **TOP 3** in the Game Development category.

It was also awarded by the **11 bit studios** company.

{{< video src="animations.webm" type="video/webm" preload="auto" controls="1" loop="1">}}

The gameplay is focued on cooperation between the two players.
As agent, you have to sneak around the map, avoiding the guards and activating the switches.
As hacker, you have to help the agent by distracting the guards and hacking the security cameras.
Because of the assymetry between the abilities of the two players, it's crucial that they communicate and cooperate with each other.

You can download the game on [itch.io]("https://cladur.itch.io/silence") or check the source code on [GitHub]("https://github.com/cladur/silence).

## Development

### Art

#### Assets

All the assets - models, textures and animations were created single-handedly by Agata Granosik.
They were made using Blender and Substance Painter, and then later imported into the game using our own custom tools.
The game's artstyle was designed to be realistic, yet a bit stylized.
Textures were created using the PBR workflow.

{{< gallery >}}
  <img src="assets/12.png" class="grid-w33" />
  <img src="assets/16.png" class="grid-w33" />
  <img src="assets/17.png" class="grid-w33" />
  <img src="assets/32.png" class="grid-w33" />
  <img src="assets/03.png" class="grid-w33" />
  <img src="assets/04.png" class="grid-w33" />
  <img src="assets/05.png" class="grid-w33" />
  <img src="assets/07.png" class="grid-w33" />
  <img src="assets/08.png" class="grid-w33" />
  <img src="assets/09.png" class="grid-w33" />
  <img src="assets/10.png" class="grid-w33" />
  <img src="assets/13.png" class="grid-w33" />
  <img src="assets/14.png" class="grid-w33" />
  <img src="assets/15.png" class="grid-w33" />
  <img src="assets/19.png" class="grid-w33" />
  <img src="assets/20.png" class="grid-w33" />
  <img src="assets/22.png" class="grid-w33" />
  <img src="assets/23.png" class="grid-w33" />
  <img src="assets/24.png" class="grid-w33" />
  <img src="assets/25.png" class="grid-w33" />
  <img src="assets/26.png" class="grid-w33" />
  <img src="assets/27.png" class="grid-w33" />
  <img src="assets/28.png" class="grid-w33" />
  <img src="assets/30.png" class="grid-w33" />
  <img src="assets/31.png" class="grid-w33" />
{{< /gallery >}}

#### Music and Sounds

### Renderer

#### PBR Renderer with Deferred Shading

The renderer is based on the Physically Based Rendering model.
It uses a deferred shading technique to render the scene in multiple passes.
Because of that, our engine is capable of rendering hundreds of lights without any performance issues.

{{< figure src="effects/deferred3.png" title="Deferred Lights" >}}

Pictured above is the tutorial scene with all the lights visualized.

<!-- Due to the lack of light baking, we "emulated" light bouncing through the scene by placing multiple light sources in the place of a single actual light source.
On the picture above, you can see each light having 3 different "shapes".
There's a spot light, which is the main source of light, a large point light, which is used to simulate light bouncing off the environment, and a small point light placed near the light source, which is used illuminate the lamp and give it the bloom effect. -->

#### Volumetric Lights

The renderer supports volumetric lights, which are used to create a more climatic atmosphere.
They are computed based on the light's shadow map and raymarching.

{{< video src="videos/volumetric.webm" type="video/webm" preload="auto" autoplay="1" controls="" loop="1" muted="1">}}

#### Bloom

The renderer also supports a bloom effect, which is used to create a more realistic lighting.

{{< video src="videos/bloom.webm" type="video/webm" preload="auto" autoplay="1" controls="" loop="1" muted="1">}}

#### SSAO

{{< video src="videos/ssao.webm" type="video/webm" preload="auto" autoplay="1" controls="" loop="1" muted="1">}}

#### SSR

{{< video src="videos/ssr.webm" type="video/webm" preload="auto" autoplay="1" controls="" loop="1" muted="1">}}

{{< video src="videos/ssr2.webm" type="video/webm" preload="auto" autoplay="1" controls="" loop="1" muted="1">}}


#### Decals

{{< video src="videos/decals.webm" type="video/webm" preload="auto" autoplay="1" controls="" loop="1" muted="1">}}

#### Particles

{{< video src="videos/particles.webm" type="video/webm" preload="auto" autoplay="1" controls="" loop="1" muted="1">}}

### Editor

#### Mouse Picker and Gizmos

#### Prefabs

#### Scene Hierarchy

#### Inspector

#### Content Browser

### Engine

#### Asset Baker

#### ECS

#### CVars
