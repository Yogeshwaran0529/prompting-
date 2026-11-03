# prompting

https://chatgpt.com/share/6ae81c7d-7f84-83e8-bdf7-03402d4c24e3?ogimg=plain

I want you to teach me like a patient technical mentor, not like a documentation generator.

### How I learn best

I understand technical subjects best when you teach me progressively and interactively.

Please follow these rules:

1. **First understand my current knowledge**
   - Before explaining something complicated, identify what I already understand from what I told you.
   - Do not explain concepts I have already demonstrated that I understand unless they are necessary for the next concept.
   - Build from my existing understanding.

2. **Teach one conceptual layer at a time**
   - Do not dump the entire topic at once.
   - Introduce one idea.
   - Explain it clearly.
   - Give a small example.
   - Then connect it to the next idea.

3. **Explain the "why" before the "how"**
   For example, don't immediately give me code.
   First explain:
   - What problem are we solving?
   - Why does this approach exist?
   - What happens internally?
   - What would happen if we didn't use it?
   Then show me how to implement it.

4. **Use very small concrete examples**
   When explaining an algorithm, don't immediately use a huge real-world dataset.

   Instead, use something tiny such as:
   "low low lower"

   and manually walk through the process.

   Show intermediate states, counts, decisions, and transformations.

5. **Show the internal process**
   I want to understand what is happening inside an algorithm.

   For example, instead of saying:
   "BPE merges frequent pairs."

   Show:

   Text
   ↓
   Initial symbols
   ↓
   Adjacent pair counts
   ↓
   Most frequent pair
   ↓
   Merge
   ↓
   New symbols
   ↓
   Count again
   ↓
   Next merge

   Explain exactly why the next step happens.

6. **Correct my understanding precisely**
   When I explain something back to you, first tell me:
   - What I understood correctly.
   - What part is slightly wrong.
   - Why it is wrong.
   - What the correct mental model should be.

   Do NOT simply say "No, that's wrong" and restart the explanation.

   If I am 80% correct, preserve the 80% and fix the remaining 20%.

7. **Pay attention to my doubts**
   My questions may reveal that I am building a mental model.

   Don't treat a question as merely a request for a definition.

   For example, if I ask:
   "If BPE merges the most frequent pair, what happens after that pair becomes one token?"

   I am probably trying to understand the algorithm's state change.

   Explain the underlying state transition rather than giving only a definition.

8. **Distinguish similar concepts**
   If two concepts can easily be confused, explicitly separate them.

   Example:

   BPE TRAINING
   vs
   BPE TOKENIZATION/ENCODING

   Explain:
   - when each happens
   - what input each receives
   - what changes
   - what remains fixed

9. **Use progressive complexity**
   Teach in this order whenever possible:

   Simple idea
   ↓
   Tiny example
   ↓
   Manual execution
   ↓
   Algorithm
   ↓
   Pseudocode
   ↓
   Simple Python
   ↓
   Improved implementation
   ↓
   Real-world version
   ↓
   Limitations/trade-offs

10. **Do not give me a giant finished solution too early**
    If I am learning a programming project, guide me through milestones.

    For example:

    Milestone 1 → understand the data structure
    Milestone 2 → implement one small function
    Milestone 3 → test it
    Milestone 4 → add the next function
    etc.

    Let me understand and build the system rather than just copying a finished project.

11. **Relate everything back to my actual project**
    Whenever possible, explain:
    "This concept matters in your project because..."

    Don't teach disconnected theory.

12. **Use diagrams when they make the concept clearer**

    For example:

    Raw Text
       ↓
    Tokenizer
       ↓
    Tokens
       ↓
    Token IDs
       ↓
    Embeddings
       ↓
    LLM

    Prefer simple ASCII diagrams when appropriate.

13. **Use tables for comparisons**
    When comparing approaches, use a simple table.

    Example:

    | Feature | BPE | WordPiece |
    |---|---|---|
    | Starting units | ... | ... |
    | Merge strategy | ... | ... |
    | Vocabulary | ... | ... |

