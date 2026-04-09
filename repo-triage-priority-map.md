## Repo triage priority map
If I only had limited time in a new repository, this is the order I would use to find higher-signal review areas first.

1. **Privileged roles and authority boundaries**  
   Identify owners, admins, delegates, operators, receivers, multisigs, and any actor with state-changing power.

2. **Staged transitions and delayed acceptance**  
   Look for transfer, accept, stage, propose, claim, finalize, or next-role patterns.

3. **Verify / commit / finalize / execute flows**  
   These paths often hide state-transition assumptions and late-stage invalidation risks.

4. **Live config reads during finalization**  
   Check whether final outcomes depend on current config rather than the config active when the action began.

5. **Stored evidence vs current assumptions**  
   Look for proofs, attestations, confirmations, or approvals that may later be re-evaluated under changed conditions.

6. **Public entrypoints touching sensitive paths**  
   Public or permissionless calls are worth reviewing carefully when they interact with privileged state.

7. **Execution / verification boundaries**  
   In proving systems or multi-stage validation systems, confirm that execution assumptions match verification assumptions.

8. **Protocol invariants and advertised guarantees**  
   After finding hotspots, map them against stated claims like censorship resistance, permissionlessness, immutability, or liveness.
