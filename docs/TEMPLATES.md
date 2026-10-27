# TEMPLATES — approval sheets

Use these for every proposal so the owner reviews the same fields every time.

## Move spec sheet
```
Move:            <name>                 Character: <id>        Status: PROPOSED
Input:           <action slot> (PC / touch / gamepad)
Function:        <what it does, in one or two sentences>
Range / hitbox:  <shape, size in studs, offset, per active window>
Startup:         <frames @60fps> (<ms>)
Active:          <frames> (<ms>), hits: <n>
Recovery:        <frames> (<ms>)    On block: <+/- frames>
Cooldown:        <s>        Cost: <energy / meter>     Meter gain: <on hit / on block>
Damage:          <per hit / total>   Combo scaling: <applies / exempt>
Hitstun:         <frames>            Block stun: <frames>
Knockback:       <type: none / push / launch / slam / wall-bounce>, <vector, studs/s>
Properties:      <super-armour frames, i-frames, guard-break, unblockable, projectile>
Cancels:         <into / from>
Counterplay:     <how the opponent beats, avoids or punishes it>
Animation:       <keyframe beats: anticipation → strike → follow-through → recovery>
VFX:             <trail, slash arc, impact, particles, colours>
Audio:           <swing, impact, voice>
Camera:          <shake strength, hitstop ms, any camera move>
```

## Animation / VFX / cinematic proposal
```
Name / context:   <move or event>                        Status: PROPOSED
Beat sheet:       t=0.00 <pose / action> · t=0.12 <...> · ...
Camera:           <framing, motion, FOV, duration, who sees it>
Particles/trails: <emitters, colours, lifetime, counts per quality tier>
Impact frames:    <hitstop ms, flash or invert frame, screen effects>
Sound cues:       <timestamps and descriptions>
Performance:      <particle cap, mobile tier fallback>
Production needs: <animations to author, textures or meshes to upload, owner input>
```

## Map phase sign-off
```
Phase: <pre-build package / greybox / art / lighting / perf>     Status: PROPOSED
Deliverables:     <links to SVG layout, screenshots from owner, specs>
References used:  <REF-xxx ...>
Open questions:   <...>
```
