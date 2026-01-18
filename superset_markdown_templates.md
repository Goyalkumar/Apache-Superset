# APACHE SUPERSET MARKDOWN TEMPLATES
# Document Tagging Analytics Dashboard

===============================================================================
These are ready-to-use markdown components for your Superset dashboards.
Simply copy and paste into Markdown components in your dashboard.
===============================================================================

---

## TEMPLATE 1: MAIN DASHBOARD HEADER
---

```markdown
<div style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); 
            padding: 35px; 
            border-radius: 12px; 
            color: white; 
            margin-bottom: 25px;
            box-shadow: 0 8px 20px rgba(102, 126, 234, 0.3);">
  <div style="display: flex; justify-content: space-between; align-items: center;">
    <div>
      <h1 style="margin: 0; font-size: 32px; font-weight: 600; letter-spacing: -0.5px;">
        📊 Document Tagging Analytics
      </h1>
      <p style="margin: 8px 0 0 0; opacity: 0.95; font-size: 16px;">
        Comprehensive analysis of document relationships and tag classifications
      </p>
    </div>
    <div style="text-align: right;">
      <div style="font-size: 14px; opacity: 0.9;">Last Updated</div>
      <div style="font-size: 18px; font-weight: 600;">January 02, 2026</div>
    </div>
  </div>
</div>
```

---

## TEMPLATE 2: SECTION HEADER (Document Search)
---

```markdown
<div style="background: white; 
            padding: 25px; 
            border-radius: 10px; 
            margin-bottom: 20px;
            border-left: 5px solid #667eea;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);">
  <h2 style="margin: 0 0 10px 0; color: #667eea; font-size: 24px; font-weight: 600;">
    🔍 Document Search
  </h2>
  <p style="margin: 0; color: #6c757d; font-size: 14px;">
    Search and filter documents by name, tags, date range, and classification status. 
    Use the filters below to narrow down results.
  </p>
</div>
```

---

## TEMPLATE 3: KPI SUMMARY CARDS
---

```markdown
<div style="display: grid; 
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); 
            gap: 20px; 
            margin: 20px 0;">
  
  <!-- Card 1: Total Documents -->
  <div style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); 
              padding: 25px; 
              border-radius: 12px; 
              color: white;
              box-shadow: 0 4px 12px rgba(102, 126, 234, 0.3);
              text-align: center;">
    <div style="font-size: 14px; opacity: 0.9; text-transform: uppercase; letter-spacing: 1px; margin-bottom: 10px;">
      Total Documents
    </div>
    <div style="font-size: 42px; font-weight: 700; line-height: 1;">
      1,245
    </div>
    <div style="font-size: 13px; opacity: 0.85; margin-top: 8px;">
      ↑ 12% from last month
    </div>
  </div>
  
  <!-- Card 2: Active Tags -->
  <div style="background: linear-gradient(135deg, #4CAF50 0%, #45a049 100%); 
              padding: 25px; 
              border-radius: 12px; 
              color: white;
              box-shadow: 0 4px 12px rgba(76, 175, 80, 0.3);
              text-align: center;">
    <div style="font-size: 14px; opacity: 0.9; text-transform: uppercase; letter-spacing: 1px; margin-bottom: 10px;">
      Active Tags
    </div>
    <div style="font-size: 42px; font-weight: 700; line-height: 1;">
      342
    </div>
    <div style="font-size: 13px; opacity: 0.85; margin-top: 8px;">
      23 new this week
    </div>
  </div>
  
  <!-- Card 3: Classification Rate -->
  <div style="background: linear-gradient(135deg, #2196F3 0%, #1976D2 100%); 
              padding: 25px; 
              border-radius: 12px; 
              color: white;
              box-shadow: 0 4px 12px rgba(33, 150, 243, 0.3);
              text-align: center;">
    <div style="font-size: 14px; opacity: 0.9; text-transform: uppercase; letter-spacing: 1px; margin-bottom: 10px;">
      Classification Rate
    </div>
    <div style="font-size: 42px; font-weight: 700; line-height: 1;">
      94%
    </div>
    <div style="font-size: 13px; opacity: 0.85; margin-top: 8px;">
      1,168 classified
    </div>
  </div>
  
  <!-- Card 4: Unknown Tags -->
  <div style="background: linear-gradient(135deg, #FF9800 0%, #F57C00 100%); 
              padding: 25px; 
              border-radius: 12px; 
              color: white;
              box-shadow: 0 4px 12px rgba(255, 152, 0, 0.3);
              text-align: center;">
    <div style="font-size: 14px; opacity: 0.9; text-transform: uppercase; letter-spacing: 1px; margin-bottom: 10px;">
      Unknown Tags
    </div>
    <div style="font-size: 42px; font-weight: 700; line-height: 1;">
      45
    </div>
    <div style="font-size: 13px; opacity: 0.85; margin-top: 8px;">
      ⚠️ Needs review
    </div>
  </div>
  
</div>
```

