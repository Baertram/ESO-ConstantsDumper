# ESO-ConstantsDumper

The Elder Scrolls Online addon:
Simple addon to dump the CONSTANTS (copy from the constants section of that file) from the ESOUIDocumentationPxx.txt files with their values to the SavedVariables.

You need to create a file called "DumpVars_constants.lua" with these lines:

if DumpVars == nil then DumpVars = {} end
DumpVars.constantsToDump = {}

Between the {} of the table DumpVars.constantsToDump add the constants like this:
["ACTION_TYPE_ABILITY"] = ACTION_TYPE_ABILITY,
["ACTION_TYPE_CHAMPION_SKILL"] = ACTION_TYPE_CHAMPION_SKILL,
["ACTION_TYPE_COLLECTIBLE"] = ACTION_TYPE_COLLECTIBLE,
["ACTION_TYPE_EMOTE"] = ACTION_TYPE_EMOTE,
...

-> See the example file included with constants of the game's API 101032

Ingame enable the addon and call the slash command /dumpvars from your chat editbox.
The SavedVariables will be saved to live/SavedVariables/DumpVars.lua

Delete this file before you login and dump the constants, so that it will be re-created new and empty for your current API!
