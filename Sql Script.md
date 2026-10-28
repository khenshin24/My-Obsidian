

ALTER TABLE wfpprojects
ALTER COLUMN name TYPE VARCHAR(1000);


ALTER TABLE wfoactivities
ALTER COLUMN name TYPE VARCHAR(1000);



Backend : PFIS-166  
.

.

.

- FROM: Office of Human Capital Development  
    TO: Office of Industry Manpower Development
    Code : OOIMD
    
- FROM: Office of Tourism Development Planning, Research and Information  
    TO: Office of Tourism Development Planning, Research and Information Management
    Code : OOTDPRAIM
    
- FROM: Protocol and Engagements  
    TO: Office of Assistant Secretary for Protocol and Engagement Unit
    Code : OOASFPAEU
    
- FROM: Tourism Regulation, Coordination, and Convergence  
    TO: Office of the Assistant Secretary for Tourism Regulation, Coordination, and Convergence
    Code : OOTASFTRCAC


sql script 

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