---

## TEMPLATE 4: NAVIGATION MENU
---

```markdown
<div style="background: white; 
            padding: 20px; 
            border-radius: 10px; 
            margin-bottom: 20px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);">
  <h3 style="margin: 0 0 15px 0; color: #2c3e50; font-size: 18px; font-weight: 600;">
    📋 Quick Navigation
  </h3>
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 12px;">
    
    <a href="#document-search" style="display: block; padding: 12px 16px; background: #f8f9fa; 
       border-radius: 8px; text-decoration: none; color: #495057; font-weight: 500;
       transition: all 0.3s; border-left: 4px solid #667eea;">
      🔍 Document Search
    </a>
    
    <a href="#parent-child-tag" style="display: block; padding: 12px 16px; background: #f8f9fa; 
       border-radius: 8px; text-decoration: none; color: #495057; font-weight: 500;
       transition: all 0.3s; border-left: 4px solid #764ba2;">
      🏷️ Parent Doc - Child Tag
    </a>
    
    <a href="#parent-child-doc" style="display: block; padding: 12px 16px; background: #f8f9fa; 
       border-radius: 8px; text-decoration: none; color: #495057; font-weight: 500;
       transition: all 0.3s; border-left: 4px solid #4CAF50;">
      📁 Parent Doc - Child Doc
    </a>
    
    <a href="#unknown-tags" style="display: block; padding: 12px 16px; background: #f8f9fa; 
       border-radius: 8px; text-decoration: none; color: #495057; font-weight: 500;
       transition: all 0.3s; border-left: 4px solid #FF9800;">
      ⚠️ Unknown Tag Report
    </a>
    
    <a href="#classified-tags" style="display: block; padding: 12px 16px; background: #f8f9fa; 
       border-radius: 8px; text-decoration: none; color: #495057; font-weight: 500;
       transition: all 0.3s; border-left: 4px solid #2196F3;">
      ✅ Classified Tag Report
    </a>
    
  </div>
</div>

<style>
a:hover {
  background: #667eea !important;
  color: white !important;
  transform: translateX(5px);
}
</style>
```

---

## TEMPLATE 5: INFO BOX WITH INSTRUCTIONS
---

```markdown
<div style="background: #e7f3ff; 
            border-left: 5px solid #2196F3; 
            padding: 20px; 
            border-radius: 8px; 
            margin: 20px 0;">
  <h4 style="margin: 0 0 10px 0; color: #1976D2; font-size: 16px; font-weight: 600;">
    💡 How to Use This Dashboard
  </h4>
  <ul style="margin: 0; padding-left: 20px; color: #495057; line-height: 1.8;">
    <li>Use the <strong>filters</strong> at the top to narrow down results</li>
    <li>Click on any <strong>data point</strong> in charts to cross-filter other visualizations</li>
    <li>Hover over charts for <strong>detailed tooltips</strong></li>
    <li>Use the <strong>search box</strong> in tables to find specific documents</li>
    <li>Export data using the <strong>download button</strong> on each chart</li>
  </ul>
</div>
```

