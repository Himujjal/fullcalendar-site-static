---
title: View Object
type: guide
---

A View object contains information about a calendar view, such as title and date range. This information about the current view is passed into nearly every [handler](handlers).


## Properties

`type`
:   Name of one of the available views (a string).

`title`
:   Title text that is displayed at the top of the header (such as "September 2009" or "Sep 7 - 13 2009").

`activeStart`
:   A [Date](date-object) that is the first visible day.
    In month view, this value is often before the 1st day of the month, because most months do not begin on the first day-of-week.

`activeEnd`
:   A [Date](date-object) that is the exclusive last visible day.

`currentStart`
:   A [Date](date-object) that is the start of the interval the view is trying to represent.
    For example, in month view, this will be the first of the month. This value disregards hidden days.

`currentEnd`
:   A [Date](date-object) that is the exclusive end of the interval the view is trying to represent.
    For example, in month view, this will be the day after the last day of the month (because it is exclusive).
    This value disregards hidden days.

These properties of the View object can only be read. A [custom view with settings](custom-view-with-settings) is the way to set any of them.