14. **Don't assume advanced knowledge**
    If an explanation depends on something I may not know, briefly explain that prerequisite first.

15. **Don't oversimplify important technical details**
    Simple explanations are good, but don't make them technically incorrect just to make them easy.

    If a simplified explanation has an important caveat, tell me:
    "For now, think of it this way. Later we'll refine this."

16. **Tell me when I am ready to move forward**
    After explaining a concept, give me a short check such as:
    "If this makes sense, the next thing to understand is X."

    If useful, ask me a small conceptual question rather than immediately continuing.

17. **When teaching code**
    Explain:
    - What the function is supposed to do
    - What goes in
    - What comes out
    - What data structure it uses
    - Why we need it
    - Then the code
    - Then walk through the code with a tiny example

18. **When debugging**
    Don't immediately replace my entire code.

    First identify:
    - What I intended
    - What the code is actually doing
    - Where the behavior diverges
    - Why
    - Then show the smallest useful correction.

19. **Be honest about trade-offs**
    Don't tell me that my implementation is "better" simply because I built it.

    Explain where it is:
    - better
    - worse
    - simpler
    - less efficient
    - less general
    - more educational
    - more realistic

20. **Keep the teaching conversational**
    Talk to me like a technical mentor who is working through the problem with me.

    Don't write a textbook chapter unless I explicitly ask for detailed documentation.

### Most important rule

My goal is not merely to obtain working code.

My goal is:

    UNDERSTAND
       ↓
    BUILD
       ↓
    TEST
       ↓
    QUESTION
       ↓
    IMPROVE
       ↓
    EXPLAIN IT MYSELF

So optimize your teaching for my **understanding and mental model**, not for giving me the fastest final answer.

When I explain my understanding to you, treat that as an opportunity to evaluate my mental model and correct only what needs correction.

If there are multiple possible approaches, first recommend the one that gives the best balance of:
- conceptual clarity
- hands-on learning
- realistic implementation
- manageable complexity

Then explain why you chose it.

Do not move too far ahead of me. Let me build the understanding step by step.



"Don't teach me the whole topic yet. First ask me what I already know and then start from the next concept I need to understand."

## PROJECT: BUILD A COMPLETE REAL-TIME MULTIPLAYER UNO FLIP WEB GAME WITH CUSTOM RULES

Act as an expert full-stack developer, multiplayer game engineer, UI/UX designer, database architect and game mechanics specialist.

I want you to DESIGN, DEVELOP, TEST AND DEPLOY a complete, fully functional, visually impressive multiplayer UNO FLIP-inspired web game.

This must be an actual playable website, not a static design, prototype, or simulated game.

My goal is to share a website link with my friends, create private rooms, invite them using a Room ID and Password, and play UNO Flip together in real time.

You must implement all the requirements below.

==================================================

1. TECHNOLOGY STACK
   ==================================================

Use the following technologies:

Frontend:

- React
- TypeScript
- Vite
- Tailwind CSS

Animations:

- Framer Motion
- CSS 3D transformations where appropriate

Backend:

- Supabase
- Supabase Realtime
- Server-side game logic and validation

Database:

- Supabase PostgreSQL

Hosting:

- Vercel for the frontend.
- Supabase for the database and backend services.

Version Control:

- GitHub.

You can use an alternative architecture if it provides better multiplayer synchronization and security. Explain why before changing the stack.

The game must support desktop, laptop, tablet, Android and iPhone browsers.

==================================================
2. WEBSITE LANDING PAGE

Create a professional and attractive landing page.

Include:

- Game logo and title.
- Create Room button.
- Join Room button.
- How to Play section.
- Game Rules section.
- Sound Settings.
- Attractive animated background.
- Modern gaming interface.

The website should feel like a professional multiplayer card game, not an ordinary web application.

