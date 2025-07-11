# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Community-Coin is a monetary policy research project proposing wealth-backed local currency systems as an alternative to debt-based fiat money. The project enables communities to create currency units by attesting asset ownership while retaining full use of those assets, eliminating interest payments.

## Repository Architecture

### Primary Documentation System
This is an **Org-mode documentation project** with dual document streams:

- **`Community-Coin.org`** - Comprehensive 630+ line business plan with technical details, financial projections, and Altman Z-Score analysis
- **`README.org`** - Executive summary and project overview for general audiences

### Multi-Format Output Pipeline
The project uses **Emacs Org-mode export** to generate professional outputs:

```
Source (.org) → LaTeX (.tex) → PDF + Text outputs
```

**Generated files** (excluded from git):
- `.pdf` files - Professional presentation versions
- `.tex` files - LaTeX intermediate compilation  
- `.txt` files - Plain text accessibility versions
- `.aux`, `.toc` - LaTeX build artifacts

### Government Communications
`communications/` contains chronological Alberta Government proposals:
- `Proposal - Alberta Buck - 20240603.pdf` - Initial submission
- `Proposal - Alberta Buck - 20241017 - Deck.pdf` - Presentation deck
- `Proposal - Alberta Buck - 20241104 - Reply AR 58480.pdf` - Response to feedback
- `Proposal - Alberta Buck - 20250405.pdf` - Latest comprehensive proposal

## Common Development Commands

### Document Generation
No traditional build system exists. Document processing uses Emacs Org-mode:

1. **Edit source**: Modify `.org` files with Org-mode syntax
2. **Export to LaTeX**: `C-c C-e l l` in Emacs
3. **Export to PDF**: `C-c C-e l p` in Emacs  
4. **Export to text**: `C-c C-e t t` in Emacs

### LaTeX Processing
If working outside Emacs, use LaTeX directly:
```bash
pdflatex Community-Coin.tex
pdflatex README.tex
```

### File Management
Key files to edit:
- `Community-Coin.org` - Main technical document
- `README.org` - Project summary and navigation
- `communications/` - Government correspondence (PDF only)

## Technical Implementation Context

### Three-Phase Development Strategy
1. **Phase 1**: Cryptocurrency payment rails (Bitcoin Lightning, Ethereum L2)
2. **Phase 2**: Centralized wealth attestation with trusted community authorities
3. **Phase 3**: Full decentralization via Holochain technology

### Core Innovation
**Interest-free wealth monetization**: Users attest asset ownership to create currency units while retaining full asset use, eliminating traditional borrowing costs.

### Financial Modeling
Uses Altman Z-Score analysis to demonstrate business health improvements vs. debt financing, projecting up to 2 full S&P credit rating improvements.

## Working with This Repository

### Key Relationships
- **README.org** serves as entry point with links to all documentation
- **Community-Coin.org** contains comprehensive technical analysis
- Generated files provide distribution formats but should not be edited directly
- Government communications demonstrate real-world application and feedback

### Documentation Standards
- Professional academic formatting with LaTeX export settings
- Comprehensive footnoting and cross-referencing
- Mathematical notation for financial analysis
- Chronological organization of government engagement

When making changes, always edit the `.org` source files and regenerate outputs through the Org-mode export process.