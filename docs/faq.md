# Frequently Asked Questions (FAQ)

Common questions and answers about Advanced Search & Bulk Actions.

## General Questions

### What is Advanced Search & Bulk Actions?

Advanced Search & Bulk Actions is a Zendesk sidebar app that enhances your ability to search, filter, and manage tickets, organizations, and users. It provides powerful search capabilities, advanced filtering, bulk update operations, saved searches, and data export functionality.

### Do I need a special Zendesk plan to use this app?

Yes, you need:
- Zendesk Support **Growth plan or higher**
- Permission to install Zendesk apps (typically admin or account owner)

### Is this app free?

The app has two tiers:
- **Free version** - All features except unlimited PDF exports
- **Premium version** - Removes the 100-record PDF export limit

### Where does the app appear in Zendesk?

The app appears in the **right sidebar** when viewing tickets. Click the Apps icon to open it.

## Installation & Setup

### How do I install the app?

1. Go to Zendesk Admin → Apps and integrations → Zendesk Marketplace
2. Search for "Advanced Search & Bulk Actions"
3. Click "Install"
4. Follow the prompts to complete installation

### Why don't I see the app in my sidebar?

**Possible reasons:**
- App not installed or not enabled
- Insufficient permissions
- Using Zendesk plan below Growth tier
- Browser extension blocking it

**Solutions:**
- Verify installation in Admin → Apps
- Check with your Zendesk admin
- Try different browser
- Disable ad blockers

### Can I use the app on mobile?

The app is **optimized for desktop browsers**. Mobile support is limited. For best experience, use:
- Desktop or laptop computer
- Modern browser (Chrome, Firefox, Safari, Edge)
- Screen width at least 1024px

## Searching

### How is this different from Zendesk's built-in search?

Advanced Search & Bulk Actions offers:
- ✅ Visual filter builder (no syntax needed)
- ✅ Bulk update operations
- ✅ CSV and PDF export
- ✅ Saved searches
- ✅ Column customization
- ✅ Search organizations and users easily

Zendesk's search:
- Global search bar
- Requires query syntax knowledge
- Limited bulk operations
- Basic export options

### Can I search across all entity types at once?

No, you must select one entity type (Tickets, Organizations, or Users) per search. This ensures relevant filters and columns are available.

### What's the maximum number of search results?

Zendesk's Search API returns up to **1,000 results** per search. If you need more:
- Add filters to narrow results
- Use date ranges to split searches
- Export in batches

### Do searches include archived tickets?

Yes, searches include all tickets including solved, closed, and archived tickets. Use status filters to narrow results.

### Can I save multiple versions of the same search?

Yes! Save as many variations as you need. For example:
- "High Priority Open" and "High Priority All Statuses"
- "My Tickets Today" and "My Tickets This Week"

## Filtering

### What fields can I filter by?

**Tickets:**
- Status, Priority, Type
- Assignee, Requester, Submitter
- Group, Organization
- Created date, Updated date, Due date
- Tags, Subject
- Custom fields

**Organizations:**
- Name, Tags
- Created date, Updated date
- Custom fields

**Users:**
- Name, Email, Role
- Organization
- Tags, Created date, Updated date
- Custom fields

### Can I use AND/OR logic in filters?

Currently:
- **Multiple filters = AND logic** (all conditions must match)
- **Multiple values in search box = OR logic** (any condition matches)

Example:
- Filters: Priority=High AND Status=Open (both must be true)
- Search: `priority:high priority:urgent` (either can be true)

### How do I search for empty fields?

Use the "is empty" operator:
1. Add filter
2. Select field (e.g., Assignee)
3. Select operator "is empty"
4. No value needed

This finds records where that field has no value.

## Bulk Actions

### Can bulk changes be undone?

**No**, bulk changes are permanent and cannot be undone. Always:
- ✅ Review selection carefully
- ✅ Test with small batch first
- ✅ Export data before bulk changes
- ✅ Double-check field values

