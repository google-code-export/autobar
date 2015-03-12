# Hiding AutoBar #
  * Fade outside combat (after say 20 seconds)
  * Popup on shift, this is for the popups only.
I think this would be a useful feature because running around in alt-z mode is really nice so something close to that in the regular interface but with the minimap showing would rock. This becomes easier in 2.1 with better alpha support.

# Buttons #
  * Plugin architecture so buttons can be more customized.
  * Buttons could handle inventory for certain items like buff consumables, pots, ammo etc.
  * Instance / Boss settings would be nice. This requires some kind of general ACE mechanism for determining who we are fighting.
  * Buff detection: grey out buff items if user already has that buff. This is a lot of work involving matching buff type with items that give it.
  * Deal with charges: display them & use smaller charged items first.
> ### Crafting Buttons ###
    * This is a good idea, but the crafting API is just so cruddy...
> ### Drag Button ###
    * A button that you can directly drag items onto from inventory without opening up config
> ### Mount Button ###
    * Handle flying vs ground.
> ### Pet Food Button ###
    * Custom food blend for your pets food preferences.
    * Maybe have an unhappiness outline so you know to feed the poor thing b4 it runs away.
> ### Shaman Totem Buttons ###
    * Need to add indicator of active status
> ### Always popup option ###
    * I think this would be a great button specific option, for buttons such as combined mana regen, where you go through different pots, mana gems etc in a fight. Allowing a single button to remain expanded would allow MUCH quicker clicking through these.
# More Better PT3 #
    * PT3 use is pretty shallow at the moment. This can be extended to use PT3 sets directly instead of custom AutoBar sets. This gives AutoBar access to sets in PT3 from other mods like Baggins for instance.
    * This would also entail some PT3 browsing & picking code.
    * Ideally PT3 would be able to handle metadata to facilitate this. Theres a discussion on PT3 about this.
# Data versioning & verification #
    * Version AutoBar data & explicitly upgrade & leave behind obsolete stuff. This is now implemented.
    * Verify the data is not corrupt
    * Hopefully this would avoid people needing to delete the AutoBar WTF files instead of just using Reset on the profile page and/or /script ReloadUI()

