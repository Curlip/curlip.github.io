# Guard Shield

![](/ek/assets/enemies/guard-shield/sprite@8x.png)

A shield used by the [Cursed Guard](/ek/documents/enemies/cursed-guard.html) as protection. The physical embodiment of dark enchantments, the power that formed them seems to come from something, or someone, of much more power than their master.

## Stats:

**HP**: 5,000
**DEF**: 10

## Shots

| Projectile | Damage | Effect | Range | Speed <br> (tiles/sec) | Comments |
|:-:|---|---|---|---|---|
| Invisible | 100 | - | 0 | 0 | Doesn't Move <br> Pierces Players |

## Phases

### Orbit

The only phase of the Guard Shield, in this phase the Shields circle the Guard at a range of 2 tiles. They will also shoot there shot every second in order to stop people walking over them.

## XML

```XML
<Object type="FIX" id="Invi">
        <Class>Projectile</Class>
        <Texture>
            <File>Invisible</File>
            <Index>0x00</Index>
        </Texture>
        <Rotation>0</Rotation>
        <Size>100</Size>
</Object>

<Object type="FIX" id="Guard Shield">
    <Group>Cursed Guard Encounter</Group>

    <Enemy/>
    <Class>Character</Class>
    <StasisImmune/>

    <MaxHitPoints>5000</MaxHitPoints>
    <Defense>10</Defense>

    <AnimatedTexture>
        <File>curlip8</File>
        <Index>0x02</Index>
    </AnimatedTexture>

    <!-- Shots -->

    <Projectile id="0">
        <ObjectId>Invi</ObjectId>
        <Damage>100</Damage>
        <Speed>0</Speed>
        <LifetimeMS>400</LifetimeMS>
        <MultiHit />
    </Projectile>

    <Behavior bucket="orders" listenIds="Cursed Guard">FollowOrders</Behavior>

    <State id="Ini"></State>
    <State id="orbit">
        <Behavior bucket="movement" protecteeId="Cursed Guard" acquireRange="20" speed=".4" radius="2" speedVariability="0" radiusVariability="0">Orbit</Behavior>
        <Behavior type="auto" numShots="1"  projectileId="0" cooldown="1" defaultAngle="0">Shoot</Behavior>
    </State>
    <State id="terminate">
        <Behaviour>Decay</Behaviour>
    </State>
</Object>
```
