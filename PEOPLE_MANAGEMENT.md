# People Management Guide

This guide explains how to manage people in the lab website, including status changes when someone becomes alumni.

## People Data Structure

Each person in `_data/people.yml` has the following fields:

```yaml
- name: "Person Name"
  picture: "/images/people/person.jpg"
  home_url: "https://person-website.com"
  description: "Brief description of the person"
  rank: "faculty|phd|ms|ug|alumni"  # Current status
  current_position: "Current job title and company"  # For alumni
  links:
    - type: "scholar|github|twitter|home"
      url: "link_url"
```

## Status Management

### When Someone Becomes Alumni

1. **Update their rank**: Change `rank` from `phd/ms/ug` to `alumni`
2. **Add current_position**: Include their new job title and company
3. **Update description**: Change from present tense to past tense
4. **Keep them in projects**: They remain listed in project pages automatically

### Example Status Change

**Before (Active Student):**
```yaml
- name: "Jane Doe"
  description: "Jane is a PhD student working on robot learning."
  rank: "phd"
  current_position: "PhD Student, USC"
```

**After (Alumni):**
```yaml
- name: "Jane Doe"
  description: "Jane was a PhD student working on robot learning."
  rank: "alumni"
  current_position: "Research Scientist, Google DeepMind"
```

## Automatic Updates

- **Project Pages**: When you update someone's status in `people.yml`, all project pages automatically show their new status and current position
- **People Page**: The main people page will categorize them correctly based on their rank
- **Project Cards**: Thumbnails in project cards will show their updated information

## Adding New People

1. Add their entry to `_data/people.yml`
2. Add their photo to `/images/people/`
3. Include them in relevant projects by adding their name to the `people:` list in project files

## Project Integration

Projects automatically pull people information from `_data/people.yml`. To add someone to a project:

1. Add their name to the `people:` list in the project's front matter
2. Ensure their name exactly matches the `name` field in `people.yml`

The project page will automatically display:
- Their photo
- Current status (rank)
- Description
- Current position (if alumni)
- Social links

## Publication Integration

Projects automatically show related publications from `_data/publications.yml`. To link a publication to a project:

1. Add a `projects:` field to the publication in `_data/publications.yml`
2. List the project IDs (filename without .md extension) that the publication relates to

Example:
```yaml
- title: 'Your Publication Title'
  authors: 'Author Names'
  venue: 'Conference Name'
  projects:
    - example_project
    - human_robot_interaction
  links:
    - type: pdf
      url: /pdfs/publications/paper.pdf
```

The project page will automatically display:
- Publication title and authors
- Venue information
- Publication image (if available)
- All links (PDF, arXiv, code, etc.)
- Organized by year
