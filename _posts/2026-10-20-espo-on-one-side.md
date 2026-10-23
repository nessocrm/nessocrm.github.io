---
layout: post
title: "Espo on one side"
date: 2026-10-20
lang: en
locale: en_US
permalink: /en/blog/espo-on-one-side/
alt: /it/blog/espo-da-una-parte/
description: "Nesso always has Espo on one side and a channel on the other: the connection is the channel and the integration is the rule."
image: /assets/images/blog/ch1-two-sides.webp
image_sm: /assets/images/blog/ch1-two-sides-640.webp
image_alt: "Sheets on one side, four squares in the middle, a dark archive on the other."
series: giro
series_order: 1
author: Nesso
---

This is the first of four readings of the same run. It does not tell the story of a customer. It tells a decision already taken in the engine, and the consequences that decision has on a master-data file that arrived at night. The file is an example, the same one the home of the site shows in small: a new row, an unchanged row, a row with a missing column, and a note a person wrote on Espo that the file must not empty. The chapters after this one go into the key, into the empty cell, and into the switches that stay off. Here the boundary stops: who stands on one side, who stands on the other, and what does not cross.

If a sentence of this diary and a sentence of the manual diverge, the manual wins. The manual lives in the docs folder of the public repository, and it changes together with the code. This site does not recompile it. The diary explains the why. The manual remains the text that says what the program does today.

## The sentence

Nesso always has Espo on one side. On the other side there is an external system. In the middle there is a channel, an entity, and a mapping of fields. The passage toward Espo uses Espo's HTTP APIs, with the authorization header Espo expects. Espo's tables are not an interface. They are not opened, they are not updated with a query, and they are not used as a queue.

The sentence is short because the product is short. The person who configures does not write a stored procedure. They choose the channel, name the entity, say which column is the identity and which field ends up where, and decide how often the run must start. From there the same engine moves the records, whichever entity it is. A webhook from a site can feed Leads. A second integration, on the same connection or on another, can feed Contacts. The engine does not change its trade when the entity changes. The rule changes.

The name of the external system is not in the code. It can be an ERP, a site, a folder of files, or a database read with a SELECT. The product does not become that name. If the name entered the code, every new customer would be a change to the program. Instead, every new customer is a configuration: a connection, one or more integrations, and a mapping reread by a person.

## Two objects, not one

The connection is the channel. It holds the address, the way of authenticating, and the type of entrance or exit. The integration is the rule. It holds the entity, the column that serves as identity, the mapping of the fields, the cadence, the owner of each field, and whether write-back is on. By default that write is off. Chapter four explains why, and what happens if someone turns it on.

An integration has only one connection. A connection can have more than one integration. That is the right shape for a file that brings the master data at night and, in a second run, the sites. The two rules do not mix, because each has its own identity. The key contains the id of the integration. Two files on the same Account entity remain two stories. Chapter two shows how that key is made. Here it is enough to know that the separation is deliberate. One connection with only one rule would force two trades into the same mapping, and the day one of the two files changes a column, both would break.

Direction follows the channel. If the connection is HTTP, the integration leaves Espo: the cursor remembers the last record sent, and the next run sends only what has changed. If the connection is a webhook, a SELECT, a CSV, an Excel file, an SFTP, an FTPS, a PDF whose name contains the company key, or a document, the integration enters. An HTTP integration does not become an upload. A file integration does not become an exit. Changing direction means changing the connection, not ticking a hidden box inside the same rule.

This separation avoids a common mistake. Someone takes a file, loads it, and then wants to send Espo's changes back onto the same file without having decided which columns come back. In Nesso that return is another decision, and it stays off until the columns are named. The inbound channel remains an inbound channel. The return, if one day it is turned on, writes only where someone has indicated a column name.

## Tonight's file, as the thread

To avoid speaking in the abstract, the four chapters use the same file. In the telling it is called the master-data file. It arrives at night in a folder. It has a column with the external code, one with the name, one with the city, one with the VAT number, and one with a note. The external code is the identity. The name, the city, and the VAT number are fields of the source. The note, in this integration, has Espo as its owner, because a salesperson writes it on the record and the night file must not delete it.

In tonight's file, three cases are enough to see the run.

The row for code C014 is identical to the last time. The hash of the row is already the one that was saved. Espo is not called. There is no update to make, and there is no reason to touch the record. A second identical send does not duplicate the record and does not rewrite it.

