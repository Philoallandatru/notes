```sql
CREATE TABLE athletes(
	id INTEGER PRIMARY KEY,
	name TEXT,
	sex TEXT,
	age INTEGER,
	height INTEGER,
	weight INTEGER
);

CREATE TABLE athlete_events(
	id INTEGER,
	team TEXT,
	noc TEXT,
	games TEXT,
	sport TEXT,
	event TEXT,
	medal TEXT
);

CREATE TABLE host_cities (
	games TEXT PRIMARY KEY,
	year INTEGER,
	season TEXT,
	city TEXT
);

CREATE TABLE regions (
	noc TEXT PRIMARY KEY,
	region TEXT,
	notes TEXT
);
```

