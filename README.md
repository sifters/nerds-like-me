cd /tmp && rm -rf nerds-like-me && git clone https://github.com/shertokj/nerds-like-me.git && cd nerds-like-me && gh repo view shertokj/nerds-like-me > /dev/null && cat > README.md << 'EOF'
# Nerds Like Me 🦞

AI meetup community in Chicago. Building, sharing, and learning about AI agents, skills, and automation together.

## Hackathon Resources

- **[Slide Deck](https://shertokj.github.io/nerds-like-me/hackathon/deck/)** — Pop-up Agent Skill Hackathon presentation
- **[Participant Guide](https://github.com/shertokj/nerds-like-me/blob/main/hackathon/participant-guide.md)** — Building your first AI skill, reference guide

## Contributing

1. Fork this repo
2. Add your skill to `hackathon/skills/` (or open a PR with a new folder)
3. Submit a pull request

Questions? Find us at a [Nerds Like Me](https://www.meetup.com/nerds-like-me/) meetup.
EOF
git add README.md && git commit -m "Add README with GitHub Pages links" && git push origin main