The row for code C001 is not on Espo yet. The run prepares it as a new Account. In the story the home tells, the name is Nord Est and the city is Trieste. The key that will be born on the standard entity is made of the integration id, a colon, and C001. On the entities Espo already has, the field is called cExternalKey. The note, on creation, is written anyway if the file brings it. The record does not exist yet, and there is no person's note to protect. From the next run on, the owner counts, and chapter three explains that calmly.

One row, the eighteenth in the story, does not have a required column. The file does not move into elaborati. The discard is a single discard, of the file, not a queue of rows. The other rows are not let through halfway. A missing cell is a different case, and in that case the column is there: that row is discarded, and the others continue. They are two different errors. The first says the file is not the one that was expected. The second says a row is incomplete. Treating them the same way would either block everything for one cell, or load a truncated file as if it were whole.

There is also the case tonight's file does not show, which chapter three keeps at its center. A row that was there yesterday is not there tonight. The record on Espo is closed and stays in the history. The first time a run would close records, it asks for confirmation. The gesture is only anticipated here, because without this chapter's boundary it would look like a deletion. It is not.

## Who reads the run

Four people look at the same file, and they are not looking for the same thing.

The person who keeps the number looks at the home. The number of aligned master records counts only if today's inbound run toward Account succeeded. A success from yesterday is not presented as today. If the run fails, the percentage is not shown. If a file is expected within an hour and that hour passes without a successful run, the border lights up. The number is a check. It does not write to Espo and it does not correct the file.

The person who has the note is the salesperson. They wrote a sentence on the record that the file does not know, or that the file would bring empty. The field has Espo as its owner. The night run does not empty it. If the file brings a different value, that value goes to a queue to be looked at. The badge on the record says who wrote last. It is not a legal chronology. It is the mark of the last run that touched the record, useful when someone has to see whether the row is still the file's row.

The person who checks opens the preview before the write. They see what would be born and what would change. A VAT number that is already present is seen before the POST. Undoing goes back over what the run has written. The first closing of records that have disappeared asks for confirmation from this person, or from whoever has the job of saying yes. A truncated file does not close the list by itself.

The person who installs does four steps: connection, entity, mapping, run. The recipe for master data, contacts, sites, or the price list is a starting point. It is reread. It is not a certified connector, and the name of the ERP is not written in the program. The switch-on plan says what stays off: write-back, the retry queue, the portal filter, the seal on secrets. The handover page does not contain the passwords. Without the variable NESSO_SECRET_KEY the volume keeps them in clear text. That has to be said to the person who receives the trial. Chapter four is all of this, with the details. Here it enters only as part of the boundary. The person who installs hands over a run, not a second ERP.

## Entities, not a second archive

The entities live in Espo. The engine does not invent entity names. It reads the entities this installation exposes. Account, Contact, Lead, Opportunity, Case, Task, Meeting, Call, and Document are standard entities, when they are there. On those, the external key is the custom field cExternalKey.

If the entity does not exist, Nesso can create it through the API. You indicate the singular and the plural. Espo adds the prefix C. The fields of the new entity do not receive a second prefix. The key, on an entity created here, is called externalKey. An entity created here is an Espo entity. Whoever has the team can see it. It is not a parallel archive kept in the engine's SQLite file.

The SQLite file is the engine's memory: connections, integrations, hashes, the cursor, the journal. It does not replace Espo and it is not a second CRM. The master data do not live there. What lives there is the memory of which row has already been seen and which record has already been sent. They are two different memories, and chapter two separates them. Confusing them is how an upload rewrites everything every night, or an exit resends the same records forever.

The team and the assigned person come from a column of the file or from a fixed team. Visibility is a rule of Espo: this row belongs to the Sales team, assigned to this person. Nesso does not invent a permission outside Espo. Espo users are not created from a master record. A column of people's names does not become a list of logins. Creating a user is an administration gesture, with a password and a role. A file of customers does not contain that gesture.

The price-list recipe points at the Product entity. If this installation does not have that entity, the price-list fields stay empty. The recipe does not invent the catalog. It is an honest limit: better an empty mapping, visible, than a ghost Product created to make a slide's figures add up.

## What does not cross

The CRM's mail stays in Espo. Nesso does not become the program that reads the mailbox, and it does not become the program that sends mail. Whoever already has mail configured in Espo leaves it there. Adding a mail channel because the engine is already in the middle would mix two trades and two secrets. The secret of a mailbox is not the secret of a master-data file.

The Advanced Pack is not rewritten. It is not in the repository. If someone has it locally, it stays local. The engine does not publish it and does not copy it together with the data of a real installation. The boundary is the same as for the dumps: the trial starts empty.