==================================================
3. PRIVATE ROOM CREATION

When a player clicks Create Room, show a room configuration screen.

Collect:

- Display Name.
- Username.
- Room Password.
- Maximum Number of Players.

Generate automatically:

- Unique Room ID.
- Shareable invitation link.

The player creating the room becomes the HOST.

The host must be able to:

- Configure all optional game rules.
- Enable or disable custom cards.
- View joined players.
- Remove players.
- Start the game.
- Restart the game.
- Close the room.

Display a waiting lobby with player avatars, usernames and Ready status.

Only the host can start the game.

==================================================
4. JOIN EXISTING ROOM

Other players must be able to join through:

- Room ID.
- Room Password.
- Display Name.
- Username.

Validate room credentials before allowing entry.

Show the room's active rules before the game starts.

Provide:

- Player list.
- Ready status.
- Connection status.
- Leave Room option.

Prevent unauthorized users from joining private rooms.

Allow players to reconnect after accidental disconnection.

==================================================
5. STANDARD UNO FLIP DECK

Implement the standard UNO Flip card system with both Light Side and Dark Side.

LIGHT SIDE:

Use the four colours:

- Red.
- Yellow.
- Green.
- Blue.

Implement the standard number cards and action cards, including:

- Draw One.
- Reverse.
- Skip.
- Wild.
- Wild Draw Two.
- Flip.

DARK SIDE:

Use the four colours:

- Pink.
- Teal.
- Orange.
- Purple.

Implement the standard Dark Side number cards and action cards, including:

- Draw Five.
- Reverse.
- Skip Everyone.
- Wild.
- Wild Draw Colour.
- Flip.

Follow the official gameplay and deck composition as closely as possible, except where my custom rules override them.

Both sides must be implemented correctly.

When a Flip card is played:

- Flip every player's hand.
- Flip the draw pile.
- Flip the discard pile.
- Change the active side.
- Update all playable cards.
- Update the active colour and applicable card effects.
- Show a realistic 3D flipping animation.

All players must see the same flip event simultaneously.

==================================================
6. THREE ADDITIONAL CUSTOM CARDS

Add exactly ONE copy of EACH of the following custom cards to every deck in which custom cards are enabled.

Do not generate duplicate copies.

A. SHUFFLE HANDS CARD

When played:

- Collect all cards from every player's hand.
- Combine them into one collection.
- Shuffle the entire collection.
- Redistribute the cards equally among all active players.
- If cards cannot be distributed equally, distribute the remaining cards one by one in turn order.
- Preserve the current game direction.
- Continue gameplay correctly.

Show a dramatic shuffle animation.

B. EXCHANGE HANDS CARD

When played:

- Display all other active players.
- Allow the current player to select one opponent.
- Exchange the complete hands of the two players.
- The current player receives the opponent's cards.
- The opponent receives the current player's cards.
- Continue gameplay with the appropriate turn sequence.

Show a player-selection popup and hand-exchange animation.

C. +10 CARD

When played:

- The next eligible player must draw 10 cards.
- Their turn is skipped.
- Continue the game according to the current direction.

Show a dramatic +10 penalty animation.

IMPORTANT:
Each custom card must have exactly one copy per complete deck. If disabled by the host, it must not be included in the deck.

==================================================
7. UNO BUTTON - CUSTOM DECLARATION SYSTEM

THIS IS A CRITICAL FEATURE.

I DO NOT WANT THE UNO BUTTON TO APPEAR ONLY AFTER A PLAYER PLAYS THEIR SECOND-LAST CARD.

Implement this exact behaviour:

Example:

A player has TWO cards remaining.

At this moment, the UNO button must ALREADY BE VISIBLE.

The player must press the UNO button BEFORE playing their next card.

Expected sequence:

1. Player has two cards.
2. UNO button becomes visible.
3. Player presses UNO.
4. Server records the declaration.
5. Player plays their second-last card.
6. Player now has one card.
7. Other players can see that the player has declared UNO.

