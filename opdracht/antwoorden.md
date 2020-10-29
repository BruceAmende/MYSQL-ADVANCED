# Antwoorden Eindopdracht

1. Copy paste je gemaakte SQL query hieronder
SELECT races.name AS "Grand Prix",  circuits.name AS "circuit_Naam" FROM races
LEFT JOIN circuits ON races.circuitId = circuits.circuitId
WHERE races.year = "2018" 

2. Copy paste je gemaakte SQL query hieronder
LEFT JOIN drivers ON driver_standing.driverId = drivers.driverId 
LEFT JOIN races ON driver_standing.raceId = races.raceId
WHERE races.year = "2017"
AND driver_standing.points = "10"
3. Copy paste je gemaakte SQL query hieronder
SELECT drivers.forename, drivers.surname, pitstops.duration FROM pitstops 
LEFT JOIN drivers ON pitstops.driverId = drivers.driverId 
WHERE pitstops.duration < "25"
4. Copy paste je gemaakte SQL query hieronder
SELECT constructors.name,  races.name AS "Grand Prix" FROM races 
LEFT JOIN constructors ON races.circuitId = constructors.constructorId 
WHERE constructors.name = "McLaren" 
AND races.year = "2018"
5. Copy paste je gemaakte SQL query hieronder
SELECT circuits.name AS "circuit_Naam",  circuits.country AS "circuit_Land", races.name AS "Grand Prix", drivers.surname FROM races
LEFT JOIN circuits ON races.circuitId = circuits.circuitId
LEFT JOIN drivers ON drivers.driverId = drivers.driverId
WHERE races.year = "1950"
AND drivers.surname LIKE "F%"
