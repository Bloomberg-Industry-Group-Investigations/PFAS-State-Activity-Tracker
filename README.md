# Bloomberg Industry Group Investigations PFAS State Activity Tracker

***WARNING: This tracker is no longer being updated and should not be considered up-to-date. The tracker may not reflect current laws or regulations. It is being maintained in its current state as a reference.***

## Terms of Use

By downloading the Dataset, you agree that you will attribute the Dataset and any use of the Dataset to Bloomberg Law. You may use the Dataset for personal or internal business purposes, and may make limited use of the Dataset in connection with the provision of other services to clients; provided that you may not monetize the Dataset or otherwise make commercial use of the Dataset where the Dataset constitutes all, or substantially all, of the commercial offering. The Dataset is provided "as-is" and without any express or implied warranties.

## Introduction

This repository contains the database that makes up the PFAS State Activity Tracker. The tracker contains legislative and regulatory actions on PFAS that are happening at the state level. Proposed, pending, and enacted measures are included.

**The tracker is no longer being updated and should not be considered up-to-date.**

A searchable version of the database along with a short snippet of the latest developments can be found on [the Bloomberg Law website](https://news.bloomberglaw.com/pfas-project/pfas-state-activity-tracker).

PFAS, which stands for per- and polyfluoroalkyl substances, are a group of man-made chemicals that are distinguished by their durability and water resiliency. They're often referred to as "forever chemicals" because of their inability to naturally break down.

## How the Database was Constructed

This database was initially constructed by surveying existing PFAS state laws and regulatory actions. Where none were immediately apparent, state agencies were contacted for additional information. The tracker was previously primarily maintained by monitoring alerts set up on the Bloomberg Law and Bloomberg Government platforms.

The increasing amount of states' activity on PFAS and the manual nature of updating the tracker means that inevitably omissions or errors may have resulted when the tracker was being maintained. Additionally, information may not have been immediately updated when new developments occurred.

## Note on Database Structure

This dataset is organized such that each regulatory or legislative action is an
individual observation, or row. Legislative actions that contain multiple versions of the same bill (such as a Senate version and a House version) are combined in a single entry. The bill that's listed first under the `Notes` field is where the URL will direct.

Legislative proposals are included in the tracker until they are no longer actively under consideration (usually due to the legislative session ending). Since many legislative sessions span two years, a bill may remain on the tracker more than a year after its introduction even if no action has been taken in some time.

Appropriations bills that include spending allocations for PFAS-related initiatives are not included on the tracker until they become law. This is due to the volume of appropriations bills that are introduced during legislative sessions, as well as the many iterations these bills undergo.

## Data Description

[PFAS State Activity Tracker.csv](data/PFAS%20State%20Activity%20Tracker.csv) - A
comma-separated values file of the PFAS State Activity Tracker.

## Data Dictionary

| Data Field | Description | Data Type |
| ---------- | ----------- | --------- |
| `State` | State | string |
| `Rule Type` | Type of measure being proposed or enacted: *Binding, Court Order, Legislation, No action, Non-binding guidance, Proposed Action* | string |
| `Action Type` | Focus of action being proposed or enacted: *Environment, Environment and Health, Environment and Liability, Environment and Product, Health and Safety, Liability, Other, Product, Unknown* | string |
| `Description` | Description of what action is being taken on PFAS | string |
| `Status` | Status of action: *Pending, In effect* | string |
| `Effective Date` | When the action takes effect (if applicable) | date |
| `Link Text` | Text to display for hyperlink (*Note: Used for generating clickable links in PDFs and the interactive table*) | string |
| `URL` | URL to more information on the action | string |
| `Hyperlink` | Hyperlink that combines the `Link Text` and `URL` into a clickable object (*Note: This will not display in the CSV and will only appear as plain text*) | string |
| `Links` | Text written in HTML that combines the `Link Text` and `URL` into syntax that opens the link in a new page (*Note: This is for generating clickable hyperlinks in the searchable version of the tracker*) | string |
| `Notes` | Additional information on the action (if applicable), such as bill number or when legislation was signed into law | string |
|`Entry Last Updated` | When the entry was last updated | date |
