# Francisco's resume source data

## Status

- **Stage:** production ready
- **Audited:** 2026-08-23

This project is the single source of truth for Francisco's resume data, including profile, work experience, projects, certifications, education, achievements, languages, and skills. This data is consumed by Francisco's web portfolio and CV generator.

## Data structure

The data lives in `index.json` with the following structure:

```JSON
{
  "profile": {
    "firstName": "",
    "lastName": "",
    "fullName": "",
    "headline": "",
    "email": "",
    "phone": "",
    "location": "",
    "website": "",
    "profilePhoto": ""
  },
  "summary": {
    "short": "",
    "long": ""
  },
  "workExperience": [
    {
      "position": "",
      "company": "",
      "employmentType": "",
      "startDate": "YYYY-MM",
      "endDate": "YYYY-MM or null",
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
      "date": "YYYY-MM-DD",
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
      "description": [],
      "date": "",
      "link": "",
      "image": ""
    }
  ],
  "languages": [
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
      "category": ""
    }
  ]
}
```

## Field notes

- **`summary`**: `short` is a 1-2 line version for cards and ATS headers; `long` is the full CV summary.
- **`workExperience[].startDate` / `endDate`**: ISO `YYYY-MM` strings for sorting and duration computation. `endDate: null` means the role is current. `duration` is the human-readable display string.
- **`workExperience[].employmentType`**: one of `Full-time`, `Contract`, or `Freelance`.
- **`workExperience[].skills` / `projects[].skills`**: arrays of skill ids referencing entries in the top-level `skills` array.
- **`projects[].date`**: ISO `YYYY-MM-DD` string.
- **`projects[].video`**: YouTube video id.
- **`skills[].category`**: one of `languages`, `frontend`, `backend`, `dataAndAI`, `devopsAndCloud`, `databases`, or `other`. Grouped skill lists (e.g. for a CV's technical skills section) are derived by filtering on this field.
