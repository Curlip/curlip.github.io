# Cursed Guard

![Cursed Guard](/ek/assets/enemies/cursed-guard/sprite@16x.png)

 _“A guard summoned by Oryx during his descent into madness. A poor sole is said to still remain in the flesh of this creature, a sense of empathy may be present.”_

---

An enemy that spawns at the start of the Realm in the mountainous section of the Godlands. It is not a quest and must be searched for. It spawns a set piece consisting of a 3x3 of discolored ground. The Cursed Guard functions similarly to a beer god. 4-6 players must stand around the Guard in order for the Cursed Guard to float out of the ground and begin its phases.

## Stats

**HP**: 100,000 <br />
**DEF**: 60     <br />

Immune to Stasis <br />
Immune to Stun

## Shots

| Projectile | Damage | Effect | Range | Speed <br> (tiles/sec) | Comments |
|:-:|---|---|---|---|---|
|![](/ek/assets/enemies/cursed-guard/shots/paraspray@2.png)| 0 | **Paralyze** for 0.7 Seconds | 5.6 | 15 | **"Radial Paralyze"** <br /> Pierces |
|![](/ek/assets/enemies/cursed-guard/shots/magicspray@2.png) | 175 | - | 15 | 20 | **"Magic Spray"** |
|![](/ek/assets/enemies/cursed-guard/shots/sword@2.png)| 250 | - | 20 | 10 | **"Guard Sword"** <br /><br /> Visually Large |
|![](/ek/assets/enemies/cursed-guard/shots/shield1@2.png)| 125 | - | 13 | 15 | **"Guard Shield"** |
|![](/ek/assets/enemies/cursed-guard/shots/shield2@2.png)| 160 | **Stun** for 3 seconds <br /> **Slow** for 3 Seconds | 14 | 15 | **"Guard Shield B"**

## Phases

The Cursed Guard will take one of two "paths" randomly, these are effectively groups of Phases. This is decided before the event is spawned and effects the amount of players required to raise the Guardian.

### Sleeping Phase

The Guard will sit invisible on the setpiece, when the Enchanted Path is chosen it will take 6 players to raise the Guard. While in the Enraged Path it will only take 4.

### Enchanted Path

In this phase the Guard is said to be "Enchanted" by Oryx, into doing the biding of the Mad God.

#### Raising

The Guard, invulnerable, will rise out of the ground over a period of 10 seconds. During this time it is shooting out a ring of "Radial Paralyzes" every 0.8 seconds. It also fires 10 bombs in a circle with a range of 2 and a radius of 2, these will do 200 damage and fire every second.

After 10 seconds in transitions to the _Turrets Phase_.

#### Turrets

The Cursed Guard, still invulnerable, summons 8 [Guard Turrets](/ek/documents/enemies/guard-turret.html) at a range of 7 around it in a circle. The Guard now becomes vulnerable and the turrets begin the _Protection Phase_, orbiting the Guard while shooting inwards at it.

After 20 seconds the Guard will become invulnerable, and the turrets transition to the _Chase Phase_, in this phase the turrets chase players at incredible speed. After all the Turrets are destroyed the Guard will move into the _Transition Phase_.

#### Transition

The transition phase is a hybrid of damage taking and damage assessment, in this phase there is a chance for easier melee damage, as well as damage all round.

In the Transition Phase the Guard will shoot a ring of "Radial Paralyzes", however this time they only shoot ever 2 seconds. The Guard also fires a 30&deg; spread of "Magic Spray" at the nearest player every second.

If the Guard gets under 15,000 HP in this phase it will transition to the _Rage Phase_, otherwise it will restart the turrets phase.

### Enraged Path

In the Enraged Path the Guard is willingly doing the bidding of the Mad God, trying to crush them personally.

#### Raising

This phase is the sane as that of the _Enchanted Path_. However this time the phase only lasts 5 seconds, this is meant to display energy in the Guard.

#### Turrets

The turrets phase for this path contains a lot more elements, it has both [Guard Turrets](/ek/documents/enemies/guard-turret.html), and well as [Guard Shields](/ek/documents/enemies/guard-shield.html).