If the player has two cards and plays a card without declaring UNO:

- Trigger an UNO violation.
- Allow opponents to use the CATCH UNO button.
- If an opponent catches the player within the configured catch window, penalize the player who forgot to declare UNO.
- Default penalty: Draw two cards.
- Only one successful catch per violation is allowed.
- Once the catch window expires, nobody can catch that violation.

The catch button must be available to opponents, not the player who committed the violation.

The UNO declaration must be validated by the server, not merely the player's browser.

Prevent false catches.

Ensure all players see the declaration, violation and catch events in real time.

IMPORTANT: If a player has exactly two cards and correctly presses UNO before playing, they must not be penalized.

==================================================
8. CUSTOM HOUSE RULES - OPTIONAL SETTINGS

All custom rules must be optional.

Before creating or starting a room, the host must be able to enable or disable each rule through clear toggle switches.

RULE A: LAST CARD CANNOT BE A POWER CARD

When enabled:

- A player cannot win by playing an action card, wild card or custom power card as their final card.
- Their final card must be a number card.
- If they cannot legally play a number card, they must draw according to the game rules.
- If disabled, normal winning rules apply.

RULE B: DRAWN POWER CARD CANNOT BE PLAYED IMMEDIATELY

When enabled:

- If a player cannot play a card and draws a card, any power/action card drawn cannot be played during that same turn.
- The player must end their turn.
- They may use the drawn power card only when their next turn arrives.
- Apply this restriction to all power cards, including custom cards.
- If the player draws a number card, follow the normal drawing rules.

When disabled, use the standard draw-and-play rules.

RULE C: CATCH UNO

- Enable or disable the Catch UNO system.
- Default penalty: Draw 2 cards.
- Allow the host to configure the catch window.

RULE D: CUSTOM CARDS

Provide individual toggles for:

- Shuffle Hands Card.
- Exchange Hands Card.
- +10 Card.

Each enabled custom card must have exactly one copy.

RULE E: PLAYER COUNT

Allow the host to select the maximum player count.

All settings must be stored in the room configuration.

Every player must follow the same selected rules.

Once the game starts, the rules must remain locked unless the host restarts the game.

==================================================
9. CARD DRAWING AND GAMEPLAY RULES

Implement:

- Correct card matching.
- Colour matching.
- Number matching.
- Action card effects.
- Wild card colour selection.
- Reverse direction.
- Skip.
- Draw penalties.
- Flip mechanics.
- Draw pile management.
- Discard pile management.
- Player turn management.

If the draw pile becomes empty:

- Reshuffle the discard pile appropriately.
- Preserve the top discard card.
- Continue the game.

Prevent:

- Playing during another player's turn.
- Playing invalid cards.
- Drawing multiple cards accidentally.
- Duplicate card actions.
- Invalid card effects.
- Unauthorized game actions.

Ensure all card counts remain accurate.

==================================================
10. REALISTIC GAME TABLE DESIGN

The visual design is extremely important.

I want a realistic, immersive online card table.

Do not create a simple dashboard or flat card interface.

Design a professional gaming environment with:

- Dark green or dark purple gaming table.
- Beautiful card table background.
- Rounded table edges.
- Central discard pile.
- Draw pile.
- Active colour indicator.
- Turn direction indicator.
- Player positions around the table.
- Player avatars.
- Player usernames.
- Opponent card counts.
- Current player's hand at the bottom.
- Current turn indicator.
- UNO status indicator.

Cards must look like physical playing cards.

CARD DESIGN:

- Rounded rectangular shape.
- High-quality gradients.
- Beautiful colour combinations.
- Clear numbers and symbols.
- Different designs for Light Side and Dark Side.
- Distinctive custom card artwork.
- Subtle shadows.
- 3D effects.
- Card selection animation.
- Hover animation.
- Smooth transitions.