Production dumps are not imported into the trial Espo. They are not mounted, the attachments are not copied, and the backup is not used as a development database. An empty Espo is the trial. A dump is something else. It contains people, notes, files, and a history that did not ask to end up on a laptop. The public repository, github.com/nessocrm/nessocrm, brings up, with Docker Compose, the database, an empty Espo, and the engine. This page does not collect mail and does not open an account. The contact is the repository.

There is no run without Espo. The product is not a generic bridge between any two systems. Taking Espo off one side and putting anything else there would make another program, with another name. The opening sentence is also a refusal of that generalization. The channel can change. The Espo side cannot.

## A script, a query, a second CRM

A script reads the CSV and does an insert. The next day the file has one row fewer and the script deletes, or it leaves the record and nobody knows the source no longer has it. There is no preview. There is no hash, so it rewrites even the row that has not changed. If the salesperson's note sits in the same table, the script empties it when the cell arrives empty. It has no owner for the field. It works the first night. The second night is already an incident, only the incident has the shape of a success: the command exited with code zero.

A query on Espo's tables skips the checks, the teams, the history, and the hooks. The day Espo changes a schema, the query is the first piece that breaks, and it breaks in silence: the column is still there, the meaning is not. Nesso speaks with Espo only over HTTP. The key, the team, and the closing pass through the APIs. Espo's database is not a channel, not even only to read. Reading an entity is a call. Writing an entity is a call. The outbound cursor remembers the last modifiedAt and the id, and it advances only after the POSTs that succeeded. If the external key is missing, the pull stops: the records after that do not leave. This too is in chapter two. Here it says that the caution lives in the protocol, not in a more careful query.

A second CRM keeps the master data in another product and then chases them into Espo. The truth doubles. A correction made over there is not the correction made over here, and on Monday morning someone chooses by feel which of the two is the real one. Nesso is not that second place. It always has Espo on one side. The other side is a channel: a file, a SELECT, a call. The truth of the source fields, by default, is the source, including the empty cell. The exception is named field by field, and it is the Espo owner. There is no third truth in the middle, kept for safety in the engine's file.

## The recipes and the demo

Master data, contacts, sites, and the price list are four starting points. Each one names an entity and some columns. They do not write on their own. They do not certify that the system on the other side has one particular name. Propose the mapping reads the column names, in the language of the page, and proposes the Espo field, including the VAT number if the entity has a fiscal field. A column that is not recognized stays empty, to be filled in by hand. The synonyms are a list. They do not go out onto the network. They do not save the integration. The person reviews, and then saves.

Complete the empty columns calls a model only if an address is set. It fills the columns that are still empty, among the fields the entity knows. It does not touch a column that is already mapped. It does not save. The call sends the column names, at most three short cells, and the name of the field. It does not send the connection's password. The model's address does not enter the configuration download. Without an address, no call is made, and the proposal by synonyms remains. The model does not choose the channel, does not create entities, and does not turn write-back on. The journal of a run and the scheduler stay in the language of the run. The model does not rewrite them.

The Gruppo Meridia demo, in the manual, is the trial of a run. It is not a second product and it is not a customer published on this site. Naming it here is so that it does not hang in the air as a commercial case. It is a trial Espo, with runs described in the manual, useful to someone who wants to see the shape of a load before putting in their own files. The four flows of the backup from which the idea was born — the site, the night files, the master data, the jobs — are not code. They become configurations, if they are needed. They are not four programs inside Nesso.

## The run, still without the details

The cadence is manual, five minutes, fifteen, an hour, or a fixed time. An integration that is paused is skipped by the scheduler and by the webhook. Run now is the exception: that one starts because a person asked for it. The same integration does not start twice. The second start receives the answer that a run is already in progress. Two different integrations can run at the same time. If one is already in progress, the scheduler skips it and does not write an error every thirty seconds.

After an error, the clock updates and the full interval is waited. Only with retry_failed on does the clock stay where it was, and the run can present itself again sooner. It is a choice, off by default. An error is not an invitation to hammer Espo. It is an invitation to read the journal, which stays in the language the run was started in. The page can be in Italian or in English. The journal is not translated afterwards.

The preview does not write. Read mode and the general switch stop writes. A run in read mode reads, compares, and does not send the POST. These are the brakes. They sit in chapter four together with the queue, the portal, and the seal, because they are all of the same kind: they exist, and by default they do not change a run that already works.

## The page, the journal, the language

