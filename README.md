# Node.js Developer Test

## Requirement

-   Create Web API and Database for fetching and storing patient records following given schema.
    -   to get all patient
    -   to get specific patient with details
    -   to create new patient
    -   to update specific patient 
    -   to delete specific patient (You able design soft delete.)

- Create Web API and Database for fetching and storing encounter record following given schema.
  - to get all encounters
  - to get specific encounter
  - to create encounter
  - to update encounter
  - to delete encounter (You able design soft delete.)

### Patient

| Column Name | Type     | Constraint |
| ----------- | -------- | ---------- |
| patientId   | uuid     | PK         |
| firstName   | string   | Not null   |
| middleName  | string   |            |
| lastName    | string   | Not null   |
| birthDate   | Date     |            |
| createdAt   | DateTime |            |
| updatedAt   | DateTime |            |

### Encounter (Visit History)

| Column Name         | Type     | Constraint      |
| ------------------- | -------- | --------------- |
| encounterId         | uuid     | PK              |
| visit               | DateTime |                 |
| discharge           | DateTime |                 |
| physicalExamination | LongText |                 |
| historyOfIllness    | LongText |                 |
| followUp            | Date     |                 |
| patientId           | uuid     | FK with Patient |

-   Separate file for controllers and services.

-   You can design file structure.
-   Deploy this microservice with `docker-compose` for extra score

PS. 
Sugest library
- Express.js for server framework lib.
- Prisma for ORM.
