## Notes from learning hour

1. Event-Carried State Transfer


2. Event Notification
"I as a sub take state from another service". This one keep your susscriber-service stay dummy. It's safe and 




Fat event vs. Thin event.
- fat event contains a bit more data than you need; thin carries only those data you need

Aggregate Event. It's closer to a fat event, but main difference carries some extra data in the matter of hide business logic

if publisher produces a lot of small events (start X, move X in Y, start new XX etc) but all you need is final report of those all small events - here the aggregate event comes in handy


### Event store
stream_id: :user_id

it means that by user_id each event will be stored next to last stored event. 


streams_to_link: [:client_id, :location_id]
it needs when your event for user_id should be stored as well in stream :client_id and .... Why? Because the event relates to not one entity (User) but in other as well (Client, Location)


Good source of knowledges for Elixir and CQRS/EventSourcing - https://github.com/commanded/commanded/blob/master/guides/Aggregates.md



DB table "event_store"
table "snapshot" - it's kind of "save point" or a cache from which you app can start to read events. Why? To avoid re-read all 3.5 billion events before your snapshot. you will read stapshot + all new events stored after snapshot


---
Event Sourcing and CQRS are not the patterns for high level. 
It's better to use it locally, cause ES/CQRS are hard one, heavy pattern. 



to read more about it - https://martinfowler.com/articles/201701-event-driven.html
