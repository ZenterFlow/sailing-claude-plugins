# Global Skills for Sailing Claude Plugins

This directory contains global skills that apply across all plugins in the sailing curriculum marketplace.

## Skills Included

### 1. plugin-formatter
**Description**: Formats plugin folders and files according to Claude Code plugin marketplace guidelines

**Purpose**: Automatically validate and fix plugin structure, naming conventions, metadata files, and documentation to ensure compliance with Claude Code specifications.

**Key Features**:
- Validates plugin.json, marketplace.json, and manifest.json against schemas
- Converts directory and file names to lowercase-with-hyphens
- Auto-fixes string-to-object conversions (author, owner fields)
- Regenerates README.md skill lists
- Creates missing template files
- Validates frontmatter in skill.md files

**Activation**:
- "format this plugin"
- "fix plugin structure"
- "validate plugin format"
- "check plugin compliance"

**Files**:
- `skill.md` - Main skill documentation
- `rules.md` - Detailed formatting rules
- `templates/` - File templates for plugins, skills, READMEs
- `schemas/` - JSON schemas for validation

## Usage

These global skills are available across the entire repository and can be invoked from any plugin directory.

## Version
v1.0.0 (2025-11-01)
