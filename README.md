Introduction: this project focuses on the places on the campaign route of Sunni Ali, the first king of the Songhai Empire in West Africa. 

Goals: Use Google Earth, GeoName, and Wikipedia to locate places occurred on the military journey of Sunni Ali in Tarikh al-Fattash. Reconstruct geographical data and a timeline based on the text. Store the data in the .yml format for future use in the new perseus.tufts.edu. 

Sources: Tarikh al-Fattash; comments from the English edition by Wise and Abu Taleb

Choice of language format: 
YAML (.yml) or JSON (.json) each has its own pros and cons for developers using different languages. Compared with JSON, YAML is commonly deemed to be a data-representation language easier to visually read for human readers and hence I chose it for this project. It can also be converted to JSON if needed in the future. 

YAML file explained: 
1.	Title: the name of the place in the text of Tarikh Fattash (edition?)
2.	Type: settlement, river, lake, province
3.	url: Wikipedia, GeoName; or other relevant website if the previous two platforms do not offer any information.
4.	data: 
a.	otherNames: modern or alternate names
b.	ifPolygon: True if the place cannot be pinpointed as a point on the map; it is rather an area, a country, or a province. False if it is a place that can be pinpointed as a point with coordinates. 
c.	coordinates: latitude, longitude. For places as a polygon, the author gives a description in the commentary about how much this polygon covers and coordinates of where the center of this polygon is. 
d.	modernCountry: in which modern country this place is located 
e.	frequency: how often this place is mentioned in Tarikh Fattash
f.	ifCampaign: True if Sunni Ali has been to this place on the way of his campaign; False if this place is mentioned for the sake of additional knowledge.  
g.	confidence: this entry is evaluated into three levels: 1, 2, and 3. For 1, it denotes full confidence with which we connect the place mentioned in the text with coordinates on the map. 2 denotes ambiguity: the name of a place could match with a modern location, but the author cannot be sure based either on the texts or commentary of Wise and Abu Taleb. 3 denotes absolute uncertainty, which means the author cannot locate the place. 
h.	commentary: include the author’s commentary, explaining why we choose the coordinates; include commentary of Wise and Abu Taleb

