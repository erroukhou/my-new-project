# Smart School Orientation System

Final project for the Building AI course

## Summary

This project aims to develop an AI-driven system to assist students in choosing the most suitable academic path based on their skills, interests, and career aspirations. By analyzing student data and preferences, the system provides personalized recommendations, improving educational outcomes 


## Background

Choosing the right academic path is one of the most critical decisions for students, yet many struggle due to:
* Lack of proper guidance
* Insufficient understanding of their strengths and career opportunities
* Mismatch between skills and chosen fields.
  This problem is widespread in schools, especially where resources for professional guidance are limited. As someone passionate about education and technology, I believe AI can democratize access to tailored school orientation and help students make informed decisions.


## How is it used?

The system works as follows:

* Data Input: Students input their grades, skills, interests, and future aspirations through a web or mobile interface.
* Analysis: The AI analyzes their data and matches it with profiles of successful individuals, career trends, and academic requirements.
* Recommendations: The system suggests potential academic paths and career options, providing reasoning and resources for each recommendation.
![AI School Orientation](images/AI.webp)

This is how you create code :
```
def recommend_academic_path(grades, interests):
    """
    Recommends an academic path based on grades and interests.
    
    Parameters:
    grades (dict): A dictionary of grades for subjects.
    interests (list): A list of interests.
    
    Returns:
    str: Recommended academic field.
    """
    recommendations = {
        "Science": ["Math", "Physics", "Biology", "Chemistry"],
        "Technology": ["Programming", "Robotics", "Engineering"],
        "Arts": ["Literature", "History", "Art"],
        "Business": ["Economics", "Management", "Accounting"],
    }

    # Calculate average grade
    avg_grade = sum(grades.values()) / len(grades)

    # Match interests with recommendations
    for field, subjects in recommendations.items():
        if any(interest in subjects for interest in interests):
            if avg_grade >= 70:  # Minimum grade threshold
                return f"We recommend you explore the {field} field based on your interests and grades."
    
    return "We couldn't determine a specific recommendation. Consider exploring more diverse fields!"


# Example input
student_grades = {
    "Math": 85,
    "Physics": 78,
    "Biology": 75,
    "Chemistry": 70,
    "Literature": 60,
    "History": 55
}

student_interests = ["Math", "Physics"]

# Recommendation
recommendation = recommend_academic_path(student_grades, student_interests)
print(recommendation)

```


## Data sources and AI methods
The project leverages various data sources and AI techniques:
Data Sources:
*  School performance records.
*  Online surveys assessing interests and skills
AI Methods:
# Natural Language Processing (NLP) to analyze student inputs and career profiles
# Collaborative filtering for personalized recommendations
# Decision trees and neural networks for classification and prediction 
| Source            |       Description              |
| -----------       | -----------                    |
| School databases  | Academic performance data      |
| Career databases  | Job market trends and skills   |

## Challenges

What the project doesn’t solve or limitations:
*  The system might not be able to account for sudden changes in job market trends.
*  Privacy concerns around student data need to be addressed with robust security measures.
*  AI biases in recommendation systems could lead to suboptimal guidance if not properly calibrated.

## What next?
Future directions for this project include:
Integrating real-time updates from job markets to enhance recommendations.
Adding a mentorship program where students can connect with professionals in their chosen fields.
Expanding language support to make the system globally accessible.
 


## Acknowledgments

* Inspired by my interest in education and AI.
* Special thanks to educators and mentors who provided insights into student counseling challenges.
 
















