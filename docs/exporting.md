# Exporting Data

Export your search results to CSV or PDF for reporting, analysis, or record-keeping.

## Export Formats

Advanced Search & Bulk Actions supports two export formats:

![Export Options](../images/07-export-options.png)

### CSV (Comma-Separated Values)
- ✅ **Unlimited records**
- ✅ Opens in Excel, Google Sheets, Numbers
- ✅ Best for data analysis
- ✅ Includes all columns
- ✅ Easy to manipulate and filter

### PDF (Portable Document Format)
- ⚠️ **Maximum 100 records** (freemium limitation)
- ✅ Professional appearance
- ✅ Good for reports and presentations
- ✅ Print-ready format
- ✅ Cannot be edited (maintains integrity)

## How to Export

### Step 1: Perform a Search

First, find the data you want to export:

1. Select entity type (Tickets, Organizations, or Users)
2. Enter search query or build filters
3. Click Search
4. Review results to confirm they're what you want

### Step 2: Select Export Format

1. **Click the "Download" button** (top right)
2. **Choose format**:
   - **Export to CSV** - For unlimited records
   - **Export to PDF** - For up to 100 records

### Step 3: Download File

1. Your browser downloads the file automatically
2. File name format: `tickets_export_2026-02-15.csv` or `tickets_export_2026-02-15.pdf`
3. Open the file in your preferred application

## What Gets Exported

### Tickets Export Includes:
- Ticket ID
- Subject
- Status
- Priority
- Requester
- Assignee
- Created date
- Updated date
- Tags
- All visible columns

### Organizations Export Includes:
- Organization ID
- Name
- Tags
- Created date
- Updated date
- Custom fields

### Users Export Includes:
- User ID
- Name
- Email
- Role
- Organization
- Created date
- Updated date
- Tags

## Export Use Cases

### For Reporting

**Monthly ticket summary:**
1. Search: `created>2026-02-01 created<2026-03-01`
2. Export to CSV
3. Open in Excel
4. Create pivot tables and charts

**Agent performance:**
1. Search: `assignee:john.doe@company.com status:solved`
2. Export to CSV
3. Analyze resolution times
4. Generate performance report

### For Analysis

**Trend analysis:**
1. Search: `created>2026-01-01`
2. Export to CSV
3. Import into analytics tool
4. Identify patterns and trends

**Customer segmentation:**
1. Search organizations by tags
2. Export to CSV
3. Analyze customer characteristics
4. Build customer profiles

### For Record-Keeping

**Audit trail:**
1. Search: `updated>2026-02-01`
2. Export to PDF
3. Save for compliance records
4. Archive monthly exports

**Backup important searches:**
1. Run critical saved searches
2. Export to CSV
3. Store backups of key data
4. Maintain historical records

### For Presentations

**Executive summary:**
1. Search: `priority:urgent status:open`
2. Export to PDF (under 100 records)
3. Include in presentation deck
4. Share with leadership

## Working with CSV Exports

### Opening CSV Files

**Microsoft Excel:**
1. Double-click the CSV file
2. Or: File → Open → Select CSV
3. Data appears in spreadsheet

**Google Sheets:**
1. Go to sheets.google.com
2. File → Import → Upload
3. Select the CSV file
4. Choose import settings

**Apple Numbers:**
1. Drag CSV into Numbers
2. Or: File → Open → Select CSV

### Analyzing CSV Data

**Sort and filter:**
- Use Excel/Sheets filtering
- Sort by any column
- Apply conditional formatting

**Create pivot tables:**
- Summarize ticket counts
- Group by assignee, status, priority
- Calculate averages and totals

**Make charts:**
- Visualize trends over time
- Compare agent workloads
- Show ticket distribution

**Example Excel formulas:**
```
// Count open tickets
=COUNTIF(D:D,"Open")

// Average resolution time
=AVERAGE(E:E)

// Tickets per agent
=COUNTIF(F:F,"agent@company.com")
```

## Working with PDF Exports

### PDF Features

