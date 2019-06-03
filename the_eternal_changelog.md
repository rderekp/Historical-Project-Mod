# The Eternal Changelog

This file is not for the faint of heart. It details every single change ever made to the mod. It's likely full of typos and mistakes.

***

## v0.4.4 - 17/05/2019

* Event 90057 - Look to $COUNTRYNAME$ should no longer fire for vassal states, since these can't be taken from sphere.
* Fixed province 2103 - Philippolis being in the rows for RGO change for coal and iron, making it constantly flip between both. It will stop on Coal now.
* Fixed the "Living Space" event to make sure it gives a proper CB, even when bordering colonial nations. The event wont target neighbouring fascist countries anymore (or fire if your country is dismantled), to help these countries end up more or less aligned rather than quarrelling all the time. To avoid it giving several CBs in different nations, the event now fires another event to a given nation, which gives the CB: if they have more than 4 states and are not a colonial nation, you get the a Demand Concession CB. If they have more than 4 states and are a colonial nation, you get a place in the sun CB. If they have less than 4 states, you get a conquest CB. So a fascist nation works through colonies before going to core territory and finally conquest with these events. The amount of infamy you get was made random from 1 to 3. Added an option to ignore the event, which will anger the jingoists and the fascists.
* Fixed several vanilla and HPM typos in inventions and events.
* Changed Dismantlement so vassals and landlocked nations can't participate in colonial dismantlement. Changed the old NNM dismantlement (that still lives on, based on states rather than countries) to a quarterly OnAction event, so it only happens last (and guarantees any colony that needs to be distributed as a country will be so).
* Recognize Circassia/Chechnya/Dagestan decisions will disappear after 1840.
* Reworked the Limburg crisis to be less convoluted. Instead of keeping Limburg free throughout it, the Dutch will annex the country and the Germans will choose how to react. If they press their claim, they will get a one year core in the province (acting as a claim), and they can choose to go to war to press their claim. Regardless of the outcome, after one year and in the next quarterly pulse they will lose their core there - regardless if they own the province or not. If they do own the province though, it will be renamed to Limburg. Reworked AI logic when picking options on the chain, made infamy gain a bit random for the Germans and made it so annexing Limburg is a decision rather than an event.
* Fixed the Laos protectorate decision so you can't create a landlocked colony.
* Fixed a vanilla bug with the brigades_compare localization that could show the wrong country being the target of a fired event (inside an event).
* Added Laos, Cambodia, Burma, Vietnam and Malaysia (only the 2 states in "mainland Malaysia") to the Imperialism CB. To use it against native countries in these regions, the country needs revolution and counterrevolution and for it to be after the Berlin Conference. There are special requirements - declaring Indochina as a colony (decision) for Vietnam, Laos and Cambodia. Being crowned emperor of India for Burma. Owning Delhi, Calcutta and any Burmese core is an exception for Burma since only the UK can take the empress decision. Malaysia is only active for the owners of Singapore and any country that owns a province in Cambodia proper can go after the Cambodian state. Hopefully this will make the AI more aggressive when colonizing SE Asia. Also note that the Imperialism CB is exclusive to European powers.
* The above also means that the decision to "create" Indochina is not exclusive to France anymore (and now it has a big red warning to let players know its useful to take it and get a CB). The recurrent event that France got to conquer Vietnam/Laos/Cambodia was scrapped out and only the imperialism CB is left now. This means that conquering Indochina is not something France has an advantage for, it depends on the competing powers in Vietnam - either owning Saigon or Hanoi will let you take the decision. Made the decision inherit Vietnam if its in the sphere of the one who takes it and both have very good relations.
-Moved province 2572 - Nan from the Shan states to the Ayutthaya state. To leave the states more or less balanced moved 1353 - Ratchaburi from Ayutthaya to Pattani
-Made the decision to Annex Champasak not exclusive to France anymore. Made it appear more frequently (so the player knows what is needed) and made the requirements a bit more diverse. It does need the player to use the "create Indochina" decision, though.
-Made negotiating an unequal treaty (a decision) with Vietnam and the border treaty with Thailand not exclusive to France anymore. This mean any GP can get Saigon now, as long as they fulfil other requirements. These decisions now have a 50% chance of giving 1 Infamy.
-Changed the decision to annex Laotian minors/Cambodia require the "Indochina" decision. So to annex these minors through decisions, you need to have declared the intention to form Indochina. Made these decisions have a 50% chance of giving 1 Infamy when you take them.
-Similar to the decision to integrate the laotian minors and Cambodia, added a decision to annex Vietnam if you own a Vietnamese core, have Mass Politics and they are in your sphere.
-As a final reminder, these decisions dealing with Indochina/SE Asia as well as the use of the Imperialism CB in the region require the "$Country_ADJ$ Indochina" Decision to be taken. These and the other decisions dealing with Indochina can be taken by any European GP and Japan except Turkey and Russia. Turkey, Russia and other GPs need the "Sea power & The Merchant Marine" tech school to be able to use these decisions.
-If Russia is dismantled without the participation of Japan, Japan will still get cores on the rest of Sakhalin - but it won't remove Russian cores. 
-Fixed the recurrent event for the integration of the Malay minors being able to fire too soon instead of when leaders died.
-Made the "Freedom of Religion" act decision be applicable to the Netherlands too.
-Made the Netherlands a semi-constitutional monarchy. Changed the Party reforms to Harassment and the voting one to Weighted Wealth. Citizen (voting) Rights were restricted to Primary culture only. Based on https://en.wikipedia.org/wiki/States-Provincial and https://en.wikipedia.org/wiki/United_Kingdom_of_the_Netherlands#Constitution_and_government
-Removed Flemish as accepted from the Netherlands. They can get it back passing a decision that requires a few things and burn through some prestige. This is done to represent better the catholic/protestant divide and the reasons that led to the Belgian revolution, as well as keep the Belgians more rebellious rather than being immediately accepted by the Netherlands.
-Moved Sociology and Political Science inventions to Biologism. Removed 30% education efficiency from Darwinism and distributed it equally to Social Science and Social Alienation.
-Reduced Ottoman minority CON/MIL gain and increased the tax efficiency of the initial ottoman policy.
-Fixed a bug in the EIC minimod that would make the EIC be integrated soon after it appeared.
-Changed 805 - Salonika from Cattle to Cotton and 767 - Maribor from Wood to Coal and 768 - Ljubljana from Cotton to grain. Greece changes based on "Land Tenure and Related Sectors of the Balkan Economy, 1600-1800" and Slovenia changes based on https://www.erih.net/how-it-started/industrial-history-of-european-countries/slovenia/
-Changed picking Tech School to not depend on Party ideology but party policies, mostly mimicking the already existing issues needed. The only exception is the Avantgarde Intelligentsia, which depends on literacy, consciousness and prestige. Also made AI countries with Revanchism not pick pacifist tech schools while communist countries won't pick the more Commerce tech schools. This should make choices more dependent on current situation - an AI country with unclaimed cores will be more likely to go after military-industrial complex.
-Refusing to go through any of the Opium Wars will now reduce the prestige of Great Britain by one fourth and will also dictate monetary reparations.
-Made all events and decisions where the player will pay something with the debt system properly show a red number telling them how much it will cost, to avoid confusion over bugs not debiting the money or money disappearing. Do note that if you don't have the money, the debt system kicks in and takes the money from your country, automatically, in instalments of 10k per payment, until the debt is paid in full. You will receive no warning about this.
-Reshuffled states in Burma and Thailand so they are a bit more balanced. Removed the Shan state that straddled both countries.
-The decision to establish a protectorate over Sarawak is no longer exclusive to the UK - any country can take it as long as they own the lands surrounding it (and sphered the country).  The decision has a 50% chance of giving 1 infamy.
-Increased the MTTH of the event for communist countries that gets rid of the Rich strata from 15 days to 60 months. This should allow pops to run, stop quick revolutions from causing lasting damage and it will represent the time that it takes to organize all this. Also added an option to not touch the capitalists, which will anger communist pops.
-Players should get an event letting them know when the Imperialism CB becomes available to them.
-Reshaped provinces in Armenia, Iran and Afghanistan. Re-divided the 2 Afghan states in North Afghanistan and South Afghanistan. Repurposed province 2133 - South Georgia into Gizab, in Afghanistan. South Georgia was a small arctic island that the UK could colonize.
-Revamped Terrain in the southern Caucasus, Iran and Afghanistan. The Zagros mountain range should be in now, and these 3 regions are much more mountainous than before. Reshaped the coast of Iran to reflect the changes, changed terrain to dry versions when appropriate. Terrain work was based on https://upload.wikimedia.org/wikipedia/commons/9/91/Iran_topo.jpg & https://4.bp.blogspot.com/-63r9Xbbxqm4/U1_4zuTY6VI/AAAAAAAABTw/QNIQICkhgNY/s1600/Afganistan-Kraj-G%C3%B3rski.jpg & https://upload.wikimedia.org/wikipedia/commons/d/db/Turkey_topo.jpg
-Added events for bankrupt countries to randomly lose infrastructure: railways, forts and ports.
-Increased countries base tax and admin efficiency by 5%.
-Fixed a bug in the NNM dismantlement code where, if Germany was dismantled, it didn't check if France (that owned Western Rhineland/Palatinate) had a truce (with Germany) and it ended up releasing Rhineland as a vassal even if France wasn't involved in the war. Also fixed a bug where Easter Rhineland was considered part of Wester Rhineland, effectively meaning that, even if France controlled Western Rhineland and the Palatinate, they would still release Rhineland as a puppet.
-Made so Eupen-Malmedy only goes to the owner of Liege if the owner of Liege has a truce with Germany.
-Changed INVENTION_IMPACT_ON_DEMAND from .15 to .13. Reverted mechanized_fishing_vessels bonus from 40% to vanilla 50%.
-Fixed a bug on the changes to vanilla that made it easier for accepted pops to migrate to colonies: they weren't really working, so colonial migration was working as vanilla. It is working now, so accepted pops will behave as primary pops when deciding to move to the colonies.
-Changed the Bureaucrats percentage in Michigan from 0.4% to 0.6% and in Arkansans from 0.23% to 0.8%. This should enable them to become states sooner.
-Egypt should correctly lose cores on Adana when they lose the Oriental crisis.
-Added Somalia to the "Colonial Claim" system during the Scramble for Africa.
-Deactivated the Imperialism CB in Mozambique after the Scramble starts.
-The event that changed the party_appointed reform for non-dictatorships will now fire if there's voting, not only if the government is controlled by liberal or by socialists. It will also move the UH reform to "population equal weight" in democracies, instead of making it "appointed".
-Stopped the "Trade for Heligoland?" event giving Kenya AND two Tanzanian provinces to the UK. Now it will only give Kenya or - if Germany doesn't own Kenya - make Germany pay 100k£.
-Venice should move their capital to Venice if they own it and it's not the capital.
-Separated the modifier for Substate nations in 2 - one for the AI and one for the player. The player is not forced to set minimum tariffs or taxes. Reduced the tax efficiency effect of both and the minimum tax for the AI.
-Moved Corfu to the Thessaly state.
-Made an event for Boer minors where an overlord that doesn't own Cape Town or for Indian Minors that A) are neighboured by a GP but not neighboured by their overlords or B) were recently released as the result of the dismantlement of their former masters to choose to: 1) become a puppet of the neighbouring GP, 2) declare independence, 3) join a neighbour of the same culture group and 4) keep the status quo.
-Yemen will be created with slavery abolished if the country that organizes it has slavery abolished.
-African colonies can now be organized with fewer states controlled. If you control half the states, you can usually organize it.
-When dismantling a nation that owns parts of another nation's colony (e. g. dismantling the UK who controls part of Mozambique and Portugal is the one who took the "organize colony" decision for Mozambique), those colonial territories will be given to the master of that colonial nation (the UK would give their Mozambique cores to Portugal) regardless if they have a truce or participated in the war. What that means is that dismantling will gravitate towards completing partial colonies, instead of perpetuating them.
-Restricted CB use during Mexican-American War/Oriental Crisis/French Expedition in Korea. What this means is that, during these scripted wars, the nations involved can only target the nation (like the US targeting Mexico) with the original CB. This is mainly done so the AI doesn't end up adding other unnecessary CBs (like the US adding acquire core CBs), but the restrictions are also applicable for the player. Made the acquire_all_cores CB cost less warscore since the AI never reached the required amount of warscore in the one instance it was used (mexican-american war) and white-peaced because of it.
-Changed event 30000 - Organizing a World Fair from taking money directly and instead made it use the debt system. This is mainly to stop the AI going bankrupt over the event, which happens not infrequently.
-Choosing to take Rhodes during the Italo-Turkish war will only give infamy if they can give you Rhodes.
-Removed the old NNM event meant to represent the Italo-Turkish war as it was obsolete. Made the option to demand Rhodes not given infamy if the turks can't give it (because they don't own it).
-Fixed the "Hegemony over the Nile" event chain not working properly.
-Slight adjustments to help the AI during the Texan Revolution.
-Moved Serbia's capital to Kragujevac at the game start. They can move it back through a decision.
-Carlist/Christino sympathies will no longer sap Spain's prestige.
-Reduced the amount of prestige you get from annexing core countries/states.
-Made a few modifiers such as Caudillos and "the_big_army" have a prestige downside. During the fight with the PBC Chile and Argentina will now get the "Caudillos" modifier.
-Made Ottoman starting prestige on par with Spain's.
-Increased all GPs starting prestige by 30, to compensate for the prestige gained in the initial wars in SPs.
-Reduced the frequency of the "A Treatise on Economics" Event.
-The End of the Liberal Revolutions event should now give 5 or 10 prestige instead of 5 or 15.
-Reduced the prestige that Denmark gets from a few vanilla flavour events. Most of their prestige spam came from these and liberal revolution events.
-Fixed the events from the Vanilla/NNM Liberal Revolutions so when they move an issue in a direction, it moves only one step over the current level. For example: If you have landed voting, the event would (previously) move pops 10% to universal voting, which is useless since no pop can support that since it's not the next reform. Now instead the event will move pops 10% to the next level (in the case of landed voting that would be "weighted wealth").
-Repurposed province 1813 - Arlit from the Sahara to be Hasakah, in Syria.
-Removed Vanilla Lakes Razzaza and Tharthar from the map, since both are artificial lakes created in the 20th century.
-Rework of terrain and provinces in the Middle East: the areas claimed by the Ottoman Empire/Saudi Arabia but not de facto under central authority were made into unoccupied provinces. These can be colonized by decision later, with cores being distributed according to current cores in neighbouring provinces. Several provinces had their terrain changed to reflect the arid conditions of the area. Kuwait will start independent but on the Ottoman sphere. Based on "Kuwait: Anglo-Ottoman Relations 1890-1914" found in https://shodhganga.inflibnet.ac.in/bitstream/10603/14230/11/11_chapter%204.pdf
-Added an event related to the history of Kuwait.
-Reworked the decision to claim the Arab Coast (as in Arab Gulf) for the Ottomans - now it doesn't require the Ottomans to be a GP, but there are other requirements. The decision will vassalize Kuwait if it's in the Ottoman's sphere of influence, with a later decision to inherit it if it's vassalized. The decisions and the decisions surrounding the Ottoman Expansion in Qatar and Bahrain have been reworked to be more dynamic and also to apply to Egypt.
-Reworked the events dealing with British intervention in the Qatar-Bahrain war. Now the UK gets a "make puppet" CB in Bahrain, to represent their protectorate there that was part of the peace deal.
-Added 1163 - Qatif and 1164 - Hufuf to the Abu Dhabi state. Renamed the state to "Arabian Gulf" - this is so any country with cores in those provinces can conquer them without needing to conquer Riyadh.
-Fixed a wrong modifier in "rebel_types" who should make non-liberal controlled but very politically liberal governments be less likely of being target to a Jacobin uprising.
-Organizing Madagascar will make the "end the merina monarchy" decision unavailable.
-Added an option to refuse independence for South Africa and not have the event repeat again.
-When using the "Claim Savoy" decision, France will fire an event to the owner of Savoy demanding the provinces. If refused, France gets lower relations and break any alliances. If accepted, cores (Italy/S-P) are removed from Savoy and the provinces are transferred to France.
-If Galicia-Lodomeria is landlocked out of Austria, Austria will release it. Bukovina will also be released not as a vassal but as an independent state.
-The decisions to integrate Bahrain/Qatar in the trucial states now require mass politics and will only show if you sphere either of these.
-Fixed a bug that was stopping Polish minors from ever using the "Unite with Poland" Decision.
-Minor rework of the Tonghak rebellion event chain: CBs given will be appropriate to country status (so no "add to sphere" for non GPs). Instead of it always ending with Korea puppet by someone, I made an option for Korea to retreat to Pyongyang, moving the capital there and starting a war with however is trying to puppet Korea. According to a random chance beforehand, representing how successful the initial invasion was, Japan might start this was already owning Inchon and Hanseong. This chance is drastically higher if the Chinese choose not to intervene. Now this intervention might lead to a 3 way war with Japan and China trying to puppet Korea (separately) and Japan and China fighting over that.
-If by 1870 Egypt is not civilized, not in anyone's sphere and is either free or their overlord is not a GP, then the #1 GP can take a decision to seize the province and build the canal.
-Fixed the event that removes party loyalty after 1845. It wasn't working like it was supposed to.
-Stopped the January Uprising event chain giving Congress Poland non-polish cores just because polish was a majority in the province.
-When NGF forms (through the normal decision), Austria gets the option of shifting their focus, abandoning their sphere in the German states and focusing in the Balkans, raising their relations with the NGF and removing their German Sphere, or they can keep everything they have and ignore this.
-Increased Egypt mobilization bonus from the Muhammad Ali reforms from 9% to 14%
-Removed all (but one) hard exclusions (based on tags) to the Liberal Revolutions events. Only exception is the United Baltic Duchies, which still have a hard ban. Reworked the time the event takes to fire to take into account unemployment, industrial score, closed borders, as well as press and meeting reforms.
-Slight reshape in 3 provinces in Sudan/South Sudan.
-Added a naval base in Galway, Port Elizabeth and Aden in 1836.
-Techs: Redistributed RGO production bonus for Coal and Iron, starting at bessemer process, so production increases earlier. Slightly boosted "cotton gin" and made the US start with it.
-Added a few more optional requirements for the Congo Conference decision: made it easier for Belgium and countries with the Naval tech school to take the decision. Changed the date that "The Dark Continent" unlocks from 1895 to 1890 if there's no conference.
-Every time a Semi-Constitutional or Constitutional Monarchy changes the ruling party outside a election - that is, the monarch uses its power to overrule the election result - a constitutional crisis event will fire that will reduce prestige, plurality and add militancy as well as a modifier. Players in democratic governments should use the party loyalty NFs to swing the elections in favour of the party they favour. 
-Non Prussian-formed Germany will not get the decisions to Appoint Bismarck, Rename Kaiser-Wilhelms land, Appoint Von Moltke, or get the Prussian tech-school. Italy can't use Cavours diplomacy if not formed by S-P.
-Made the "Academia Della Crusca" decision not bankrupt Tuscany.
-Japan is now exempt from paying tribute to the Shogun.
-The League of Three Emperors should be more likely to succeed. Germany should also break their alliances with other GPs during (and if someone accepts) the formation of the League, instead of only Austria/Russia doing it.
-Added a few more aristocrats/bureaucrats/officers to Yemen and the Gulf states.
-Made so the Ems Dispatch decision will not be taken by the AI the moment NGF forms. This is done so the Franco-Prussian war doesn't start immediately while the AI is unprepared because the AI can't contain themselves.
-Stopped the AI from using the AI-only CB "Unification Humiliate" against Austria-Hungary.
-Minor state rework in Persia. Merged Luristan and Lorestan in a single state. Moved 1134 - Dekhord from the state of Isfahan to Fars.
-Joined Olomouc and Troppau, in the Sudetes region, with Bielsko and Teschen in Austrian Silesia to make the state of Lower Silesia (based on https://en.wikipedia.org/wiki/Austrian_Silesia)
-If Krakow was integrated in Galicia-Lodomeria, they will lose their core once Austria turns into Austria-Hungary or if Austria uses the "Restore Empire" CB on them.
-Changed so Luxury, Medium and Common factories use Steel to be built rather than iron. Basic and cheap factories as well as steel works still use iron though.
-Changed Aruba to be a gold producing province from the start (based on https://www.britannica.com/place/Aruba ). Lille, in France, will start producing iron from 1860 onwards.
-Fixed pops in the Ionian islands (Greek, British, North Italians and Sephardi pops). Change RGO in both islands to fruit. Changed party names to historical names or greek party names. Added North Italian and British as accepted - something they lose if they ever acquire non-cored territory. The Ionian Islands will start as a Constitutional monarchy. Added some Sephardi pops to Athens. Based on the detailed and spectacular work of anon here https://web.archive.org/web/20190517113659/https://pastebin.com/bysiU0rm
-Removed Transylvania from the "End of the Federation - Totalitarian" Danubian Federation event. Tried to make sure it doesn't start wars with countries that doesn't exist.
-Added a decision to rename the Bourbon island to Île de la Reunion if you're a republic. It can also be renamed to Island Bonaparte if you're the Second Empire.
-Changed Krakow's population to around 140,000 (35,000 pops) from the previous 100,000 pops (source: https://www.britannica.com/place/Republic-of-Cracow)
-Changed "Open Hearth Furnace" to unlock in 1885.