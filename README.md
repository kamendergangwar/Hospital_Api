# Information about API:
### Theme:
- We’re going to design an API for the doctors of a Hospital which has been allocated by the
govt for testing and quarantine + well being of COVID-19 patients
- There can be 2 types of Users
- Doctors
- Patients
- Doctors can log in
- Each time a patient visits, the doctor will follow 2 steps
- Register the patient in the app (using phone number, if the patient already exists, just
return the patient info in the API)
- After the checkup, create a Report
- Patient Report will have the following fields
- Created by doctor
- Status (You can use enums if you want to):
- Can be either of: [Negative, Travelled-Quarantine, Symptoms-Quarantine,
Positive-Admit]

- Date

# Instructions about SetUp:

First start with downloading the code and and write npm install on code editor, it will install all dependencies on your editor.
You will need a code editor and mongoDB setup on your computer.
We will use postman to check the api is working or not,So download postman on your computer.

## How to USE?

URL: ` http://localhost:5000/api/v1`

#### End Points:
1. `/doctor/register`(POST): Register the new doctor using name,email and password(all requireds).
- INPUT:

![](/Images/1.png)

- OUTPUT

![](/Images/2.png)

2. `/doctor/login`(POST): Doctor can Login using email and password.

- INPUT:

![](/Images/3.png)

- OUTPUT(Generate JWT Token)

![](/Images/4.png)

3. `/patients/register`(POST): Doctor can Register the patient using name and Phone Number.

#### Need for further use:

![](/Images/5.JPG)

- INPUT:

![](/Images/6.JPG)

- OUTPUT

![](/Images/7.JPG)

4. `/patients/:id/create_report`(POST): Doctor can create report of the Patients.

#### Need for further use:

![](/Images/8.JPG)

- INPUT:send status([0:Negative, 1:Travelled-Quarantine, 2:Symptoms-Quarantine, 3:Positive-Admit]) and doctor id 

![](/Images/9.JPG)

- OUTPUT

![](/Images/10.JPG)

5. `/patients/:id/all_reports`(GET):Retrive all reports of a patient by ID.

- OUTPUT

![](/Images/11.JPG)

5. `/reports/:status`(GET):Retrieve all reports from DB filter on the basis of Status sent in params.

- OUTPUT 

![](/Images/12.JPG)


# DEPLOYEMENT
Project already deployed on Render.com(For better exp: use Postman for accesing above Routes)

Do Visit: 
