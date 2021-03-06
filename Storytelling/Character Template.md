
# Standardized Character Templates
With advanced AI generation now available we can create massive quantities of characters extremely quickly for what is effectively free. The storytelling communities can therefore greatly benefit by coordinating a standardized template for characters and other storytelling materials.

## Advantages of Standardizing a Character Template
* Creates a consistent format to train AI models on.
* Creates a consistent format for editors, APIs, databases, and other development tools to use.
* Enables automatic integration into other storytelling materials, such as settings, relationships, factions, locations, etc.
* Greatly simplifies collaboration between storytellers.
* Greatly simplifies worldbuilding process and reduces the time investment.
* Provides a shared vocabulary and understanding among the community.
* Enables a universal system for lookup and retrieval.
* Simplifies the process of generating content for AI and humans alike.
* Allows the creation of relationship webs with other characters.
* Allows storytellers to quickly and easily manage entire settings.
* Allows quick modification of existing characters.
* Allows collections of characters with formative experiences and relationships.
* Allows the characters to grow and evolve (given the nature of this particular template style).

## The Character Template
The character template is a full directory that contains multiple aspects of a character within it. The character's aspects are stored as individual files that were standardized for the template.

A character template represents a character in their original setting, which may vary if they are introduced into new settings. This template is designed to interoperate with the overall, with some aspects of the character designed through other templates for purposes of improved story tracking.

The files contained with a character's directory are as follows:
* /images: Contains artwork of the character.
* /stages: Contains modification templates of the base character at different life stages or circumstances.
* /styles: Contains appearance templates for a variety of styles the character may appear in.
	* /default: Contains the default appearance template, which all other templates are based off.
* Stage Overview: A text file that provides an overview of the character's current stage.
* Previous Stage: A text file that indicates which stage was previous, and describes the transformation to the current stage.
* Details Template: Contains any details that are generally considered fixed and unchanging; e.g. name, titles, aliases, character GUID, etc.
* Model Template: Contains genetic markers and appearance (race, gender, weight, hair style, tattoos, etc).
	* Tracks values with the purpose of being used for procedural generation of the character.
* Abilities Template: Contains things like attributes, skills, feats, specialized knowledge, etc.
	* This template can include percentile markers to help AI automatically adapt characters to specific settings.
	* For example, having 90th percentile computer skill is very different in a 1980's setting than a 2000's setting.
* Personality Template: Contains things like interests, moral alignment, ideologies, etc.
* Belongings: Contains the character's expected possessions and assets.
* Status: Contains the character's expected status, occupation, achievements, etc.
* Backstory: Contains the character's and loosely defined formative events.
* Relationships: Contains the approximation of expected relationships the character has.

## The Actor Template
The actor template bridges a character with a story, and allows the actor to grow and change throughout the story by tracking their timeline. While a character template is considered static, the actor template can be as dynamic as the story needs it to be.

The actor template is a full directory that can overwrite details about the base character template. As it changes, it preserves a git-like repository of its changes, along with the appropriate updates to /history to explain and maintain backstory of the reasons for those changes.

The files contained within an actor directory are as follows:
* /savestate: A directory that can be used to save previous states of the actor at different stages of development or circumstance.
* /history: A directory dedicated to the historical timeline of the actor, specific events, etc. Includes backstory.
* /relationships: Contains relationship templates between this actor and otchers, from this actor's perspective.
* Actor Details: Includes a reference to the base character template, base savestate, story template, game template, and other critical details.
	* When savestates are used, the 'base savestate' value is important to determine which values are defaulted.
* Stat Template: Contains a game-specific stat template based on what story, setting, and game is applied.
* Status Template: Contains details on status; e.g. occupation, reputation, achievements, etc.
* Belongings Template: Contains details on notable possessions, assets, resources, etc.
