# Catalog-Hackathon-4

####CHILD VACCINATION MANAGEMENT SYSTEM:
Child vaccination is a huge challenge which is being faced by parents to enhance their chiLD's immune system and to reduce the risk for infectious diseases.In this particular scenario we majorly focus on the easy scheduling of child vaccination.

MAJOR CHALLENGES FACED DURING CHILD VACCINATION:
1)Healthcare Infrastructure
2)Cost
3)Lack of awarness
4)misinformation
5)Fear of side effects

------------------------>We try to implement the code for easy scheduling of child vaccination by using the childs's professional and personal data.
The major objective of this is to implement it in a user-friendly manner.

------------------------>CODE FOR IMPLEMENTATION:

Two functions are being implemented in this code one is for calculating the vacination schedule and the other is to print the vaccination schedule.
We take the child's birth date as input and the schedule is printed accordingly.

from datetime import datetime,timedelta
def calculate_vaccination_schedule(birth_date):
    schedule ={
        "Hepatitis B (1st dose)":birth_date+timedelta(weeks=0),
        "Hepatitis B (2nd dose)":birth_date+timedelta(weeks=4),
        "DTaP (1st dose)":birth_date+timedelta(weeks=8),
        "DTaP (2nd dose)":birth_date+timedelta(weeks=16),
        "DTaP (3rd dose)":birth_date+timedelta(weeks=24),
        "MMR (1st dose)":birth_date+timedelta(weeks=52),
        "Varicella (Chickenpox)":birth_date+timedelta(weeks=52),
        }
    return schedule
def print_vaccination_schedule(schedule):
    print("\nVaccination Schedule:")
    for vaccine,date in schedule.items():
        print(f"{vaccine}:)
def main()
birth_date_str=input("Enter the child's birth date (YYYY-MM-DD):")
    try:                                                                                 /////Calculating and displaying the vaccination schedule
        birth_date=datetime.strptime(birth_date_str,"%Y-%m-%d")
        schedule=calculate_vaccination_schedule(birth_date)
        print_vaccination_schedule(schedule)
        
except ValueError:
        print("Invalid date format.Please enter the date in YYYY-MM-DD format.")
if __name__=="__main__":
    main()


****IF THE DATE OF BIRTH OF A PARTICULAR CHILD IS TAKEN AS INPUT THE TOTAL VACCINATION SCHEDULE WILL BE PRINTED ACCORDINGLY.THIS MAKES THE VACCINATION TASKS EASIER.




