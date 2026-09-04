# Changelog

All notable changes to this widget will be documented in this file.

## [2.0.0] - 2026-09-04

### Changed
- Migrated widget hosting from Zoho's internal CDN to Git-based repository
- Updated Quote_Stage reference from "Committed" to "Quote Ready" to match CRM picklist rename
- Widget now hosted at GitHub instead of Zoho's Zappsusercontent

### Technical
- Maintained backward compatibility with existing `stage_update` function
- All existing features and UI remain unchanged
- Updated documentation with new hosting information

## [1.0.0] - Original Release

### Added
- Initial Receive PO widget implementation
- Customer PO number entry field
- Order Priority dropdown selection
- Quote Stage display with color coding
- Validity date display with expiration detection
- Confirmation modal for Draft/Sent stage transitions
- Integration with Zoho CRM's embedded SDK