### How many records can I update at once?

**Recommended maximum: 100 records per bulk action**

For larger operations:
- Split into multiple batches
- Perform sequentially
- Monitor for errors

### Why did some records fail to update?

Common reasons:
- **Permissions** - You lack permission to update those records
- **Validation** - Field values don't meet Zendesk's rules
- **Required fields** - Missing required field values
- **Dependencies** - Custom field dependencies not met

Check Zendesk logs for specific error messages.

### Can I bulk update custom fields?

Yes, if:
- ✅ You have permission to edit those fields
- ✅ Custom fields are supported field types
- ✅ Values are valid for the field

### Do bulk actions trigger automations?

**Yes!** Bulk updates can trigger:
- Automations
- Triggers
- Macros
- Webhooks
- Email notifications

Plan accordingly when performing bulk operations.

## Saved Searches

### Where are saved searches stored?

Saved searches are stored **locally in your browser** using localStorage. They are:
- ✅ Private to you (not shared with others)
- ✅ Per browser (Chrome searches won't appear in Firefox)
- ✅ Per device (computer searches won't appear on phone)

### Can I share saved searches with my team?

Not directly. However, you can:
1. Document the search query and filters
2. Share the documentation with team members
3. Team members manually recreate the search

Example:
```
Search name: Escalated Issues
Entity: Tickets
Filters: Priority = Urgent, Status = Open
```

### What happens if I clear my browser cache?

**Saved searches will be deleted** if you clear browser data. To prevent loss:
- ✅ Export important searches (document query/filters)
- ✅ Avoid clearing "Site Data" in browser settings
- ✅ Recreate searches after cache clear

### Can I export my saved searches?

Currently, there's no built-in export for saved searches themselves. However:
- You can export the *results* of saved searches to CSV/PDF
- Document your search configurations manually

## Exporting

### What's the difference between CSV and PDF exports?

| Feature | CSV | PDF |
|---------|-----|-----|
| Record limit | Unlimited | 100 (freemium) |
| Editable | ✅ Yes | ❌ No |
| Analysis | ✅ Excel, Sheets | ❌ View only |
| Professional | Basic | ✅ Formatted |
| File size | Larger | Smaller |

### Why is PDF limited to 100 records?

This is a **freemium limitation**. Upgrade to Premium to remove this limit.

For unlimited exports, use CSV format.

### Can I schedule automatic exports?

Not currently. You must manually:
1. Run search
2. Click Download
3. Save file

**Workaround:** Create a workflow reminder to export regularly (e.g., weekly reports).

### What format is the CSV file?

- **Encoding:** UTF-8
- **Delimiter:** Comma (,)
- **Line endings:** CRLF (Windows-compatible)
- **Quote character:** Double quotes for fields containing commas

This ensures compatibility with Excel, Google Sheets, and other tools.

### Can I export to Excel format directly?

No, but CSV files open directly in Excel:
- Double-click the CSV file
- Or: Excel → File → Open → Select CSV

CSV is universally compatible and works across all spreadsheet applications.

## Performance

### Why is my search slow?

**Common causes:**
- Very broad search (no filters)
- Searching across many thousands of records
- Complex filter combinations
- Zendesk API rate limiting
- Network latency

**Solutions:**
- Add filters to narrow results
- Use date ranges to limit scope
- Try during off-peak hours
- Check internet connection

### The app feels sluggish. How can I improve performance?

**Tips:**
1. **Close unnecessary tabs** - Free up browser memory
2. **Use fewer filters** - Simplify complex searches
3. **Limit results** - Use date ranges and status filters
4. **Refresh browser** - Clear temporary data
5. **Use modern browser** - Chrome, Firefox, Edge work best

### How many records can the app handle?

**Recommended limits:**
- **Search results:** 1,000 records (Zendesk API limit)
- **Bulk actions:** 100 records per operation
- **CSV export:** Unlimited (but very large files may be slow)
- **PDF export:** 100 records (freemium) or unlimited (premium)

## Troubleshooting

### The app won't load / shows white screen

**Try these steps:**

1. **Refresh the page** - Press F5 or Cmd+R
2. **Clear cache** - Browser Settings → Clear Cache
3. **Try incognito/private mode** - Rules out extension conflicts
4. **Different browser** - Test in Chrome, Firefox, or Edge
5. **Check console** - Look for errors in browser DevTools
6. **Contact support** - If issue persists

### I get "API Error" when searching

**Possible causes:**
- Zendesk API temporarily unavailable
- Rate limit exceeded
- Network connectivity issue
- Invalid search query

**Solutions:**
1. Wait 1-2 minutes and try again
2. Simplify your search query
3. Check Zendesk status page
4. Verify network connection

### Filters aren't working correctly

**Debugging steps:**

1. **Clear all filters** - Click "Clear" button
2. **Add filters one at a time** - Identify which filter causes issues
3. **Check field values** - Ensure values exist in Zendesk
4. **Review operators** - "is" vs "is not" vs "contains"
5. **Test with simple query** - Verify app functionality

### Results show wrong data

**Verify:**
- ✅ Correct entity type selected (Tickets vs Organizations vs Users)
- ✅ Filters applied as intended
- ✅ Using correct operator (is vs contains)
- ✅ Date ranges are valid
- ✅ Search query syntax is correct

## Data & Privacy

### Is my search data stored by the app?

**No.** The app:
- ✅ Only stores saved search *configurations* locally in your browser
- ✅ Does not store or transmit search *results*
- ✅ Does not send data to external servers
- ✅ All searches happen via Zendesk's API directly

### Are exports secure?

Yes:
- ✅ Exports generated locally in your browser
- ✅ Files saved directly to your computer
- ✅ No data sent to third parties
- ✅ You control where exports are stored

### Can other users see my saved searches?

**No.** Saved searches are:
- ✅ Stored in your browser only
- ✅ Private to you
- ✅ Not visible to admins or other users
- ✅ Not synced across devices

## Getting Help

### Where can I find more documentation?

- 📚 [Getting Started Guide](./getting-started.md)
- 🔍 [Searching & Filtering](./searching.md)
- ⚡ [Bulk Actions](./bulk-actions.md)
- 💾 [Saved Searches](./saved-searches.md)
- 📊 [Exporting Data](./exporting.md)

### How do I report a bug?

1. **Document the issue:**
   - What you were trying to do
   - What happened instead
   - Any error messages
   - Browser and version

2. **Report it:**
   - Email: support@yourcompany.com
   - GitHub Issues: [Link to your repo]
   - Include screenshots if possible

### How do I request a feature?

We'd love to hear your ideas!
- Email: feedback@yourcompany.com
- Include: What feature you want and why it would be useful

### Can I get one-on-one help?

For personalized assistance:
- **Email support:** support@yourcompany.com
- **Live chat:** Available during business hours
- **Schedule demo:** Book a session with our team

## Upgrading

### What does Premium include?

**Premium features:**
- ✅ Unlimited PDF exports (no 100-record limit)
- ✅ Priority support
- ✅ Early access to new features
- ✅ Custom export templates (coming soon)

### How do I upgrade to Premium?

Contact us:
- Email: sales@yourcompany.com
- Include your Zendesk subdomain
- We'll send pricing and activation instructions

### Is there a trial period?

Yes! Try Premium free for **14 days**:
- Full feature access
- No credit card required
- Cancel anytime

---

## Still Have Questions?

**Contact Support:**
- 📧 Email: support@yourcompany.com
- 💬 Live Chat: Available Mon-Fri 9AM-5PM EST
- 📞 Phone: +1 (555) 123-4567

[← Back to Home](../README.md)