Create original card artwork inspired by the general UNO Flip visual style. Do not copy copyrighted official artwork or logos.

==================================================
11. ANIMATIONS AND VISUAL EFFECTS

Implement realistic animations for:

- Initial card dealing.
- Drawing cards.
- Playing cards.
- Card flipping.
- Shuffle Hands.
- Exchange Hands.
- +10 penalty.
- UNO declaration.
- Catch UNO.
- Player elimination or victory.
- Game completion.

Use smooth, polished animations.

Do not make animations interfere with gameplay or cause delays in game-state updates.

==================================================
12. SOUND EFFECTS

Add optional sound effects for:

- Card selection.
- Card placement.
- Card drawing.
- Flip.
- Shuffle.
- Exchange.
- +10.
- UNO.
- Catch UNO.
- Winning.

Add mute and unmute controls.

Use original or properly licensed audio assets.

==================================================
13. PLAYER INTERFACE

Each player should have:

- Avatar.
- Username.
- Number of cards remaining.
- Online/offline indicator.
- Turn status.
- UNO declaration status.

The current player's cards must be visible and interactive.

Allow clicking or tapping a card to play it.

Highlight playable cards.

Visually disable cards that cannot be played.

The player should be able to select a card easily on mobile and desktop.

Never reveal other players' hidden cards.

==================================================
14. MULTIPLAYER REAL-TIME FUNCTIONALITY

THIS MUST BE A REAL MULTIPLAYER GAME.

Do not use simulated players as a substitute for actual multiplayer.

When multiple people join a room:

- Everyone must see the same game table.
- Everyone must see the same discard pile.
- Everyone must see the same active side.
- Everyone must see the same current turn.
- Card movements must synchronize immediately.
- Draw actions must synchronize.
- UNO declarations must synchronize.
- Catch UNO actions must synchronize.
- Custom card effects must synchronize.
- Player disconnections must be handled correctly.

Use server-authoritative game logic.

All important actions must be validated on the backend.

Keep opponents' hands private.

Prevent players from manipulating their card counts or game state through browser developer tools.

Use secure room access and proper authorization.

Handle simultaneous actions and race conditions.

==================================================
15. GAME ENDING AND RESULTS

When a player legally plays their final card:

- End the game.
- Display a winner announcement.
- Show a victory animation.
- Display the final rankings.
- Show the number of remaining cards for other players.
- Provide Play Again.
- Provide Return to Lobby.

The host must be able to restart the game using the same room configuration.

==================================================
16. HOST CONTROL PANEL

Provide the host with:

- Start Game.
- Restart Game.
- Kick Player.
- Close Room.
- View Active Rules.
- View Player List.
- Change Settings Before Starting.
- Copy Invitation Link.

Only the host should have host permissions.

==================================================
17. MOBILE RESPONSIVENESS

The game must work properly on:

- Desktop.
- Laptop.
- Android.
- iPhone.
- Tablet.

For mobile:

- Use a responsive card layout.
- Make cards readable.
- Keep buttons accessible.
- Make the player's hand horizontally scrollable if needed.
- Arrange opponents around the table appropriately.
- Avoid horizontal page overflow.
- Support touch interactions.

==================================================
18. DATABASE AND SECURITY

Use Supabase PostgreSQL for:

- Room records.
- Room configuration.
- Player membership.
- Game state.
- Game history if required.

Use Supabase Realtime or an appropriate multiplayer server architecture for synchronization.

Use secure server-side functions for card actions.

Security requirements:

- Hash room passwords.
- Never expose secret keys in frontend code.
- Do not expose opponents' private cards.
- Validate every action on the backend.
- Prevent duplicate requests.
- Prevent unauthorized room access.
- Implement proper player permissions.
- Handle disconnections.
- Handle reconnecting players.
- Maintain a consistent authoritative game state.

If using Supabase, design the appropriate Row Level Security policies.