The Guard will throw out 8 Turrets at range of 7, and 8 Shields at a range of 2. The shields start in their only phase, the _Orbit Phase_, while the turrets start in there _Chase Phase_. The Guard is invulnerable at this point.

If the Turrets are not dead after 15 seconds all the Guards minions will self terminate and the Guard will begin the phase again. If all the Turrets do die in this time the Guard will transition to the _Chase Phase_.

#### Chase

Any existing Guard Shields will now self terminate, and the Guard becomes vulnerable.

The Guard begins to chase players around with a slow follow speed of 2. It fires the ring "Radial Paralyzes" every 0.8 seconds. It will also shoot a 45&deg; spread of 5 "Guard Shields" every 0.6 seconds.

After 15 seconds the Guard transitions to the _Slashing Phase_.

#### Slashing

Th Guard stands in place and shoots one "Guard Sword" every 0.4 seconds. In this phase it is armored. After 5 seconds it moves to the _Transition Phase_.

#### Transition

The Guard will shoot a ring of "Radial Paralyzes" every 2 seconds. It also shoots a 75&deg; spread of 3 "Guard Shields" every 0.6 seconds.

If the Guard gets under 15,000 HP in this phase it will transition to the _Rage Phase_, otherwise it will restart the chase phase.

### Rage Phase

The Guard becomes invulnerable and flashes red for 3 seconds. After this time it becomes vulnerable and begins shooting a 45&deg; spread of 5 "Guard Shield B's" every 0.4 seconds. It also shoots a "Guard Sword" every 0.4 seconds.

After 10 seconds the Guard glows green and stops shooting. In this phase it is armored. This is intended as time to damage the Guard.

The Guard will be in its rage phase until death.

## Loot

| Bag | Loot |
| :-: | - |
| ![](/ek/assets/rotmg/pbag.png) | ![](/ek/assets/rotmg/4ability.gif) ![](/ek/assets/rotmg/3-4ring.gif) ![](/ek/assets/rotmg/7-9armor.gif) ![](/ek/assets/rotmg/8-9weapon.gif) |
| ![](/ek/assets/rotmg/egg.png) | ![](/ek/assets/rotmg/eggs.gif) |
| ![](/ek/assets/rotmg/cyan.png) | ![](/ek/assets/rotmg/5ability.gif) ![](/ek/assets/rotmg/5ring.gif) ![](/ek/assets/rotmg/10-12armor.gif) ![](/ek/assets/rotmg/10-11weapon.gif) |
| ![](/ek/assets/rotmg/potbag.png) | ![](/ek/assets/rotmg/Stats.gif) |
| ![](/ek/assets/rotmg/whitebag.png) | ![](/ek/assets/items/cursed-mail-of-depths-beneath/droptable.png) |

Also drops portal to "Elemental Kingdom"

## XML

