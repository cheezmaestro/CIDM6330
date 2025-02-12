# Military Aviation Improved Maintenance System - MAIMS
An exploration of several improvements to existing systems; because the military loves documentation almost as much as it loves bad acronyms.

West Texas A&M  
CIDM 6330 - Spring 2025  
By Ryan Anderson
<div style="page-break-after: always; visibility: hidden"> 
\pagebreak 
</div>

# Introduction
In the world of military aviation maintenance documentation there have been very few advances over the past 40 or so years.
The records of this documentation are maintained in several large systems which have emerged over the years.
These systems are immense, both in cost and footprint. The purpose of this design is to imagine a system that attempts to improve the affordability, simplicity (maintainability),
and user experience (UX) of legacy systems.

As such, the primary focus will be to explore the underlying architecture which would enable these improvements.
That is to say, the focus will not be on perfectly matching data structure exactly to United States Air Force (USAF) technical
requirements except where it is necessary to consider them in system design (organizational structure being a prime example).

Furthermore, as this is simply an academic exercise, it will not attempt to capture the breadth and depth of functions
legacy systems are required to support. The scale of functions, use cases, physical locations, & users supported by legacy systems
is astounding. The features chosen for this exercise are what can be considered the core discipline of aircraft maintenance documentation, namely;
discrepancy discovery, removal, repair, & replacement of parts.

The end goal is a hybrid web application, built on opensource components, which can support mobile as well as desktop usage.

<div style="page-break-after: always; visibility: hidden"> 
\pagebreak 
</div>

# Table of Contents

1. Requirement Statements
    1. User Stories
    2. Use Cases
    3. Features
    4. Gherkin Validation

2. Specifications
    1. Concepts
    2. UX Notes
    3. Interfaces (Controls)
    4. Behaviors

<div style="page-break-after: always; visibility: hidden"> 
\pagebreak 
</div>

# Requirement Statements

## User Stories
*Coming soon*

## Use Cases
### Use Case 1 – On-Equipment Repair w/Stock
An aircraft technician notices a flat tire on an aircraft (acft) while doing a pre-flight
inspection. They need to replace the wheel assembly with a good one from the
backshop.

**Actors:** Flightline technician  
**Goal:** Generate an on-equipment job against the aircraft, document the configuration change (wheel assembly removed/installed), generate a repair job for the backshop.  

**Process:**  
***Physically***, they must remove the wheel assembly, turn in the damaged assembly to the Wheel
and Tire (W&amp;T) shop, retrieve a serviceable assembly at the wheel and tire shop, and install this
serviceable assembly on the acft. Concurrently, they must document the job, their actions, the
part &amp; serial numbers of the assemblies being removed/replaced (R2) in paper forms (AFTO
349 &amp; AFTO 350). AFTO 350 accompanies the unserviceable part back to W&amp;T shop.  
***Electronically***, they must create a job to document the discrepancy (flat tire), document the R2
part numbers &amp; serial numbers on the acft, and generate a job for the wheel &amp; tire shop for the
repair of the unserviceable assembly. The job is closed once finished.

### Use Case 2 – Off-Equipment Repair w/Stock
A W&amp;T shop technician receives an unserviceable wheel assembly from the flightline and
trades it for a serviceable assembly from their stock. The backshop then repairs the
unserviceable assembly and puts it back in stock.

**Actors:** Backshop technician  
**Goal:** Receive a repair job, receive unserviceable part into shop inventory, document the repair (tire removal/replacement with in-shop replacement tire),
 & return part to serviceable status in shop inventory.  

**Process:**  
***Physically***, they receive wheel assembly and document it in their logbook. They give the
flightline a serviceable assembly and also document that in their logbook. The technician tears
down the unserviceable assembly and replaces the rubber tire with a new one. The assembly is
rebuilt and the now serviceable assembly is placed in shop stock. The AFTO 350 tag that
accompanied the unserviceable part is documented with the job number and details of the
repair.  
***Electronically***, the technician finds the “off equipment” job that was “cut” to them from the
flightline job. They document the repair and close the job.

### Use Case 3 – On-Equipment Repair w/out Stock
Pilot has reported a fault with their radar system. Flightline avionics removes a panel to
access and remove a line replaceable unit (LRU). This LRU is taken to the backshop for
troubleshooting. No replacements are on-station and so a replacement has to be ordered
through supply.

**Actors:** Flightline technician  
**Goal:** Flightline receives a job, documents configuration change on acft (panel access, removal of LRU), 
checks available stock on site, orders replacement LRU from supply, & turns in unserviceable LRU to backshop (along with a backshop job).

**Process:**  
***Physically***, the technicians are made aware of the problem by debrief (post-flight operations)
and are dispatched to look at the acft. They remove the appropriate panel and LRU and take it
to the backshop for testing. Unfortunately, there are no spare LRUs for this system so they
close the panel and document their work, concurrently, on AFTO 349 &amp; 350 forms.

***Electronically***, they receive a job number from debrief that describes the fault. They document
the opening of the panel and removal of the LRU. They cut a job for the backshop against the
unserviceable LRU. They query the on-station stock and find there are no replacement LRUs
available. They then place an order with supply against their job for a replacement LRU. They
leave the job open awaiting arrival of the replacement.

### Use Case 4 – Off-Equipment Repair w/out Stock
Unserviceable LRU is delivered to avionics backshop. The internal components are
found to be damaged. No spare components are available so they must be placed on
order from supply.

**Actors:** Backshop technician  
**Goal:** Receive a job, receive unserviceable LRU, document test & inspection, check available stock, order replacement parts.

**Process:**  
***Physically***, the technicians open the LRU to inspect it. They find burnt cards and blown
capacitors. They check their shop stock and find no spare cards. They fill out an order form to
supply for replacement cards. They document this on their AFTO 350 and set the LRU aside
awaiting delivery from supply.

***Electronically***, they receive the off-equipment job that was cut by the flightline. They document
their inspection and findings on this job. They create an order to supply for the replacement
cards (this order number is put on the AFTO 350) and attach this to the job. Leave job open
awaiting arrival of parts.

### Use Case Diagram


## Features
*coming soon*

## Gherkin Validation
*coming soon*

<div style="page-break-after: always; visibility: hidden"> 
\pagebreak 
</div>

# Specifications

## Concepts
*coming soon*

## UX Notes
*coming soon*

## Interfaces (Controls)
*coming soon*

## Behaviors
*coming soon*

### Feature X

### Feature Y..