---

## TEMPLATE 6: WARNING BOX (Unknown Tags)
---

```markdown
<div style="background: #fff3e0; 
            border-left: 5px solid #FF9800; 
            padding: 20px; 
            border-radius: 8px; 
            margin: 20px 0;">
  <h4 style="margin: 0 0 10px 0; color: #F57C00; font-size: 16px; font-weight: 600;">
    ⚠️ Action Required: Unknown Tags
  </h4>
  <p style="margin: 0; color: #495057; line-height: 1.6;">
    There are currently <strong>45 documents</strong> with unknown or unclassified tags. 
    These require manual review and classification. Click the table below to see the full list 
    and take appropriate action.
  </p>
</div>
```

---

## TEMPLATE 7: SUCCESS BOX (Completion Status)
---

```markdown
<div style="background: #e8f5e9; 
            border-left: 5px solid #4CAF50; 
            padding: 20px; 
            border-radius: 8px; 
            margin: 20px 0;">
  <h4 style="margin: 0 0 10px 0; color: #388E3C; font-size: 16px; font-weight: 600;">
    ✅ Great Progress!
  </h4>
  <p style="margin: 0; color: #495057; line-height: 1.6;">
    Your team has achieved a <strong>94% classification rate</strong> this month. 
    Only 77 documents remaining to reach 100% completion. Keep up the excellent work!
  </p>
</div>
```

---

## TEMPLATE 8: STATISTICS TABLE
---

```markdown
<div style="background: white; 
            padding: 25px; 
            border-radius: 10px; 
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
            margin: 20px 0;">
  <h3 style="margin: 0 0 20px 0; color: #2c3e50; font-size: 20px; font-weight: 600; border-bottom: 2px solid #e9ecef; padding-bottom: 10px;">
    📈 Key Statistics
  </h3>
  <table style="width: 100%; border-collapse: collapse;">
    <tr style="border-bottom: 1px solid #e9ecef;">
      <td style="padding: 12px 0; color: #6c757d; font-weight: 500;">Total Documents</td>
      <td style="padding: 12px 0; text-align: right; font-weight: 600; color: #2c3e50; font-size: 18px;">1,245</td>
    </tr>
    <tr style="border-bottom: 1px solid #e9ecef;">
      <td style="padding: 12px 0; color: #6c757d; font-weight: 500;">Classified Documents</td>
      <td style="padding: 12px 0; text-align: right; font-weight: 600; color: #4CAF50; font-size: 18px;">1,168</td>
    </tr>
    <tr style="border-bottom: 1px solid #e9ecef;">
      <td style="padding: 12px 0; color: #6c757d; font-weight: 500;">Pending Classification</td>
      <td style="padding: 12px 0; text-align: right; font-weight: 600; color: #FF9800; font-size: 18px;">77</td>
    </tr>
    <tr style="border-bottom: 1px solid #e9ecef;">
      <td style="padding: 12px 0; color: #6c757d; font-weight: 500;">Total Tags Used</td>
      <td style="padding: 12px 0; text-align: right; font-weight: 600; color: #2c3e50; font-size: 18px;">342</td>
    </tr>
    <tr style="border-bottom: 1px solid #e9ecef;">
      <td style="padding: 12px 0; color: #6c757d; font-weight: 500;">Unknown Tags</td>
      <td style="padding: 12px 0; text-align: right; font-weight: 600; color: #F44336; font-size: 18px;">45</td>
    </tr>
    <tr>
      <td style="padding: 12px 0; color: #6c757d; font-weight: 500;">Average Tags per Document</td>
      <td style="padding: 12px 0; text-align: right; font-weight: 600; color: #2196F3; font-size: 18px;">3.6</td>
    </tr>
  </table>
</div>
```

---

## TEMPLATE 9: SECTION DIVIDER
---

