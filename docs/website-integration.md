# Website Integration

The Robotics Engineering Curriculum website should not own curriculum content.

The website is responsible for:

- Loading curriculum data.
- Validating the content shape.
- Rendering dashboard, curriculum, mission, project, portfolio, notes, and progress views.
- Tracking local learner progress.

This repository is responsible for:

- Mission content.
- Project briefs.
- Skill explanations.
- Hardware reference pages.
- Resource lists.
- Reusable writing templates.

## Integration Boundary

The website should load content through a source boundary, for example:

```ts
loadCurriculum()
```

The UI should not import Markdown files or curriculum seed data directly. It should receive a normalised curriculum object.

## Future Markdown Loader

A future loader should:

1. Read this repository from disk, Git, or an API.
2. Parse Markdown front matter.
3. Validate required fields.
4. Resolve references to projects, skills, hardware, and resources.
5. Return the website curriculum schema.

## Migration Plan

1. Keep local TypeScript seed data as a fallback.
2. Add Markdown parsing.
3. Convert one module from TypeScript to Markdown.
4. Validate parity in the website.
5. Move all curriculum content into this repository.
