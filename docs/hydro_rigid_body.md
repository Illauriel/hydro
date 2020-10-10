HydroRigidBody
==============

Brief Description
-----------------

A RigidBody with buoyancy and other related forces when it is inside a `WaterArea` .

Description
-----------

When an object enters the water, three forces will be calculated:

**Buoyancy** - the pressure of the displaced  water causes an object to float.

**Drag** - an object moving through the water will slow down.  The amount of drag is dependent on the object's shape.

**Lift** - an object moving through the water at an angle will generate lift, the way a boat lifts out of the water.  This is also dependent on the object's shape.

The HydroRigidBody will expect one mesh to be a direct child.  This mesh will be the only one used to calculate the buoyancy and related forces. This mesh may be concave, but it must be closed and not intersect itself.  Buoyancy is related to volume, and an open shape does not have a volume. If you have other meshes that you want to be part of the HydroRigidBody but not involved with the hull calcuations, place them as a child of the main one.