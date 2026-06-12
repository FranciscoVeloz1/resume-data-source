# Francisco's resume source data

This project is the source data for Francisco's resume, including experience, education, certificates, achivements, etc... This data is consumed by Francisco's web porfolio and resume.

## Data structures

The data is coded as a JSON with the next structure:

```JSON
{
  "profile": {
    "firstName": "",
    "lastName": "",
    "fullName": "",
    "email": "",
    "profilePhoto": ""
  },
  "summary": "",
  "workExperience": [
    {
      "position": "",
      "company": "",
      "duration": "",
      "location": "",
      "logo": "",
      "responsibilities": [],
      "skills": []
    }
  ],
  "projects": [
    {
      "id": 0,
      "name": "",
      "date": "",
      "link": "",
      "repo": "",
      "video": "",
      "demo": "",
      "skills": [],
      "description": "",
      "image": ""
    }
  ],
  "certifications": [
    {
      "name": "",
      "issuer": "",
      "date": "",
      "link": "",
      "logo": "",
      "description": ""
    }
  ],
  "education": [
    {
      "degree": "",
      "institution": "",
      "duration": "",
      "location": "",
      "logo": ""
    }
  ],
  "achievements": [
    {
      "title": "",
      "description": "",
      "date": "",
      "image": ""
    }
  ],
  "idioms": [
    {
      "language": "",
      "proficiency": ""
    }
  ],
  "socialNetworks": [
    {
      "platform": "",
      "link": ""
    }
  ],
  "skills": [
    {
      "id": 0,
      "name": "",
      "color": ""
    }
  ]
}
```
