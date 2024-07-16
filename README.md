# about-the-income
# Define a function to calculate the highest possible income
def calculate_highest_income(base_salary, experience_years, education_level, skills_level, location_factor):
    """
    Calculate the highest possible income based on base salary, years of experience, education level,
    skills level, and location factor.

    :param base_salary: Base salary for the profession (annual).
    :param experience_years: Number of years of experience.
    :param education_level: Education level multiplier (e.g., Bachelor's = 1.0, Master's = 1.2, PhD = 1.4).
    :param skills_level: Skills level multiplier (e.g., Basic = 1.0, Intermediate = 1.1, Advanced = 1.2).
    :param location_factor: Location multiplier (e.g., City with high cost of living = 1.3).
    :return: Estimated highest possible income.
    """
    experience_multiplier = 1 + (experience_years * 0.03)  # 3% increase per year of experience
    highest_income = base_salary * experience_multiplier * education_level * skills_level * location_factor
    return highest_income

# Example usage
base_salary = 50000  # Example base salary in USD
experience_years = 10
education_level = 1.2  # Master's degree
skills_level = 1.1  # Intermediate skills
location_factor = 1.3  # High cost of living city

highest_income = calculate_highest_income(base_salary, experience_years, education_level, skills_level, location_factor)
print(f"The highest possible income based on the given factors is: ${highest_income:.2f}")
