### How do I find errors / bugs in AutoBar ###
  * See the [ErrorsBugs](ErrorsBugs.md) page.


### How do I Use AutoBar ###
  * See the [Usage](Usage.md) page.


### I cannot make my own pet / mount buttons ###
  * No, a Blizzard bug prevents this.


# How do I report a missing item? #
  * [List of Reported Missing Items](http://code.google.com/p/autobar/issues/list?q=label%3AMissingItem&can=1)
  * Please use something specific like: "Reins of the Black War Tiger 29471" or "Farkle Berry Juice 47:14000"
  * The 29471 & 47 are the ItemId for each item.
    * Get it from Loot Link as the "BaseId" in the tooltip.
    * Look it up on http://www.wowhead.com by searching by name & then looking at the items URL. The ItemId is at the end.
  * For foods & whatnot an aditional value after the colon gives how much it heals etc.
  * If Farkle Berry Juice was real and a buff food then also include what it buffs:
    * Farkle Berry Juice  47:14000   strength 30, dexterity 60, attack speed 90
  * Is there no end to the wondrous Farkle Berry Juice? It is also a combo food, so list its mana gain as well:
    * Farkle Berry Juice  47:14000 47:17000 mana strength 30, dexterity 60, attack speed 90

> I do not have the time to go search the entire game for missing items, nor do all items need to be added. If you miss it, give me the specific info I need to add it.


### How do I add items that are not in any existing categories? ###
  * See the [Usage](Usage.md) section.
  * See the "How do I report a missing item?" FAQ to get the item into the items database.
  * If you are an Ace author or have SVN access you can add the item to [PeriodicTable-3.1](http://www.wowace.com/wiki/PeriodicTable-3.0).


### How can I get the easy & classic AutoBar back? ###
  * Simply disable all but the Basic Bar
  * Remove all buttons on it that you do not like.


### Why can AutoBar no longer shuffle items during combat? ###
~~You need to enable the Shuffle attribute for a Button.  This lets it shuffle certain items during combat~~.


### Arrange on use causes a duplicate Button in the Popup! ###
> True that.


### I have a duplicate Button in the Popup! ###
> Turn off Arrange on Use.  It needs to have that extra button there.


### How do I skin AutoBar / my cyCircled does not work? ###
  * Please install [ButtonFacade](http://files.wowace.com/cat-action-bars.html).
  * Uninstall cyCircled, or get whatever mod still needs it to switch to ButtonFacade.


### How can I get my gigantic all in one Bar back? ###
  * Set **Bar Location** for each Extras Button to the Basic Bar, or **Remove** all the Extras Buttons, and then use the **Add Buttons** popup to add them to the Basic Bar.
  * Alternatively use **AutoBar/Move the Buttons** Mode.  Drag and drop all the Extras Buttons to your main bar.  Since both these bars are shared account wide this change happens for all characters.
  * Next you need to move the Class Buttons.  Set **Basic/Shared Buttons** to "Class" for the currently logged in character.  Now drag the class buttons over.  Since the Buttons are specific to that class, setting sharing to Class lets the bar remember the buttons differently for each class.
  * Repeat moving the Class Buttons for each different class you have.
  * If you have multiple characters of the same class that need individual button layouts then simply set **Shared Buttons** to "None" for one or more of them.
  * Note that with enough different classes eventually all Buttons will not fit on a single Bar.


### Files Required for AutoBar to work ###
Inside "World of Warcraft\Interface\AddOns\AutoBar":
  1. AutoBar.toc
  1. AutoBarButton.lua
  1. AutoBarCategory.lua
  1. AutoBarClassBar.lua
  1. AutoBarClassBasicButton.lua
  1. AutoBarClassButton.lua
  1. AutoBarClassPopupButton.lua
  1. AutoBarConsole-1.0.lua
  1. !AutoBarDB.lua
  1. AutoBarFuBar.lua
  1. AutoBarOptions.lua
  1. AutoBarSearch.lua
  1. Bindings.xml
  1. Core.lua
  1. embeds.xml
  1. Locale-enUS.lua
  1. Locale-koKR.lua
  1. Locale-zhCN.lua
  1. Locale-zhTW.lua
  1. Locale-deDE.lua
  1. Locale-frFR.lua
  1. Locale-esES.lua

Inside "World of Warcraft\Interface\AddOns\AutoBar\libs":

  1. LibStub\LibStub.lua
  1. AceLibrary\AceLibrary.lua
  1. AceOO-2.0\AceOO-2.0.lua
  1. AceEvent-2.0\AceEvent-2.0.lua
  1. AceAddon-2.0\AceAddon-2.0.lua
  1. AceDB-2.0\AceDB-2.0.lua
  1. AceDebug-2.0\AceDebug-2.0.lua
  1. AceHook-2.1\AceHook-2.1.lua
  1. Babble-Zone-2.2\Babble-Zone-2.2.lua
  1. Dewdrop-2.0\Dewdrop-2.0.lua
  1. FuBarPlugin-2.0\FuBarPlugin-2.0.lua
  1. !libs\LibBabble-Zone-3.0\LibBabble-Zone-3.0.lua
  1. LibPeriodicTable-3.1\LibPeriodicTable-3.1.lua
  1. LibPeriodicTable-3.1-Consumable\LibPeriodicTable-3.1-Consumable.lua
  1. LibPeriodicTable-3.1-Gear\LibPeriodicTable-3.1-Gear.lua
  1. LibPeriodicTable-3.1-Misc\LibPeriodicTable-3.1-Misc.lua
  1. LibPeriodicTable-3.1-Tradeskill\LibPeriodicTable-3.1-Tradeskill.lua
  1. Tablet-2.0\Tablet-2.0.lua
  1. Waterfall-1.0\Waterfall-1.0.lua
  1. LibStickyFrames-1.0\LibStickyFrames-1.0.lua

If these files are not inside **World of Warcraft\Interface\AddOns\AutoBar** then you have failed to download AutoBar correctly.  Please go to files.wowace.com to get the zip with what you actually need.


### How do I self cast or auto self cast? ###
  * For targeted items right click generally self casts
    * If you want to automatically cast items / spells on yourself when your target is not valid for that spell or item:
      1. Open up the Blizzard Interface Options Panel / Basic Options.
      1. Select "Auto Self Cast".


### How do I set key bindings for AutoBar? ###
  * Use the Blizzard key-binding interface:
    1. Open up the Blizzard Keybindings Panel
    1. Scroll down to the AutoBar section and bind the keys you want
  * To bind to your Custom Buttons, see the [Usage](Usage.md) section.


### AutoBar uses 5 gajillion gigabytes of memory? ###
  * This is not correct
    1. AutoBar uses about 400-500k
    1. AutoBar does use the embedded Ace libraries which load along with the first Ace mod which alphabeticaly tends to be AutoBar.
    1. The Ace libraries are shared among all your Ace mods.  If you want to get a better idea of who is hogging memory then load up the optional standalone versions of the Ace libraries.  Do not forget to delete them after your experiment is over.


### Waah, I don't want popups? ###
> Popups are either always shown, or only shown when shift is held down (as soon as I implement the shift part that is).

> The reasons are simple:
  1. Blizzard has systematically and thoroughly disabled automated choice during combat.
  1. AutoBar used to shuffle the items in a slot around based on cooldown, availability, etc.
  1. This shuffling can no longer work in combat.
  1. Therefore users need a way to in essence do this shuffling themselves, which means using the popup.
  1. Thus, the popup's availability is now mandatory.
  1. The only "hiding" of the popup will be the "Popup on Shift" key.
  1. To avoid support issues like: "I died / the raid wiped because I could not click on X potion after I ran out of Y" etc. the popup will just always be there. If you do run out of the first item there needs to be a fallback option during combat. So rather than allow users to break the mod through a "Disable Popup" option I am just not going to allow that. Popup on shift is close enough to hiding it.


### I can't see my Bar ###
  * Try a UI reload "/rl".
  * Enter Move the Bars mode to see where your bars are at.
  * Make sure your Bar's Alpha setting is high enough to see the bar.
  * If you have fadeout set for the Bar, hold down ctrl / shift / alt to make it visible again.  Make sure you have enabled one of these keys to show your Bar.
  * If you have changed your UI scale, the Bar may be positioned off the screen. Set **AutoBar/Clamp Bars to screen** then do a UI reload "/rl"


### My buttons shift around when items get used up ###
> Each Bar has various settings to control this.


### How do I get a cooldown count like <some mod> has? ###
  * AutoBar provides only the standard Blizzard cooldown clock. If you would like a digital cooldown, then get the [OmniCC](http://wow-en.curse-gaming.com/downloads/details/2775/omnicc/) mod.
  * OmniCC provides a digital cooldown for any button that has a standard Blizzard cooldown clock. I would highly recommend it.
  * A clock will never be added to AutoBar, because all I would be doing is copying the OmniCC code which makes no sense. Better to have one OmniCC, than 50 mods with duplicate OmniCC code in them.


