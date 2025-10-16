---
layout: post
title: "Building Our First Autonomous Program"
date: 2025-10-15
category: Programming
author: "Programming Team"
tags: [Python, PID Control, Autonomous, Programming]
excerpt: "Today we reached a major milestone - our robot successfully completed its first autonomous mission! Here's how we did it."
---

Today we reached a major milestone - our robot successfully completed its first autonomous mission! Here's how we did it.

## The Challenge

We needed to drive the robot straight for 24 inches, turn 90 degrees, and push a mission model. Sounds simple, but getting it accurate was harder than we thought!

## Our Solution: PID Control

We learned about PID (Proportional-Integral-Derivative) control from online tutorials and decided to implement it for steering correction. Think of it like riding a bike:

- **Proportional:** The harder you're drifting, the more you correct
- **Integral:** If you've been drifting for a while, correct even more
- **Derivative:** If you're correcting too fast, slow down the correction

## The Code

We wrote our driving function in Python using the SPIKE Prime API. Our `drive_straight_precise()` function uses motor encoders to track distance and the gyro sensor to maintain heading.

```python
async def drive_straight_precise(self, distance_inches, direction, speed):
    # Reset PID controller
    self.pid.reset()
    
    # Calculate target motor degrees
    target_degrees = self._inches_to_degrees(distance_inches)
    
    # Main control loop
    while current_position < target_degrees:
        # Read sensors
        current_heading = self.get_gyro_heading()
        
        # Calculate steering correction using PID
        error = target_heading - current_heading
        steering = self.pid.calculate(error)
        
        # Apply to motors
        motor_pair.move_tank(self.motor_pair, 
                            speed + steering, 
                            speed - steering)
```

## What We Learned

- PID tuning takes patience - our first values made the robot zigzag!
- Motor encoders are more accurate than time-based movements
- Testing on different battery levels is crucial
- Small adjustments make a big difference

## Next Steps

Now that we have accurate driving, we're working on more complex missions that require precision attachments and multiple movements. Stay tuned!

## Team Reflection

This was a huge learning experience for all of us. Our programmers spent countless hours debugging, and the whole team pitched in with testing. It's amazing to see our code come to life on the robot!