```markdown
<div style="margin: 30px 0; text-align: center;">
  <div style="display: inline-block; padding: 0 20px; background: white; position: relative; z-index: 1;">
    <span style="color: #667eea; font-weight: 600; font-size: 14px; text-transform: uppercase; letter-spacing: 1px;">
      ⬇️ Detailed Analysis Below ⬇️
    </span>
  </div>
  <div style="height: 2px; background: linear-gradient(to right, transparent, #667eea, transparent); margin-top: -12px;"></div>
</div>
```

---

## TEMPLATE 10: FOOTER WITH TIMESTAMP
---

```markdown
<div style="background: #f8f9fa; 
            padding: 20px; 
            border-radius: 8px; 
            margin-top: 30px;
            text-align: center;
            border-top: 3px solid #667eea;">
  <p style="margin: 0; color: #6c757d; font-size: 13px;">
    Dashboard last refreshed: <strong>January 02, 2026 at 14:30 UTC</strong>
  </p>
  <p style="margin: 8px 0 0 0; color: #6c757d; font-size: 12px;">
    Data source: Production SQL Database | Contact: analytics@yourcompany.com
  </p>
</div>
```

---

## TEMPLATE 11: RELATIONSHIP DIAGRAM (Parent-Child)
---

```markdown
<div style="background: white; 
            padding: 25px; 
            border-radius: 10px; 
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
            margin: 20px 0;">
  <h3 style="margin: 0 0 20px 0; color: #2c3e50; font-size: 20px; font-weight: 600;">
    🔗 Document-Tag Relationship Structure
  </h3>
  <div style="font-family: monospace; font-size: 14px; color: #495057; line-height: 2; background: #f8f9fa; padding: 20px; border-radius: 8px;">
    <div style="color: #667eea; font-weight: 600;">📄 Parent Document</div>
    <div style="margin-left: 20px;">│</div>
    <div style="margin-left: 20px;">├─── 🏷️ Child Tag 1</div>
    <div style="margin-left: 20px;">│</div>
    <div style="margin-left: 20px;">├─── 🏷️ Child Tag 2</div>
    <div style="margin-left: 20px;">│</div>
    <div style="margin-left: 20px;">├─── 📄 Child Document 1</div>
    <div style="margin-left: 20px;">│    │</div>
    <div style="margin-left: 20px;">│    └─── 🏷️ Nested Tag</div>
    <div style="margin-left: 20px;">│</div>
    <div style="margin-left: 20px;">└─── 📄 Child Document 2</div>
  </div>
</div>
```

---

## TEMPLATE 12: DRILL-THROUGH INSTRUCTION
---

```markdown
<div style="background: linear-gradient(135deg, rgba(102, 126, 234, 0.1), rgba(118, 75, 162, 0.1)); 
            border: 2px dashed #667eea; 
            padding: 20px; 
            border-radius: 10px; 
            margin: 20px 0;
            text-align: center;">
  <h4 style="margin: 0 0 12px 0; color: #667eea; font-size: 18px; font-weight: 600;">
    🔍 Click to Drill Through
  </h4>
  <p style="margin: 0; color: #495057; font-size: 14px; line-height: 1.6;">
    Click on any data point in the charts above to filter and see detailed information below. 
    Use the tabs to switch between different relationship views.
  </p>
</div>
```

---

## TEMPLATE 13: PAGE-SPECIFIC HEADERS
---

### For "Parent Doc - Child Tag" Page:
```markdown
<div style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); 
            padding: 30px; 
            border-radius: 12px; 
            color: white; 
            margin-bottom: 20px;">
  <h1 style="margin: 0 0 8px 0; font-size: 28px; font-weight: 600;">
    🏷️ Parent Document - Child Tag Relationships
  </h1>
  <p style="margin: 0; opacity: 0.95; font-size: 15px;">
    Analyze how parent documents are connected to their child tags
  </p>
</div>
```