- **Formatted table** - Clean, professional appearance
- **Headers and footers** - Include export date and metadata
- **Page numbers** - Easy navigation for multi-page exports
- **Read-only** - Cannot be edited (ensures integrity)

### Best Uses for PDF

1. **Printing** - Hard copy reports
2. **Email attachments** - Share with stakeholders
3. **Archiving** - Long-term storage
4. **Presentations** - Include in slide decks

### PDF Limitations

⚠️ **100 record maximum**

If your search has more than 100 results:
- Only the first 100 are exported to PDF
- Use CSV instead for full dataset
- Or refine your search to under 100 records

## Export Limitations

### Freemium Restrictions

| Feature | Free | Premium |
|---------|------|---------|
| CSV Export | ✅ Unlimited | ✅ Unlimited |
| PDF Export | ⚠️ Max 100 records | ✅ Unlimited |
| Export Frequency | ✅ Unlimited | ✅ Unlimited |
| File Size | ✅ No limit | ✅ No limit |

### Technical Limits

- **Browser memory** - Very large exports (10,000+ records) may be slow
- **Zendesk API** - Limited to 1000 records per request (app handles pagination)
- **File size** - CSV files can get large with many custom fields

## Best Practices

### 1. Refine Before Exporting

Don't export everything:
- Use filters to get only what you need
- Remove unnecessary columns
- Limit date ranges appropriately

### 2. Name Files Descriptively

When saving exports:
- Include date: `tickets_2026-02-15.csv`
- Include purpose: `escalated_tickets_report.csv`
- Include range: `jan_2026_solved_tickets.csv`

### 3. Regular Exports for Backup

Create a routine:
- Export critical searches weekly
- Archive monthly snapshots
- Store in organized folders

### 4. Use CSV for Large Datasets

If exporting 100+ records:
- Always choose CSV over PDF
- CSV handles large volumes better
- Easier to work with in analysis tools

### 5. Verify Export Completeness

After exporting:
- Check row count matches search results
- Verify all columns are present
- Spot-check data accuracy

## Troubleshooting

### Export Not Downloading

**Possible causes:**
- Browser blocking downloads
- Pop-up blocker enabled
- Browser permissions issue

**Solutions:**
1. Check browser's download settings
2. Disable pop-up blocker for Zendesk
3. Try a different browser
4. Check browser console for errors

### CSV Opens with Garbled Text

**Cause:** Encoding or delimiter issue

**Solutions:**
1. Open Excel
2. Use "Data → From Text/CSV"
3. Select UTF-8 encoding
4. Choose comma as delimiter

### PDF Shows "Max 100 Records" Error

**Cause:** Your search returned more than 100 results

**Solutions:**
- Use CSV instead (no limit)
- Refine search to under 100 records
- Upgrade to premium for unlimited PDF exports

### Export File is Empty

**Possible causes:**
- No search results
- No records selected
- Browser extension conflict

**Solutions:**
1. Verify search returns results
2. Try exporting again
3. Disable browser extensions
4. Try different browser

### Large Export Takes Long Time

**This is normal for:**
- Thousands of records
- Many custom fields
- Slow internet connection

**Tips:**
- Be patient; let it complete
- Don't close browser during export
- Try during off-peak hours

## Security & Privacy

### Data Handling

- ✅ Exports processed in your browser
- ✅ No data sent to external servers
- ✅ Files saved to your local computer only
- ✅ You control where files are stored

### Sensitive Data

If exporting contains sensitive information:
- Store exports securely
- Use encrypted storage
- Follow your organization's data policies
- Delete exports when no longer needed

### Compliance

For regulated industries:
- Ensure exports comply with data retention policies
- Maintain audit trails of exports
- Secure exported files appropriately
- Follow GDPR, HIPAA, or other requirements

## Next Steps

- [FAQ →](./faq.md) - Common questions and answers
- [Saved Searches →](./saved-searches.md) - Save searches for regular exports
- [Searching →](./searching.md) - Refine searches before exporting

---

[← Back to Home](../README.md) | [Saved Searches →](./saved-searches.md)
