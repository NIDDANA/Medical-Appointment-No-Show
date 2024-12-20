**Medical Appointment No Show Dataset Analysis**

**Dataset Description:**
This dataset contains information about 100,000 medical appointments in Brazil. It focuses on whether patients show up for their scheduled appointments. Each row includes details about the patient and the appointment.

**Columns Description:**
- **PatientId**: A unique identifier for each patient.
- **AppointmentID**: A unique identifier for each appointment.
- **Gender**: The gender of the patient (Male or Female).
- **AppointmentDay**: The date of the appointment.
- **ScheduledDay**: The date when the appointment was booked.
- **Age**: The patient’s age.
- **Neighbourhood**: The location of the appointment.
- **Scholarship**: Whether the patient is part of a government scholarship program (True or False).
- **Hipertension**: Whether the patient has hypertension (True or False).
- **Diabetes**: Whether the patient has diabetes (True or False).
- **Alcoholism**: Whether the patient has alcoholism (True or False).
- **Handcap**: Whether the patient has a disability (True or False).
- **SMS_received**: Whether the patient received a reminder via SMS (1 or more messages).
- **No-show**: Whether the patient showed up for the appointment (True or False).

**EDA (Exploratory Data Analysis) Questions:**
1. **How often do men go to hospitals compared to women? Which of them is more likely to show up?**
2. **Does receiving an SMS as a reminder affect whether a patient shows up? Is it related to how many days in advance the appointment was scheduled?**
3. **Does having a scholarship affect showing up for an appointment? Which age groups are affected?**
4. **Does having certain diseases affect whether a patient shows up? Does gender play a role?**

**Data Wrangling:**
The dataset is in the file `noshowappointments-kagglev2-may-2016.csv`. It contains 110,527 rows and 14 columns.

**Data Cleaning:**
- There are no missing values or duplicates.
- **PatientId** and **AppointmentID** are not helpful, so they were removed.
- **ScheduledDay** and **AppointmentDay** were converted to date format.
- A new column was created for "days until the appointment."
- **Gender**, **Scholarship**, **Hypertension**, **Diabetes**, **Alcoholism**, and **SMS_received** were converted to the appropriate data types (e.g., boolean).
- **No-show** was changed to boolean type.
- The **Handcap** column was cleaned to have only values 0 or 1.
- The **Age** column had inconsistencies, which were addressed.

After cleaning, the final dataset contains 110,521 rows and 11 columns.

**Data Visualization:**
Using **Matplotlib** and **Seaborn**, we created various charts to explore correlations between different features.

**Conclusions:**

1. **How often do men go to hospitals compared to women? Which of them is more likely to show up?**
   - Women make up almost half of the dataset and show up more often for their appointments than men. However, the higher percentage of women in the dataset might influence this.
   
2. **Does receiving an SMS as a reminder affect whether a patient shows up? Is it related to the number of days before the appointment?**
   - 67.8% of patients didn’t receive an SMS, but still showed up. There is a positive correlation between the number of days before the appointment and showing up. Patients with appointments 0-30 days away are more likely to attend, while those with appointments further in the future are less likely to show up.

3. **Does having a scholarship affect showing up for an appointment? Which age groups are affected?**
   - Having a scholarship doesn’t significantly affect showing up for appointments. The scholarship program includes a large number of young people, especially children.

4. **Does having certain diseases affect whether a patient shows up? Does gender play a role?**
   - Most patients do not have chronic diseases, but young people are more likely to have conditions like hypertension or diabetes. Having a disease may influence whether a patient shows up for an appointment.

**Built with:**
- JupyterLab
- Python 3
- Pandas
- Numpy
- Matplotlib
- Seaborn

This analysis helps us understand factors that influence whether patients show up for their medical appointments, such as gender, age, disease conditions, and reminders.
