# Deployment Notes

## What You Need Access To

To update `https://makecu.dev/`, you need one of these:

- Access to the existing Vercel project or Vercel team that currently owns `makecu.dev`.
- Access to the domain registrar or DNS provider for `makecu.dev`, so you can point the domain to a new Vercel project.
- Access to the previous GitHub repository if the existing Vercel project still deploys from it.

If you do not get any of those, you can still deploy for free to a generated Vercel URL such as `makecu-2026.vercel.app`, then swap to `makecu.dev` later.

## Free Deployment Path

1. Create or choose a GitHub repo you control.
2. Push this folder to GitHub.
3. In Vercel, choose **Add New Project** and import the repo.
4. If the repo root contains this folder, set the Vercel **Root Directory** to `mlh-hackathon-boilerplate`.
5. Keep the project as framework preset **Other**.
6. The included `vercel.json` sets:
   - Install command: `bundle install --path vendor/bundle`
   - Build command: `bundle exec jekyll build`
   - Output directory: `_site`
7. Deploy.

Vercel's Hobby plan is free for personal and small-scale projects, but Vercel's docs say it is restricted to non-commercial, personal use. If Columbia Robotics wants shared team access or official organization ownership, check whether the club should use a Vercel team or another free host such as GitHub Pages.

## Connecting `makecu.dev`

After the new deployment works:

1. In Vercel, open the project settings and add `makecu.dev` under Domains.
2. Vercel will show the required DNS records.
3. Whoever controls DNS for `makecu.dev` must add those records.
4. Wait for DNS and SSL to propagate.

If Vercel says the domain is already assigned to another project, ask the previous MakeCU organizers for access to that project/team or ask the domain owner to remove/reassign it.

## MLH Website Checklist

The MLH guide recommends these main website sections, which this page includes:

- Landing page with name, date, location, and registration placeholder
- About section
- Sponsors section
- FAQ
- Footer links and contact details

Before publishing widely, replace placeholders for:

- MyMLH registration or your official registration form
- Mentor, judge, volunteer, and sponsorship forms
- Confirmed sponsor logos and links
- Venue address, room map, and accessibility details
- Hardware inventory and safety/training requirements
- Schedule, tracks, prizes, judges, and mentors
- Official email, Discord, and social links
- Any Columbia University event policy links

References:

- MLH main website guide: https://guide.mlh.io/general-information/hackathon-website/main-website
- Vercel build settings: https://vercel.com/docs/builds/configure-a-build
- Vercel Hobby plan: https://vercel.com/docs/plans/hobby
- Vercel domains overview: https://vercel.com/docs/domains
