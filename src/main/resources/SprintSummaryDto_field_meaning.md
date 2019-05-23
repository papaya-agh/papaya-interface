referencje do arkusza "Sprinty 1-*" w
[Google Sheets](https://docs.google.com/spreadsheets/d/1doM61VumfUt55nClxNOFGWuj_AwKxchnaSgl8A_BZ-4/edit#gid=872062564)

pola:

L2: `prevAverageSprintCoefficient`
backend, running average, cachowane

L3: `startDate`
backend, ze sprintDto, persystentne w sprint

L4: `endDate`
backend, ze sprintDto, persystentne w sprint

L5: `timeToAssign = totalDeclaredTime / prevAverageSprintCoefficient`
backend, nie persystentne

L6-L12: `declaredTime[]`
backend, z membersAvailabilityDto, persystentne w availability

L13-L19: `effectiveDeclaredTime[] = declaredTime[] / prevAverageSprintCoefficient`
backend, nie persystentne

L20: `estimatedTimePlanned`
podawany w dowolnym momencie w trakcie trwania sprintu
backend, persystentne w sprint

L21: `finalTimePlanned`
podawany przy zamykaniu sprintu
backend, persystentne w sprint

L22: `timeBurned`
podawany przy zamkykaniu sprintu
backend, persystentne w sprint

L23: `totalDeclaredTime = sum(declaredTime[])`
backend, nie persystetne

L24: `totalNeededTime = coefficient * finalTimePlanned`
backend, nie persystentne

L25: `coefficient = totalDeclaredTime / timeBurned`
wyliczane przy zamykaniu sprintu
backend, persystentne w sprint

L26: `currentAverageSprintCoefficient`
backend, running average, cachowane

`timeRemaining` i `estimatedTimePlanned` nie wpływają na obliczenia i są jedynie poglądowe
