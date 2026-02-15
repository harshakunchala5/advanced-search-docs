# Saved Searches

Save your frequently used searches for quick access anytime.

## What are Saved Searches?

Saved searches allow you to store search queries and filters that you use regularly, eliminating the need to recreate them each time.

![Saved Searches](../images/06-saved-searches.png)

## How to Save a Search

### Method 1: Save Current Search

1. **Build your search**:
   - Enter search query or add filters
   - Click Search to verify results
   
2. **Click "Save" button**:
   - Located in the top action bar
   - Enter a memorable name for your search
   - Click "Save"

3. **Confirmation**:
   - Your search is now saved
   - It appears in the Saved Searches menu

### Method 2: Save from Results

After getting search results you want to save:

1. Click the **"Save"** button
2. Enter a name like "Urgent Open Tickets" or "My Pending Work"
3. Click "Save"

## Accessing Saved Searches

To use a saved search:

1. **Click "Saved Searches" button** (top left)
2. **View your saved searches list**
3. **Click on a search name** to load it
4. **Results appear automatically**

Each saved search shows:
- **Search name** - The name you gave it
- **Entity type** - tickets • organizations • users
- **Filter count** - Number of filters (e.g., "1 filter")
- **Date saved** - When you created it

## Managing Saved Searches

### Editing a Saved Search

1. Click "Saved Searches"
2. Find the search you want to modify
3. Click the **pencil (edit) icon**
4. Make your changes
5. Click "Save"

### Deleting a Saved Search

1. Click "Saved Searches"
2. Find the search you want to remove
3. Click the **trash (delete) icon**
4. Confirm deletion

⚠️ **Note:** Deleted searches cannot be recovered.

### Renaming a Saved Search

1. Click "Saved Searches"
2. Click the edit icon for the search
3. Change the name
4. Click "Save"

## Saved Search Examples

Here are some useful searches to save:

### For Support Agents

**"My Open Tickets"**
- Query: `assignee:me status:open status:pending`
- Use: Start of day dashboard

**"Escalated Items"**
- Query: `priority:urgent status:open`
- Use: Focus on critical issues

**"Awaiting My Response"**
- Query: `assignee:me status:pending`
- Use: Tickets needing attention

**"Recently Assigned to Me"**
- Filters: Assignee → is → me, Created → is after → (yesterday)
- Use: New work queue

### For Team Leads

**"Team's Open Work"**
- Query: `group:support-team status:open`
- Use: Team workload monitoring

**"Unassigned Tickets"**
- Filters: Assignee → is empty, Status → is → New
- Use: Ticket distribution

**"High Priority This Week"**
- Filters: Priority → is → High, Created → is after → (this week)
- Use: Weekly prioritization

### For Quality Assurance

**"Recently Solved"**
- Query: `status:solved updated>2026-02-10`
- Use: QA review queue

**"Tickets to Audit"**
- Query: `tags:needs-review status:solved`
- Use: Quality checks

**"Customer Feedback"**
- Filters: Type → is → Question, Tags → contains → feedback
- Use: Product insights

### For Billing/Finance

**"Billing Inquiries"**
- Query: `tags:billing status:open`
- Use: Payment-related tickets

**"Refund Requests"**
- Query: `subject:*refund* status:open status:pending`
- Use: Refund processing

## Storage & Limits

### Where Searches are Saved
Saved searches are stored:
- **Locally in your browser** (using localStorage)
- **Per user** - Your searches are private to you
- **Per browser** - Searches on Chrome won't appear in Firefox

### Limits
- **Maximum saved searches**: 50 per user
- **Name length**: Up to 100 characters
- **Storage**: Uses browser localStorage (typically 5-10MB available)

### Clearing Saved Searches
Saved searches are deleted if:
- You manually delete them
- You clear browser data/cache
- You use browser's "Clear Site Data" option

💡 **Tip:** Export your saved searches configuration before clearing browser data.

## Sharing Saved Searches

Currently, saved searches **cannot be shared** between users. Each user manages their own searches.

**Workaround for teams:**
1. Document useful searches in a team wiki
2. Share search queries via Slack/email
3. Team members can manually save the same searches

**Example documentation:**
```
Team Search: Escalated Issues
Query: priority:urgent status:open group:support
Purpose: Daily stand-up review
```

## Best Practices

### 1. Use Descriptive Names
Good names:
- ✅ "My Open High Priority Tickets"
- ✅ "Billing Issues - Last 7 Days"
- ✅ "Unassigned New Tickets"

Poor names:
- ❌ "Search 1"
- ❌ "Test"
- ❌ "Stuff"

### 2. Organize by Purpose
Group your searches mentally:
- Daily workflow searches
- Reporting searches
- Special project searches
- Cleanup/maintenance searches

### 3. Review and Clean Up
Periodically:
- Delete unused searches
- Update outdated searches
- Rename unclear searches

### 4. Start Your Day with Saved Searches
Create a morning routine:
1. Load "My Open Tickets"
2. Load "New Assignments"
3. Load "Escalated Issues"
4. Plan your day accordingly

### 5. Create Searches for Reporting
Save searches for regular reports:
- "Weekly Performance" - Run every Monday
- "Month-End Review" - Run on last day of month
- "Customer Satisfaction" - Run for quarterly reviews

## Troubleshooting

### Saved Search Not Appearing

**Possible causes:**
- Different browser or device
- Browser cache cleared
- Private/incognito mode

**Solutions:**
- Use the same browser where you saved it
- Recreate the search
- Avoid clearing browser data

### Saved Search Returns Wrong Results

**Possible causes:**
- Zendesk data has changed
- Filters may be date-dependent
- Custom fields may have changed

**Solutions:**
- Edit and update the search
- Verify filter values still exist
- Re-save with corrected parameters

### Cannot Save More Searches

**Cause:** You've reached the 50 search limit

**Solution:**
- Delete unused searches
- Archive old searches (copy to document)
- Combine similar searches

## Next Steps

- [Exporting Data →](./exporting.md) - Export saved search results
- [Bulk Actions →](./bulk-actions.md) - Use saved searches with bulk updates
- [FAQ →](./faq.md) - Common questions

---

[← Back to Home](../README.md) | [Bulk Actions →](./bulk-actions.md)