### For "Unknown Tag Report" Page:
```markdown
<div style="background: linear-gradient(135deg, #FF9800 0%, #F57C00 100%); 
            padding: 30px; 
            border-radius: 12px; 
            color: white; 
            margin-bottom: 20px;">
  <h1 style="margin: 0 0 8px 0; font-size: 28px; font-weight: 600;">
    ⚠️ Unknown Tag Report
  </h1>
  <p style="margin: 0; opacity: 0.95; font-size: 15px;">
    Review and classify unidentified tags in the system
  </p>
</div>
```

### For "Classified Tag Report" Page:
```markdown
<div style="background: linear-gradient(135deg, #4CAF50 0%, #45a049 100%); 
            padding: 30px; 
            border-radius: 12px; 
            color: white; 
            margin-bottom: 20px;">
  <h1 style="margin: 0 0 8px 0; font-size: 28px; font-weight: 600;">
    ✅ Classified Tag Report
  </h1>
  <p style="margin: 0; opacity: 0.95; font-size: 15px;">
    Summary of successfully classified tags and their distribution
  </p>
</div>
```

---

## TEMPLATE 14: TREND INDICATORS
---

```markdown
<div style="display: flex; gap: 15px; flex-wrap: wrap; margin: 20px 0;">
  
  <!-- Positive Trend -->
  <div style="flex: 1; min-width: 200px; background: white; padding: 18px; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.08); border-left: 4px solid #4CAF50;">
    <div style="color: #6c757d; font-size: 12px; text-transform: uppercase; margin-bottom: 8px;">Documents Classified</div>
    <div style="font-size: 28px; font-weight: 700; color: #2c3e50; margin-bottom: 5px;">1,168</div>
    <div style="color: #4CAF50; font-size: 13px; font-weight: 600;">
      ↑ 12.5% <span style="font-weight: 400; color: #6c757d;">vs last month</span>
    </div>
  </div>
  
  <!-- Negative Trend -->
  <div style="flex: 1; min-width: 200px; background: white; padding: 18px; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.08); border-left: 4px solid #F44336;">
    <div style="color: #6c757d; font-size: 12px; text-transform: uppercase; margin-bottom: 8px;">Unknown Tags</div>
    <div style="font-size: 28px; font-weight: 700; color: #2c3e50; margin-bottom: 5px;">45</div>
    <div style="color: #F44336; font-size: 13px; font-weight: 600;">
      ↓ 8.3% <span style="font-weight: 400; color: #6c757d;">vs last month</span>
    </div>
  </div>
  
  <!-- Neutral Trend -->
  <div style="flex: 1; min-width: 200px; background: white; padding: 18px; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.08); border-left: 4px solid #2196F3;">
    <div style="color: #6c757d; font-size: 12px; text-transform: uppercase; margin-bottom: 8px;">Avg Tags per Doc</div>
    <div style="font-size: 28px; font-weight: 700; color: #2c3e50; margin-bottom: 5px;">3.6</div>
    <div style="color: #6c757d; font-size: 13px; font-weight: 600;">
      → 0.2% <span style="font-weight: 400;">vs last month</span>
    </div>
  </div>
  
</div>
```

---

## USAGE INSTRUCTIONS

### How to Add These to Your Dashboard:

1. **Edit Dashboard** in Superset
2. Click **"Add Component"** → **"Markdown"**
3. **Copy** any template above
4. **Paste** into the Markdown editor
5. **Customize** colors, numbers, and text as needed
6. **Save** the component
7. **Drag and drop** to position it on your dashboard

### Tips for Best Results:

- Use **Template 1** at the very top of your main dashboard
- Use **Template 2 or Template 13** at the start of each page/tab
- Add **Template 3** (KPI cards) right after the header
- Use **Template 5** (instructions) for user guidance
- Add **Template 10** (footer) at the bottom of each page

### Customization:

- Replace numbers with actual metrics from your data
- Change colors by modifying hex codes (e.g., #667eea)
- Update dates and timestamps
- Modify text to match your use case
- Add your company logo URL in Template 1

---

Enjoy your professionally styled Superset dashboard! 🎨