The page on which the run is configured is in Italian or in English. The choice belongs to the page, not to the file. A master-data file has no language of the product. It has columns, and the names of those columns are read in the language of the page when someone asks for the mapping proposal. An Italian column name and an English column name can propose the same field, because the synonyms are a list per language. The proposal does not save. The person who confirms is a person, and the confirmation is the save.

The journal of a run stays in the language of the run. If the run was started from a page in Italian, the journal's sentences stay in Italian even if the next day the page is opened in English. This is not an oversight. The journal is the minute of that execution, not a brochure to be realigned. Translating it afterwards would make two minutes. The scheduler, in the same way, speaks the language in which it was set. The person who reads an error at seven in the morning has to read the sentence the engine wrote, not a paraphrase.

This diary, by contrast, exists twice, in Italian and in English, because it is an explanation and not a minute. The two texts say the same facts. They do not say that the journal will do the same. If you look in the journal for the sentence of this chapter, you will not find it. The journal says what happened to a row, not why the product has two objects.

## Two integrations on the same Account

It is worth seeing, before the technical chapters, a case the boundary makes possible and a single script makes confused. The same Espo, the same Account entity, two files. The first is the master-data file, with the customer code. The second is the sites file, with the site code. If they ended up in the same integration, the identity column would be a single column, and a site code would be read as a customer code, or the reverse. With two integrations, the master-data key contains the id of the first, and the site key contains the id of the second. Both can live on Account. They do not overwrite each other, because the whole key is different even when the external value happens to be the same string.

The connection can be the same, if the two files arrive from the same channel, for example the same folder or the same SFTP. It can be different, if the master data arrive from a CSV and the sites from a SELECT. The integration does not inherit its direction from an opinion. It inherits the direction from the connection it is attached to. Attaching the sites integration to an HTTP connection would make it leave Espo, not enter. That is a configuration error you can see, not a surprise at runtime written in a comment.

The person who installs keeps the two rules side by side and turns them on one at a time. First the master data, with the preview. Then the sites, with the preview. The number on the home, the one for aligned master records, counts inbound runs toward Account. A sites run toward Account enters that count if it is an inbound run toward Account. This has to be known, so that a success of the sites is not mistaken for the success of the customer file, and a failure of the customer file is not covered by a sites run that went well the same morning. The number is one. The runs are many. The chapter on the run, later, says when the number has the right to appear.

## Monday morning

The boundary is judged on Monday, not on the evening the file was loaded the first time. On the first evening a script and Nesso look alike: the new rows become records. On Monday the file has one row fewer, a cell that has been emptied, a note written by hand on Friday, and a person asking whether the system updated. The answer depends on where the truth is.

If the truth is a query written once, the answer is that it did what was written, and what was written did not name the note. If the truth is a second archive, the answer is that it depends which of the two you looked at. If the truth is this boundary, the answer is longer and more useful. The source fields are those of tonight's file, including the empties. The fields whose owner is Espo are those the person left. The records whose row is gone are closed, if someone confirmed the first closing, and they stay in the history. The file already processed is not reread. The expected file that did not arrive has lit the border, and the number on the home does not lie about the hour.

None of these answers requires opening the tables. They are read from the journal, from the preview, and from the badge. The boundary is this as well: on Monday you reason about objects a person can name, not about a database column that only the person who wrote the script remembers.

## What this chapter has not done

It has not described the format of the key character by character. The second chapter does that, together with the hash and the cursor, which are the two memories. It has not said what happens, field by field, when the cell arrives empty. The third chapter does that, together with the closing of the record that disappeared. It has not turned anything on. Write-back, the queue, the portal filter, and the seal stay off even at the end of the fourth chapter, because off is the behavior of the trial and the behavior of an installation that has not yet decided otherwise.

Tonight's file, at the end of this boundary, is still a file. C001 is not yet an Account. C014 has not yet been recognized as unchanged. The row without the column is not yet a discard. The later chapters make those gestures, one at a time, without moving Espo to the other side and without giving the file a product name.

One last distinction, before passing on to the key. The boundary is not a preference of style. It is the reason the engine can stay the same when the file changes. If the boundary were that Nesso speaks with one named ERP, the next chapter would be a list of that ERP's fields, and the day the file changed a column name the program would be rewritten. The boundary is that Nesso speaks with Espo on one side and with a channel on the other. The next chapter can then speak of a key, a hash, and a cursor, without asking the name of the system that put the file in the folder. The name stays outside. The rule stays inside.
