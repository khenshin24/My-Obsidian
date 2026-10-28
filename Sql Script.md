

ALTER TABLE wfpprojects
ALTER COLUMN name TYPE VARCHAR(1000);


ALTER TABLE wfoactivities
ALTER COLUMN name TYPE VARCHAR(1000);





sql script 

ALTER TABLE orgunits
ALTER COLUMN code TYPE VARCHAR(20);


-- 1. Office of Human Capital Development
UPDATE orgunits
SET name = 'Office of Industry Manpower Development',
    code = 'OOIMD'
WHERE name = 'Office of Human Capital Development';


-- 2. Office of Tourism Development Planning, Research and Information
UPDATE orgunits
SET name = 'Office of Tourism Development Planning, Research and Information Management',
    code = 'OOTDPRAIM'
WHERE name = 'Office of Tourism Development Planning, Research and Information';


-- 3. Protocol and Engagements
UPDATE orgunits
SET name = 'Office of Assistant Secretary for Protocol and Engagement Unit',
    code = 'OOASFPAEU'
WHERE name = 'Protocol and Engagements';


-- 4. Tourism Regulation, Coordination, and Convergence
UPDATE orgunits
SET name = 'Office of the Assistant Secretary for Tourism Regulation, Coordination, and Convergence',
    code = 'OOTASFTRCAC'
WHERE name = 'Tourism Regulation, Coordination, and Convergence';