```XML
<Object type="FIX" id="ParaSpray">
        <Class>Projectile</Class>
        <Texture>
            <File>FIX</File>
            <Index>FIX</Index>
        </Texture>
        <Rotation>0</Rotation>
        <Size>100</Size>
</Object>
<Object type="FIX" id="MagicSpray">
        <Class>Projectile</Class>
        <Texture>
            <File>FIX</File>
            <Index>FIX</Index>
        </Texture>
        <Rotation>0</Rotation>
        <Size>100</Size>
        <AngleCorrection>1</AngleCorrection>
</Object>
<Object type="FIX" id="GuardSword">
        <Class>Projectile</Class>
        <Texture>
            <File>FIX</File>
            <Index>FIX</Index>
        </Texture>
        <Rotation>0</Rotation>
        <Size>130</Size>
</Object>
<Object type="FIX" id="GuardShield">
        <Class>Projectile</Class>
        <Texture>
            <File>FIX</File>
            <Index>FIX</Index>
        </Texture>
        <Rotation>0</Rotation>
        <Size>100</Size>
        <AngleCorrection>1</AngleCorrection>
</Object>
<Object type="FIX" id="GuardShieldB">
        <Class>Projectile</Class>
        <Texture>
            <File>FIX</File>
            <Index>FIX</Index>
        </Texture>
        <Rotation>0</Rotation>
        <Size>100</Size>
        <AngleCorrection>1</AngleCorrection>
</Object>

<Object type="FIX" id="Cursed Guard">
    <Group>Cursed Guard Encounter</Group>

    <Enemy/>
    <Class>Character</Class>
    <Hero/>
    <God/>
    <Encounter/>
    <PerRealmMax>1</PerRealmMax>
    <KeepDamageRecord/>

    <StasisImmune/>

    <Size>0</Size>
    <MaxHitPoints>100000</MaxHitPoints>
    <Defense>60</Defense>
    <XpMult>0.3</XpMult>

    <AnimatedTexture>
        <File>FIX</File>
        <Index>FIX</Index>
    </AnimatedTexture>
    <AltTexture id="1">                                                 <!-- Invisble Sprite -->
        <Texture>
            <File>invisible</File>
            <Index>0</Index>
        </Texture>
        <!--invisible-->
    </AltTexture>
    <AltTexture id="2">                                                 <!-- Rising Animation -->
        <AnimatedTexture>
            <File>FIX</File>
            <Index>FIX</Index>
        </AnimatedTexture>
    </AltTexture>

    <!-- Shots -->

    <Projectile id="0">
        <ObjectId>ParaSpray</ObjectId>
        <Damage>0</Damage>
        <Speed>100</Speed>
        <LifetimeMS>560</LifetimeMS>
        <MultiHit />
    </Projectile>
    <Projectile id="1">
        <ObjectId>MagicSpray</ObjectId>
        <Damage>200</Damage>
        <Speed>100</Speed>
        <LifetimeMS>800</LifetimeMS>
        <MultiHit />
    </Projectile>
    <Projectile id="2">
        <ObjectId>GuardDamage</ObjectId>
        <Damage>250</Damage>
        <Speed>200</Speed>
        <LifetimeMS>800</LifetimeMS>
        <MultiHit />
    </Projectile>
    <Projectile id="3">
        <ObjectId>GuardShield</ObjectId>
        <Damage>125</Damage>
        <Speed>150</Speed>
        <LifetimeMS>666</LifetimeMS>
        <MultiHit />
    </Projectile>
    <Projectile id="4">
        <ObjectId>GuardShieldB</ObjectId>
        <Damage>160</Damage>
        <Speed>150</Speed>
        <LifetimeMS>666</LifetimeMS>
        <MultiHit />
        <ConditionEffect duration="3">Stun</ConditionEffect>
        <ConditionEffect duration="3">Slow</ConditionEffect>
    </Projectile>

    <Behavior map="guard/guardEncounter.jm">PlaceMap</Behavior>
    <Behavior>OryxTaunt</Behavior>

    <!-- Decide Path -->
    <State id="Ini">
        <Behavior altTextureId="1">SetAltTexture</Behavior>
        <Transition random="1">pathAngry,pathCalm</Transition>
    </State>

    <State id="pathCalm">
        <State id="wait">
            <Transition playerWithin="6" aftertime="1">raise</Transition>
        </State>
        <State id="raise">
            <Behavior maxSize="140" rate="14">ChangeSize</Behavior>
            <Behavior altTextureId="2">SetAltTexture</Behavior>
            <Behavior effect="Invulnerable">ConditionEffect</Behavior>
            <Embed name="radialBombs"></Embed>
            <Embed name="radialPara">
                <Param name="cooldown">0.8</Param>
            </Embed>
            <Transition afterTime="10">throwTurrets</Transition>
        </State>
        <State id="throwTurrets">
            <Behavior effect="Invulnerable">ConditionEffect</Behavior>
            <Embed name="throwMinions"></Embed>
            <Transition exist="Guard Turret">Turrets</Transition>
        </State>
        <State id="Turrets">
            <Order>
                <Transition>inwardShoot</Transition>
            </Order>
            <Transition afterTime="20">TurretChase</Transition>
        </State>
        <State id="Turret Chase">
            <Order>
                <Transition>chase</Transition>
            </Order>
            <Behavior effect="Invulnerable">ConditionEffect</Behavior>
            <Transition noneExist="Guard Turret">transition</Transition>
        </State>
        <State id="transition">
            <Embed name="radialPara">
                <Param name="cooldown">2</Param>
            </Embed>
            <Behavior type="targeted" numShots="3" projectileId="1" cooldown="1" angle="10">Shoot</Behavior>
            <Transition hitpointsLessThan="0.15">rage</Transition>
            <Transition afterTime="10">throwTurrets</Transition>
        </State>
    </State>

    <State id="pathAngry">
        <State id="wait">
            <Transition playerWithin="4" aftertime="1">raise</Transition>
        </State>
        <State id="raise">
            <Behavior maxSize="140" rate="28">ChangeSize</Behavior>
            <Behavior altTextureId="2">SetAltTexture</Behavior>
            <Behavior effect="Invulnerable">ConditionEffect</Behavior>
            <Embed name="radialBombs"></Embed>
            <Embed name="radialPara"></Embed>
            <Transition afterTime="5">throwTurrets</Transition>
        </State>
        <State id="throwTurrets">
            <Behavior effect="Invulnerable">ConditionEffect</Behavior>
            <Embed name="throwMinions"></Embed>
            <Embed name="throwShields"></Embed>
            <Transition exist="Guard Turret,Guard Shield">Turrets</Transition>
        </State>
        <State id="Turrets">
            <Order targetIds="Guard Turret">
                <Transition>chase</Transition>
            </Order>
            <Order targetIds="Guard Shield">
                <Transition>orbit</Transition>
            </Order>
            <Behavior effect="Invulnerable">ConditionEffect</Behavior>
            <Transition afterTime="15">respawnTurrets</Transition>
            <Transition noneExist="Guard Turrets">chase</Transition>
        </State>
        <State id="respawnTurrets">
            <Order>
                <Transition>terminate</Transition>
            </Order>
            <Transition>Turrets</Transition>
        </State>
        <State id="chase">
            <Order>
                <Transition>terminate</Transition>
            </Order>
            <Embed name="radialPara">
                <Param name="cooldown">0.8</Param>
            </Embed>
            <Behavior type="targeted" numShots="5" projectileId="3" cooldown="0.6" angle="9">Shoot</Behavior>
            <Behavior acquireRange="20" bucket="movement" speed="2">Follow</Behavior>
            <Transition afterTime="15">slashing</Transition>
        </State>
        <State name="slashing">
            <Behavior effect="Armored">ConditionEffect</Behavior>
            <Behavior type="targeted" numShots="1" projectileId="2" cooldown="0.4">Shoot</Behavior>
            <Transition afterTime="5">transition</Transition>
        </State>
        <State id="transition">
            <Embed name="radialPara">
                <Param name="cooldown">2</Param>
            </Embed>
            <Behavior type="targeted" numShots="3" projectileId="3" cooldown="0.6" angle="25">Shoot</Behavior>
            <Embed name="radialBombs"></Embed>
            <Transition hitpointsLessThan="0.15">rage</Transition>
            <Transition afterTime="10">chase</Transition>
        </State>
    </State>

    <State id="rage">
        <State name="glow">
            <Behavior effect="Invulnerable">ConditionEffect</Behavior>
            <Behavior type="Flash" color="FF2200" flashPeriod="3" flashRepeats="1">ShowEffect</Behavior>
            <Transition afterTime="3">shoot</Transition>
        </State>
        <State id="shoot">
            <Behavior type="targeted" numShots="5" projectileId="4" cooldown="0.4" angle="9">Shoot</Behavior>
            <Behavior type="targeted" numShots="1" projectileId="2" cooldown="0.4">Shoot</Behavior>
            <Transition afterTime="10">safe</Transition>
        </State>
        <State id="safe">
            <Behavior type="Flash" color="00FF22" flashPeriod="2" flashRepeats="2">ShowEffect</Behavior>
            <Behavior effect="Armored">ConditionEffect</Behavior>
            <Transition afterTime="5">glow</Transition>
        </State>
    </State>

    <DefineEmbed name="radialBombs">
        <Behavior target="auto" defaultAngle="0" range="2" cooldown="1" damage="200" radius="2">GrenadeToss</Behavior>
        <Behavior target="auto" defaultAngle="36" range="2" cooldown="1" damage="200" radius="2">GrenadeToss</Behavior>
        <Behavior target="auto" defaultAngle="72" range="2" cooldown="1" damage="200" radius="2">GrenadeToss</Behavior>
        <Behavior target="auto" defaultAngle="108" range="2" cooldown="1" damage="200" radius="2">GrenadeToss</Behavior>
        <Behavior target="auto" defaultAngle="144" range="2" cooldown="1" damage="200" radius="2">GrenadeToss</Behavior>
        <Behavior target="auto" defaultAngle="180" range="2" cooldown="1" damage="200" radius="2">GrenadeToss</Behavior>
        <Behavior target="auto" defaultAngle="216" range="2" cooldown="1" damage="200" radius="2">GrenadeToss</Behavior>
        <Behavior target="auto" defaultAngle="252" range="2" cooldown="1" damage="200" radius="2">GrenadeToss</Behavior>
        <Behavior target="auto" defaultAngle="288" range="2" cooldown="1" damage="200" radius="2">GrenadeToss</Behavior>
        <Behavior target="auto" defaultAngle="324" range="2" cooldown="1" damage="200" radius="2">GrenadeToss</Behavior>
    </DefineEmbed>

    <DefineEmbed name="radialPara">
        <Behavior type="auto" numShots="36"  projectileId="0" cooldown="{cooldown}" angle="10">Shoot</Behavior>
    </DefineEmbed>

    <DefineEmbed name="throwMinions">
        <Behavior type="auto" childId="Guard Turret" range="7" defaultAngle="0">ObjectToss</Behavior>
        <Behavior type="auto" childId="Guard Turret" range="7" defaultAngle="90">ObjectToss</Behavior>
        <Behavior type="auto" childId="Guard Turret" range="7" defaultAngle="180">ObjectToss</Behavior>
        <Behavior type="auto" childId="Guard Turret" range="7" defaultAngle="270">ObjectToss</Behavior>
        <Behavior type="auto" childId="Guard Turret" range="7" defaultAngle="45">ObjectToss</Behavior>
        <Behavior type="auto" childId="Guard Turret" range="7" defaultAngle="135">ObjectToss</Behavior>
        <Behavior type="auto" childId="Guard Turret" range="7" defaultAngle="315">ObjectToss</Behavior>
        <Behavior type="auto" childId="Guard Turret" range="7" defaultAngle="225">ObjectToss</Behavior>
    </DefineEmbed>

    <DefineEmbed name="throwShields">
        <Behavior type="auto" childId="Guard Shield" range="2" defaultAngle="0">ObjectToss</Behavior>
        <Behavior type="auto" childId="Guard Shield" range="2" defaultAngle="90">ObjectToss</Behavior>
        <Behavior type="auto" childId="Guard Shield" range="2" defaultAngle="180">ObjectToss</Behavior>
        <Behavior type="auto" childId="Guard Shield" range="2" defaultAngle="270">ObjectToss</Behavior>
        <Behavior type="auto" childId="Guard Shield" range="2" defaultAngle="45">ObjectToss</Behavior>
        <Behavior type="auto" childId="Guard Shield" range="2" defaultAngle="135">ObjectToss</Behavior>
        <Behavior type="auto" childId="Guard Shield" range="2" defaultAngle="315">ObjectToss</Behavior>
        <Behavior type="auto" childId="Guard Shield" range="2" defaultAngle="225">ObjectToss</Behavior>
    </DefineEmbed>
</Object>
```

## Thanks

Thankyou to anyone on the [Ideas Discord](https://discord.gg/7Kjm25c) who looked at sprites, or who helped with some concepts or numbers.
