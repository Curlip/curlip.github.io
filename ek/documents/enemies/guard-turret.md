# Guard Turret

![](/ek/assets/enemies/guard-turret/sprite@8x.png)

Minions of the [Cursed Guard](/ek/documents/enemies/cursed-guard.html), a strike from them seems to cause a once valiant warrior to lose all strength.

## Stats

**HP**: 5,000
**DEF**: 10

Immune to Stasis

## Shots

| Projectile | Damage | Effect | Range | Speed <br> (tiles/sec) | Comments |
|:-:|---|---|---|---|---|
| ![](/ek/assets/enemies/guard-turret/shots/shot@8x.png) | 70 | Weak for 3 seconds | 7 | 5 | **"Turret Shot"** |
| ![](/ek/assets/enemies/guard-turret/shots/shot@8x.png) | 90 | Weak for 3 seconds | 7 | 5 | **"Turret Shot B"** |

## Phases

### Protection

The Turrets will circle the Cursed Guard and shoot their "Turret Shot" inwards at the Guard every 0.2 seconds. In this phase they are invulnerable to serve as a hindrance to anyone attempting to hit the boss.

### Chase

In this phase the turrets will chase any player within 20 tiles at an incredible speed of 20 tiles per second, only the fastest of characters will be able to outrun them. In this phase they shoot a "Turret Shot B" at the nearest player predictively, every 0.4 seconds.

## XML

```XML
<Object type="FIX" id="TurrentShot">
        <Class>Projectile</Class>
        <Texture>
            <File>FIX</File>
            <Index>FIX</Index>
        </Texture>
        <Rotation>0</Rotation>
        <Size>100</Size>
</Object>

<Object type="FIX" id="Guard Turrent">
    <Group>Cursed Guard Encounter</Group>

    <Enemy/>
    <Class>Character</Class>
    <StasisImmune/>

    <MaxHitPoints>5000</MaxHitPoints>
    <Defense>10</Defense>

    <AnimatedTexture>
        <File>FIX</File>
        <Index>FIX</Index>
    </AnimatedTexture>

    <!-- Shots -->

    <Projectile id="0">
        <ObjectId>TurrentShot</ObjectId>
        <Damage>70</Damage>
        <Speed>50</Speed>
        <LifetimeMS>1400</LifetimeMS>
        <MultiHit />
        <ConditionEffect duration="3">Weak</ConditionEffect>
    </Projectile>
    <Projectile id="1">
        <ObjectId>TurrentShot</ObjectId>
        <Damage>90</Damage>
        <Speed>100</Speed>
        <LifetimeMS>500</LifetimeMS>
        <MultiHit />
        <ConditionEffect duration="3">Weak</ConditionEffect>
    </Projectile>

    <Behavior bucket="orders" listenIds="Cursed Guard">FollowOrders</Behavior>

    <State id="Ini"></State>
    <State id="inwardShoot">
        <Behavior effect="Invulnerable">ConditionEffect</Behavior>
        <Behavior bucket="movement" protecteeId="Cursed Guard" acquireRange="20" speed=".4" radius="7" speedVariability="0" radiusVariability="0">Orbit</Behavior>
        <Behavior type="forward" numShots="1"  projectileId="0" cooldown="0.2" defaultAngle="90">Shoot</Behavior>
    </State>
    <State id="chase">
        <Behavior acquireRange="20" bucket="movement" speed="4">Follow</Behavior>
        <Behavior type="target" numShots="1" projectileId="1" cooldown=".4" predictive="0.6">Shoot</Behavior>
    </State>
    <State id="terminate">
        <Behaviour>Decay</Behaviour>
    </State>
</Object>
```
