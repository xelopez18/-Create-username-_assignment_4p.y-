# -Create-username-_assignment_4p.y-
student_name = "Xavier Lopez"
current_gpa = 3.0        
study_hours = 20          
social_points = 50        
stress_level = 30          


print(f"Welcome, {student_name}, to your college adventure!")
print(f"Starting GPA: {current_gpa}")
print(f"Study hours: {study_hours}")
print(f"Social points: {social_points}")
print(f"Stress level: {stress_level}")


print("\nChoose your course load:")
print("A) Light (12 credits)")
print("B) Standard (15 credits)")
print("C) Heavy (18 credits)")


course_choice = input("Your choice: ")


if course_choice == "A":
    study_hours += 5
    stress_level -= 5
    current_gpa += 0.1
elif course_choice == "B":
    study_hours += 3
    stress_level += 5
    current_gpa += 0.0
elif course_choice == "C":
    study_hours -= 5
    stress_level += 15
    current_gpa -= 0.1
else:
    print("Invalid choice! Default course load assigned.")
    study_hours += 2
    stress_level += 5


study_options = ["Programming", "Math", "English", "History"]
study_choice = input("\nWhich subject do you want to focus on? ")


# Use 'not in' for invalid choice handling
if study_choice not in study_options:
    print("Invalid study choice!")
else:
    if study_choice == "Programming" and current_gpa < 3.0:
        current_gpa += 0.3
        study_hours -= 3
    elif study_choice == "Math":
        current_gpa += 0.2
        study_hours -= 2
    elif study_choice == "English":
        social_points += 5
        stress_level -= 5
    elif study_choice == "History":
        stress_level += 5
        current_gpa += 0.1




print("\nFinal semester assessment!")
final_choice = input("Do you want to attend the big exam or skip it? (attend/skip) ")


if final_choice is not None:  
    if final_choice.lower() == "attend":
        if current_gpa >= 3.5 and stress_level < 50:
            ending = "Top student ending!"
        else:
            ending = "Average ending."
    elif final_choice.lower() == "skip":
        ending = "Bad ending due to skipping exams."
    else:
        ending = "Neutral ending."
else:
    ending = "No choice made."


print("\nYour final stats:")
print(f"GPA: {round(current_gpa, 2)}, Study Hours: {study_hours}, Social Points: {social_points}, Stress Level: {stress_level}")
print("Ending:", ending)
git add xavier_assignment_3.py
git commit -m "Pass Test Case 1: Initial game setup with required variables"
git push
