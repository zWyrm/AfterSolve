# AfterSolve

**AfterSolve** is a one-stop platform used by 200+ active competitive programmers to upsolve problems from contests they actually participated in, through a minimalistic, responsive interface.

The app fetches real-time data from the Codeforces API and presents it intuitively, making it easier to explore contests and problems without navigating the Codeforces website directly.

---

## Table of Contents

- [Introduction](#introduction)
- [Tech Stack](#tech-stack)
- [API Documentation](#api-documentation)
- [Getting Started](#getting-started)
- [Contact Us](#contact-us)

---

## Introduction

A problemset platform designed for competitive programmers to **upsolve problems from past contests** they have actually participated in.
---

## Tech Stack

### Frontend

- **React.js** (with React DOM)
- **React Select**, **React Multi Select Component** (for dropdowns and multi-selects)
- **React Loader Spinner**, **React Spinners** (for loading indicators)
- `@fontsource/raleway` (custom font)
- **Axios** (HTTP client for API requests)

### Backend

- **Node.js**
- **Express.js** (web framework)
- **Axios** (for server-side API requests)
- **CORS** (Cross-Origin Resource Sharing)
- **dotenv** (environment variable management)

### API

- **Codeforces API** (for contest and problem data)

---

## API Documentation

The backend exposes endpoints to retrieve Codeforces data and user analytics.

### User Analytics Endpoint

**`GET /api/user/:handle/unsolved`**  
Returns a list of **unsolved problems** for a specific Codeforces user, filtered to include only contests the user participated in.

#### Response Example

```json
{
  "unsolved": [
    {
      "contestId": 1234,
      "contestName": "Codeforces Round #123",
      "index": "A",
      "name": "Example Problem",
      "rating": 800,
      "tags": ["math", "implementation"],
      "time": 1714556400000,
      "status": "Unattempted"
    }
  ]
}
```

### Error Responses

| Status Code | Description                      |
|-------------|----------------------------------|
| 429         | Rate limit exceeded. Try again.  |
| 503         | Codeforces API unavailable       |
| Other       | Returns a descriptive error      |

> **Note:** Backend enforces **strict CORS**. Requests are only allowed from the origin specified in the `REACT_APP_FRONT_URL` in your `.env` file.

---

## Getting Started

Navigate to [aftersolve.online](https://aftersolve.online), enter your Codeforces username, and start upsolving!

---

## Contact Us

For questions or feedback:

### Dinesh Panda  
- [LinkedIn/pandadinesh](https://www.linkedin.com/in/pandadinesh)  
- [pandaaa.dinesh3684@gmail.com](mailto:pandaaa.dinesh3684@gmail.com)
- [Discord](https://discord.com/users/1017847117991137340) 
- [GitHub](https://github.com/zwyrm)

### Prajesh Biswas 
- [LinkedIn/biswasprajesh](https://www.linkedin.com/in/biswasprajesh)
- [prajeshbiswas2005@gmail.com](mailto:prajeshbiswas2005@gmail.com)
- [Discord](https://discord.com/users/1222183347565105234)
- [GitHub](https://github.com/JeshByte)
