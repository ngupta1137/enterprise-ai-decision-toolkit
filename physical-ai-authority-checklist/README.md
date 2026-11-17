# Physical AI Authority Checklist

An instrument in the style of the Enterprise AI Decision Toolkit. Fill it in for any robot or physical AI system before it operates outside a lab or test site, including industrial robot arms, collaborative robots, autonomous mobile robots in warehouses and plants, autonomous vehicles on sites or roads, drones, service and humanoid robots, wearables and exoskeletons, and field robots. If a line cannot be filled in, the system is not ready to work there.

## 1. The system and its owner

- System name and what it is (vehicle, arm, drone, wearable, humanoid, mobile robot, other):
- The team or company responsible for it:
- Accountable decision owner, by name (one person, not a team):
- Business owner, by name:
- Technical owner, by name:
- Where it will work (factory floor, warehouse, store, hospital, public road, site, field, or other):

## 2. The job

- The one job this system exists to do, in one sentence:
- The operator or site owner problem it solves, in their words:

## 3. Permitted actions

What the system may do, with the authority state for each action (Recommend, Act with approval, or Bounded autonomy) and its limits:

- [ ] Action:
  Authority state (Recommend / Act with approval / Bounded autonomy):
  Limits:
- [ ] Action:
  Authority state (Recommend / Act with approval / Bounded autonomy):
  Limits:
- [ ] Action:
  Authority state (Recommend / Act with approval / Bounded autonomy):
  Limits:

## 4. The operating envelope

The system may act only inside all of these limits:

- Area and boundaries:
- Hours and conditions (light, weather, surface or ground state):
- Speed, load, height, or force limits:
- Minimum distance from people and animals:
- Zones, equipment, or materials it must stay out of:

## 5. May never do

Actions this system must never take, under any instruction:

- [ ] 
- [ ] 
- [ ] 

## 6. People in the space

- Who shares space with the system (workers, customers, patients, public, none):
- Minimum separation distance from people:
- Maximum speed when people are nearby:
- Who on site can stop it, and what training they receive:

## 7. Lost connection and remote operation

- Safe state when the system loses connection (stop in place, return to base, or other):
- Safe state when primary sensors fail or give conflicting readings:
- Whether a remote operator can take control, and who that is:
- What a remote operator is allowed to do:
- What a remote operator is not allowed to do:

## 8. Stop and escalate

- What the system must stop and ask about instead of deciding alone:
- Who it asks, and how (person on site, remote operator, other):
- How fast a human can take over:
- The physical stop: where it is, and who can reach it:
- The remote stop: who holds it:
- Stop drill: how often the team practices stopping it, and when it was last drilled:

## 9. Safety case and standards

This checklist sits alongside the safety case and does not replace it.

- Safety standards, certifications, or regulations that apply:
- Safety case reference and document location:
- Who signed the safety case, by name:
- Date the safety case was signed, and next review date:

## 10. Fleet and updates

Any change to software, model, or maps is a change event. Test on a small part of the fleet first, and record the change on an Authority Change Record before it reaches every unit.

- Number of units running on this software or configuration:
- Test group: which units receive changes first, and for how long:
- Evidence required before an update rolls out to the rest of the fleet:
- Rollback plan if an update fails in the field or on site:

## 11. The data

- What the system records (video, audio, location, telemetry, environmental data, other):
- Rule for incidental capture of workers, customers, patients, or the public:
- Where the data goes, and who owns it (team, operator or site owner, other):
- What the operator or site owner agreed to, in writing, before recording started:
- How long the data is kept, and who can see it:

## 12. Earning more authority

Authority widens on evidence, never on confidence. Rate the evidence against the eight-dimension Evidence Chain, starting with risk and operational readiness.

- What proof is required before the envelope gets wider (hours run, incidents, tests):
- Who reviews that proof:
- Who signs the change (record it on an Authority Change Record):
- Demotion trigger: what suspends the system's authority automatically, and who decides whether it is revoked:

## 13. Incidents

- What counts as an incident for this system:
- Where incidents are logged, and who reads the log:
- What happens to the system's authority after an incident, and what evidence, gathered after the fix, restores its authority:

---

Part of the Enterprise AI Decision Toolkit, by Nitin Gupta. Companion to the book Enterprise AI Decision System: Turning Capability into Authorized Enterprise Action (forthcoming). The toolkit's other instruments, including the Authority Change Record and the Stop Memo, are at github.com/ngupta1137/enterprise-ai-decision-toolkit, DOI 10.5281/zenodo.23464328.
