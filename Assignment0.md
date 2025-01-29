# Assignment 0
*Ryan Anderson - WTAMU - CIDM 6330*

## Problem
I work in the military aircraft sustainment world supporting maintenance and logistics information systems. In this world there are a few heavy-weight software suites which are used by different partners around the world but each of them fall short in at least one of the following key ways.
1. **High infrastructure/admin burden**  
*Usually the result of overengineering with 20+ year old technology or a sprawling, overcomplicated code base*
2. **Use highly expensive software licenses**  
*Having maintained the yearly budget for just a small implementation of one of these, the cost of licenses alone is staggering*
3. **Data structure doesn't allow multiple organizations or disconnected operations on the same database**  
*Cloud/centralized processing for multiple units and asynchronous operations impossible due to database design*
4. **Do not align with U.S. Air Force (USAF) documentation requirements**  
*Obviously not all customers require this but many Foreign Military Sale (FMS) contracts are expected to emulate U.S. standards*
5. **Have no mobile device capability**  
*A fringe case where a military would authorize mobile device usage but there are customers who do allow this and, if implemented correctly, would greatly enhance the experience of the technicians using the system*

There are some great systems out there but none which solves all of these issues.

## Domain
The domain this problem exists is the insular world of military aviation. In particular, the maintenance, documentation, and logistics tracking systems used in the U.S. military and its foreign partners.

## Personal/Professional Interest
As an analyst and systems administrator in this space my whole career, I have a deep vested interest in exploring ways to make things better for administrators like myself, end users, & customers of these systems.

## System for Prototype
My proposed prototype, which should better help me understand the problems faced in this domain is this:
* A simple web application with these features
    * LAMP (but in Python & Postgresql - as open source as possible) architecture
    * Organization data structure which allows multi-site operations with a shared dataset & no chance of duplication (key to the next component)
    * A simple mobile app for recording maintenance information/events  
        Asynchronous operation (stores data and syncs when connection is returned)

Instead of trying to address all of the multitude of issues plaguing these systems, I think that my prototype intends to focus on the three areas most in need of attention, namely: affordability, simplicity, & user experience.

Affordability could be addressed by using as much open source software as possible, thus lowering licensing costs. Simplicity can be improved through better data structure and more modern web application design (we're not in the 90's anymore!). User experience, my end goal, can be improved by finding ways of getting data generation into the hands (literally) of the technicians at the point of work.