# Bulk Actions

Update multiple tickets, organizations, or users at once with bulk actions.

## What are Bulk Actions?

Bulk actions allow you to modify multiple records simultaneously, saving time when you need to apply the same change to many items.

![Bulk Changes](../images/05-bulk-changes.png)

## How to Use Bulk Actions

### Step 1: Perform a Search

First, find the records you want to update:

1. Select your entity type (Tickets, Organizations, or Users)
2. Enter a search query or build filters
3. Click Search

### Step 2: Select Records

Choose which records to update:

- **Select individual records** - Click checkboxes next to specific items
- **Select all visible** - Click the checkbox in the table header
- **Selection count** - The number of selected items appears in the status bar

![Selected Records](../images/02-search-results.png)

### Step 3: Open Bulk Changes

1. Click the **"Bulk Changes"** button (appears when records are selected)
2. The Bulk Changes dialog opens

### Step 4: Choose Fields to Update

1. **Select a field** from the first dropdown (e.g., Priority, Status, Assignee)
2. **Select a value** from the second dropdown
3. **Add more changes** by clicking "+ Add change"
4. **Remove changes** by clicking the ✕ button

### Step 5: Review and Apply

1. **Review the warning** - "This will update X tickets. This action cannot be undone."
2. **Click "Apply Changes"** to confirm
3. **Wait for completion** - Changes are applied in the background
4. **Verify results** - Check that updates were successful

## Supported Fields

### For Tickets

You can bulk update:
- **Priority** - Low, Normal, High, Urgent
- **Status** - New, Open, Pending, On-Hold, Solved, Closed
- **Type** - Question, Incident, Problem, Task
- **Assignee** - Assign to any agent
- **Group** - Assign to any group
- **Tags** - Add or remove tags

### For Organizations

You can bulk update:
- **Tags** - Add or remove tags
- **Custom fields** - Update organization custom fields

### For Users

You can bulk update:
- **Tags** - Add or remove tags
- **Organization** - Move users to different organization
- **Custom fields** - Update user custom fields

## Bulk Action Examples

### Example 1: Escalate Priority

**Scenario:** You found 15 tickets that need urgent attention.

**Steps:**
1. Search and select the 15 tickets
2. Click "Bulk Changes"
3. Field: Priority → Value: Urgent
4. Click "Apply Changes"

**Result:** All 15 tickets now have Urgent priority.

### Example 2: Reassign Tickets

**Scenario:** An agent is going on vacation; reassign their open tickets.

**Steps:**
1. Search: `assignee:john.doe@company.com status:open`
2. Select all results
3. Click "Bulk Changes"
4. Field: Assignee → Value: jane.smith@company.com
5. Click "Apply Changes"

**Result:** All open tickets reassigned to Jane.

### Example 3: Add Tags

**Scenario:** Mark all mobile app-related tickets with a tag.

**Steps:**
1. Search: `mobile app`
2. Select relevant tickets
3. Click "Bulk Changes"
4. Field: Tags → Value: mobile-app (add tag)
5. Click "Apply Changes"

**Result:** All selected tickets tagged with "mobile-app".

### Example 4: Close Old Pending Tickets

**Scenario:** Close all pending tickets older than 30 days.

**Steps:**
1. Search: `status:pending updated<2026-01-15`
2. Select all results
3. Click "Bulk Changes"
4. Field: Status → Value: Closed
5. Click "Apply Changes"

**Result:** Old pending tickets are now closed.

## Multiple Changes at Once

You can apply multiple field changes in a single bulk action:

**Example:** Escalate AND reassign tickets
1. Select tickets
2. Click "Bulk Changes"
3. Change 1: Priority → Urgent
4. Click "+ Add change"
5. Change 2: Assignee → escalation.team@company.com
6. Click "Apply Changes"

**Result:** Tickets get new priority AND new assignee in one operation.

## Limitations & Warnings

### ⚠️ Cannot Be Undone
Bulk changes are permanent and cannot be reversed. Always double-check:
- Number of selected records
- Fields and values you're changing
- Impact of the changes

### ⚠️ Selection Limits
- Maximum 100 records per bulk action (UI limitation)
- For larger operations, perform multiple bulk actions

### ⚠️ Permissions Required
You must have permission to update the fields you're changing:
- Admins can update all fields
- Agents may have restrictions
- End-users cannot perform bulk actions

### ⚠️ Validation Rules
Bulk changes must follow Zendesk's validation rules:
- Required fields must be set
- Field values must be valid
- Custom field formats must match

## Best Practices

### 1. Test with Small Batches
When performing bulk actions for the first time:
- Start with 5-10 records
- Verify the changes work as expected
- Then scale up to larger batches

### 2. Use Precise Searches
Make sure your search results include ONLY the records you want to change:
- Review results before selecting
- Use filters to be specific
- Exclude records that don't need changes

### 3. Document Your Changes
For audit purposes:
- Note what changes you made
- Record when you made them
- Keep track of which tickets were affected

### 4. Communicate Changes
If bulk changes affect other team members:
- Notify the team before making changes
- Explain why changes were made
- Let people know which tickets were affected

### 5. Schedule During Low Traffic
For large bulk operations:
- Perform during off-peak hours
- Avoid impacting customer experience
- Consider Zendesk API rate limits

## Troubleshooting

### "Cannot Apply Changes" Error

**Possible causes:**
- No records selected
- Missing required fields
- Invalid field values
- Insufficient permissions

**Solutions:**
- Verify records are selected (checkboxes checked)
- Ensure all required fields have values
- Check that field values are valid for your Zendesk instance
- Contact admin if permission issues

### Some Records Not Updated

**Possible causes:**
- Zendesk validation rules blocked some updates
- Permission restrictions on specific records
- Custom field dependencies not met

**Solutions:**
- Review Zendesk logs for errors
- Check individual record restrictions
- Verify custom field configurations

### Bulk Action Takes Long Time

**This is normal for:**
- Large numbers of records (50+)
- Complex field updates
- Zendesk API rate limiting

**Tips:**
- Be patient; let the operation complete
- Don't close the app during processing
- For very large operations (100+), split into smaller batches

## Next Steps

- [Saved Searches →](./saved-searches.md) - Save searches for repeated bulk actions
- [Exporting Data →](./exporting.md) - Export records before bulk changes
- [FAQ →](./faq.md) - Common questions

---

[← Back to Home](../README.md) | [Searching →](./searching.md)