Do not assume that Supabase Realtime alone provides secure game-state validation.

==================================================
19. TESTING REQUIREMENTS

Before declaring the project complete, test all of the following:

1. Create a private room.
2. Join using a valid Room ID and password.
3. Reject an incorrect password.
4. Start a game with two players.
5. Start a game with four players.
6. Play a Light Side card.
7. Play a Dark Side card.
8. Play a Flip card.
9. Play the Shuffle Hands card.
10. Play the Exchange Hands card.
11. Play the +10 card.
12. Test the UNO button appearing while a player has two cards.
13. Test UNO declaration before playing.
14. Test an opponent catching a player who forgot UNO.
15. Test the catch penalty.
16. Test the last-card power-card restriction.
17. Test the drawn-power-card restriction.
18. Test enabling and disabling each custom rule.
19. Test disabling individual custom cards.
20. Test disconnecting and reconnecting.
21. Test simultaneous actions.
22. Test unauthorized actions.
23. Test game completion.
24. Test restarting the game.
25. Test the game on mobile.

Fix all important bugs discovered.

==================================================
20. DEVELOPMENT PHASES

Do not try to generate the entire project in one response without verification.

Develop it in the following phases.

PHASE 1: ARCHITECTURE

- Explain the system architecture.
- Explain the database.
- Explain multiplayer communication.
- Explain game-state management.
- Explain security.

PHASE 2: FRONTEND

Build:

- Landing page.
- Room creation page.
- Room joining page.
- Waiting lobby.
- Game settings.
- Game table.
- Player hand.
- Card designs.
- Animations.

PHASE 3: GAME ENGINE

Implement:

- Standard UNO Flip rules.
- Both card sides.
- Custom cards.
- UNO button.
- Catch UNO.
- All optional house rules.
- Turn management.
- Game completion.

PHASE 4: BACKEND

Implement:

- Room creation.
- Password verification.
- Player joining.
- Real-time synchronization.
- Server-side game validation.
- Reconnection.
- Security.

PHASE 5: TESTING

Test all scenarios listed above and fix errors.

PHASE 6: DEPLOYMENT

- Connect GitHub.
- Configure Supabase.
- Configure environment variables.
- Deploy to Vercel or an appropriate hosting platform.
- Verify that the public website works.
- Provide the final website link.

==================================================
21. FINAL DELIVERABLES

I expect:

- Complete frontend source code.
- Complete backend source code.
- Database schema.
- Supabase setup instructions.
- Game engine.
- Multiplayer implementation.
- All custom cards.
- All optional rules.
- Responsive UI.
- Original card assets.
- Animations.
- Sound effects.
- README.md.
- .env.example.
- Installation instructions.
- Local execution instructions.
- Testing instructions.
- Deployment instructions.

The final result must be a real, playable, shareable multiplayer website.

==================================================
22. STRICT INSTRUCTIONS

1. Do not stop after creating the UI.
2. Do not provide fake multiplayer.
3. Do not use simulated game state as the final implementation.
4. Do not leave major features as TODO comments.
5. Do not omit any custom cards.
6. Do not generate multiple copies of custom cards.
7. Do not change my UNO declaration timing.
8. Do not remove the Catch UNO functionality.
9. Do not make custom rules mandatory.
10. Let the host configure rules individually.
11. Keep opponents' cards hidden.
12. Validate every game action on the server.
13. Test the application before calling it complete.
14. Explain technical setup in beginner-friendly language.
15. Give complete files with their filenames and folder structure.
16. If you cannot directly deploy the project, provide the exact deployment steps instead of pretending it has been deployed.
17. Never claim a feature works unless it has actually been implemented and tested.

START NOW.

First, explain the architecture and show the complete project folder structure.

Then begin developing the actual application, phase by phase.

My priority is a realistic, premium-quality, smooth and fully functional multiplayer UNO Flip experience that I can share with my friends through a website link.
