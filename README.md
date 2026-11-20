# KnowledgeEngineering

## Practical Exercise 4: Knowledge-Based Autonomous Trailer Agent

This practical extends the Practical Exercise 3 Uniform Cost Search (UCS) trailer into a **knowledge-based agent**. The trailer stores facts and rules in a knowledge base, answers queries from it, and plans routes using only the roads the knowledge base marks as usable.

Everything is in **[`Autonomous_Trailer.ipynb`](Autonomous_Trailer.ipynb)**, organised into the lecturer's ten knowledge engineering steps, plus one optional extension.

**Knowledge base:** `Town(x)`, `Road(x, y, d)`, `RoadCondition(x, y, c)`, `At(Trailer, x)`, `Destination(Trailer, x)`. `CanUse`/`RoadOpen`, `RoadClosed` and `Reachable` are inferred by rules rather than stored.

## Results

| Scenario | Decision |
|---|---|
| All roads open | Nairobi → Nakuru → Mau Summit → Kericho → Kisumu (**357 km**) |
| Nakuru–Mau Summit closed | Nairobi → Narok → Bomet → Kericho → Kisumu (**383 km**) |
| Road reopened | 357 km route restored |
| Roads into Kisumu flooded | Unreachable; the agent does not move |

## Running

Standard library only. Open the notebook with any Python 3 kernel and choose **Run All**.
