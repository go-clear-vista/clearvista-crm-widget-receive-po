# Receive PO Widget

A Zoho CRM embedded widget for managing customer purchase orders and progressing quote stages.

## Overview

This widget allows sales representatives to:
- Enter customer PO numbers on quote records
- Update order priority
- Progress quote stages based on validation status

## Features

- **PO Entry**: Capture customer purchase order numbers
- **Order Priority Selection**: Update order priority from a dropdown
- **Stage Management**: Automatically progress quotes through stages (Draft → Sent → Quote Ready → Closed Won/On Hold)
- **Validation Display**: Show quote stage and validity date with color-coded status
- **Confirmation Modal**: Request confirmation when moving quotes from Draft/Sent stages

## Quote Stage Workflow

The widget handles the following stage transitions:

1. **Draft / Sent**: Shows confirmation modal allowing progression to "On Hold" or "Closed Won"
2. **On Hold**: Direct progression to "Closed Won"
3. **Quote Ready**: Checks validity date
   - If valid: Moves to "Closed Won"
   - If expired: Moves to "On Hold"
4. **Other Stages**: Maintains current stage

## Backend Function

This widget calls the `stage_update` Deluge function to perform the following:
- Update the `Customer_PO_No` field
- Update the `Order_Priority` field
- Update the `Quote_Stage` field

## Installation

1. Upload this widget to your Zoho CRM instance
2. Configure the "Receive PO" custom button on the Quotes module to use this widget
3. Ensure the `stage_update` function is available in your CRM

## Updates

### v2.0 (2026-09-04)
- Migrated widget hosting from Zoho to Git-based repository
- Updated Quote_Stage reference from "Committed" to "Quote Ready"
- Maintained all existing functionality

## Technical Details

- **Language**: HTML5 + JavaScript
- **CRM SDK**: Zoho Embedded SDK v1.5
- **Dependencies**: jQuery 3.6.0

## File Structure

```
app/
└── index.html      # Main widget HTML/CSS/JS
```

---

**Last Updated**: 2026-09-04  
**Hosted By**: Claude Code