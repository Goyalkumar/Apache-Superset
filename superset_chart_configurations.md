# APACHE SUPERSET CHART CONFIGURATION TEMPLATES
# Professional Color Schemes and Settings

===============================================================================
These configurations help you create consistent, professional-looking charts
Copy these settings when creating new charts in Superset
===============================================================================

---

## COLOR PALETTES

### Primary Palette (Document Analytics Theme)
```
Colors to use across all charts for consistency:

Main Colors:
- Primary Purple: #667eea
- Secondary Purple: #764ba2
- Success Green: #4CAF50
- Warning Orange: #FF9800
- Error Red: #F44336
- Info Blue: #2196F3

Gradient Colors:
- Light Purple: #7e8df0
- Light Green: #66BB6A
- Light Orange: #FFB74D
- Light Red: #EF5350
- Light Blue: #42A5F5

Neutral Colors:
- Dark Gray: #2c3e50
- Medium Gray: #6c757d
- Light Gray: #adb5bd
- Very Light Gray: #e9ecef
- Background: #f8f9fa
```

### Category Colors (for multiple series)
```
Use these for charts with multiple categories:

Sequential Palette:
['#667eea', '#764ba2', '#4CAF50', '#2196F3', '#FF9800', '#F44336', '#9C27B0', '#00BCD4']

Status Palette:
- Classified: #4CAF50
- Pending: #FF9800
- Unknown: #F44336
- Archived: #6c757d
```

---

## 1. TABLE CHART CONFIGURATION

### Basic Settings:
```json
{
  "viz_type": "table",
  "datasource": "your_dataset",
  "groupby": ["document_name", "tag_name", "classification_status"],
  "metrics": ["count"],
  "all_columns": [],
  "order_desc": true,
  "row_limit": 100,
  "page_length": 25,
  "include_time": false,
  "order_by_cols": [],
  "table_timestamp_format": "%Y-%m-%d %H:%M",
  "show_cell_bars": true,
  "align_pn": true,
  "color_pn": true
}
```

### Advanced Formatting:
```json
{
  "conditional_formatting": [
    {
      "column": "classification_status",
      "operator": "==",
      "value": "Classified",
      "colorScheme": "#4CAF50"
    },
    {
      "column": "classification_status",
      "operator": "==",
      "value": "Unknown",
      "colorScheme": "#F44336"
    },
    {
      "column": "classification_status",
      "operator": "==",
      "value": "Pending",
      "colorScheme": "#FF9800"
    }
  ]
}
```

### Custom CSS for Tables:
```css
.table-chart {
  font-family: 'Segoe UI', sans-serif;
}

.table-chart th {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%) !important;
  color: white !important;
  font-weight: 600 !important;
  text-transform: uppercase;
  font-size: 12px;
  letter-spacing: 0.5px;
}

.table-chart tbody tr:hover {
  background-color: #e7f1ff !important;
}
```

---

## 2. LINE CHART CONFIGURATION

### Basic Settings:
```json
{
  "viz_type": "echarts_timeseries_line",
  "datasource": "your_dataset",
  "metrics": ["count"],
  "groupby": ["classification_status"],
  "time_grain_sqla": "P1D",
  "time_range": "Last month",
  "color_scheme": "supersetColors",
  "show_legend": true,
  "rich_tooltip": true,
  "show_markers": true,
  "line_interpolation": "linear",
  "x_axis_title": "Date",
  "y_axis_title": "Document Count",
  "y_axis_format": ",d"
}
```

### Custom Color Mapping:
```json
{
  "color_scheme": "Custom",
  "label_colors": {
    "Classified": "#4CAF50",
    "Pending": "#FF9800",
    "Unknown": "#F44336"
  }
}
```

### Advanced Styling:
```json
{
  "x_axis_title_margin": 30,
  "y_axis_title_margin": 50,
  "x_axis_label_rotation": 0,
  "show_value": false,
  "markerSize": 6,
  "opacity": 0.8,
  "seriesType": "line",
  "stack": false,
  "area": false,
  "show_extra_controls": true,
  "extra_form_data": {
    "time_compare": ["1 month ago"]
  }
}
```

---

## 3. PIE/DONUT CHART CONFIGURATION

### Basic Settings:
```json
{
  "viz_type": "pie",
  "datasource": "your_dataset",
  "metric": "count",
  "groupby": ["classification_status"],
  "color_scheme": "Custom",
  "show_labels": true,
  "show_legend": true,
  "labels_outside": true,
  "show_labels_threshold": 5,
  "donut": true,
  "innerRadius": 50,
  "outerRadius": 80
}
```

### Custom Colors:
```json
{
  "label_colors": {
    "Classified": "#4CAF50",
    "Pending": "#FF9800", 
    "Unknown": "#F44336",
    "Archived": "#6c757d"
  }
}
```

### Donut with Center Label:
```json
{
  "donut": true,
  "innerRadius": 60,
  "show_labels": true,
  "number_format": ",d",
  "pie_label_type": "key_percent",
  "show_legend": true,
  "legend_orient": "right",
  "legend_type": "scroll"
}
```

---

## 4. BAR CHART CONFIGURATION

### Horizontal Bar Chart:
```json
{
  "viz_type": "echarts_timeseries_bar",
  "datasource": "your_dataset",
  "metrics": ["count"],
  "groupby": ["tag_name"],
  "color_scheme": "Custom",
  "label_colors": {
    "default": "#667eea"
  },
  "show_legend": false,
  "rich_tooltip": true,
  "y_axis_format": ",d",
  "x_axis_title": "Tag Name",
  "y_axis_title": "Count",
  "bar_orientation": "horizontal",
  "row_limit": 20,
  "order_desc": true
}
```

### Stacked Bar Chart:
```json
{
  "viz_type": "echarts_timeseries_bar",
  "datasource": "your_dataset",
  "metrics": ["count"],
  "groupby": ["document_type"],
  "columns": ["classification_status"],
  "color_scheme": "Custom",
  "label_colors": {
    "Classified": "#4CAF50",
    "Pending": "#FF9800",
    "Unknown": "#F44336"
  },
  "show_legend": true,
  "stack": true,
  "show_bar_value": false,
  "bar_orientation": "vertical"
}
```

---

## 5. BIG NUMBER / KPI CARD CONFIGURATION

### Simple KPI:
```json
{
  "viz_type": "big_number_total",
  "datasource": "your_dataset",
  "metric": "count",
  "subheader": "Total Documents",
  "y_axis_format": ",d",
  "time_range": "Last month",
  "compare_lag": "1 month",
  "compare_suffix": "month"
}
```

### KPI with Trend:
```json
{
  "viz_type": "big_number",
  "datasource": "your_dataset", 
  "metric": "count",
  "subheader": "Documents Classified",
  "y_axis_format": ",d",
  "time_range": "Last month",
  "show_trend_line": true,
  "start_y_axis_at_zero": true,
  "color_picker": {
    "r": 102,
    "g": 126,
    "b": 234,
    "a": 1
  }
}
```

### Custom CSS for KPI Cards:
```css
.big-number-total {
  text-align: center;
  padding: 30px;
}

.big-number-total .metric-value {
  font-size: 48px;
  font-weight: 700;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.big-number-total .metric-label {
  font-size: 14px;
  color: #6c757d;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: 600;
  margin-top: 10px;
}
```

---

## 6. FILTER BOX CONFIGURATION

### Multiple Filters:
```json
{
  "viz_type": "filter_box",
  "datasource": "your_dataset",
  "date_filter": true,
  "filter_configs": [
    {
      "column": "document_name",
      "label": "Document Name",
      "asc": true,
      "clearable": true,
      "multiple": true,
      "searchAllOptions": true
    },
    {
      "column": "classification_status",
      "label": "Classification Status",
      "asc": true,
      "clearable": true,
      "multiple": true
    },
    {
      "column": "tag_name",
      "label": "Tag Name",
      "asc": true,
      "clearable": true,
      "multiple": true,
      "searchAllOptions": true
    },
    {
      "column": "department",
      "label": "Department",
      "asc": true,
      "clearable": true,
      "multiple": false
    }
  ]
}
```

---

## 7. MULTI-ROW CARD CONFIGURATION

### Basic Settings:
```json
{
  "viz_type": "paired_ttest",
  "datasource": "your_dataset",
  "metrics": ["count", "avg_tags"],
  "groupby": ["document_name"],
  "row_limit": 10,
  "order_desc": true
}
```

---

## 8. CROSS-FILTERING SETUP

### Enable Cross-Filtering:
```json
{
  "dashboards": ["your_dashboard_id"],
  "default_filters": {},
  "chart_configuration": {
    "CHART_ID": {
      "crossFilters": {
        "scope": "global",
        "chartsInScope": ["CHART_ID_2", "CHART_ID_3"]
      }
    }
  }
}
```

---

## 9. CHART TITLES AND DESCRIPTIONS

### Consistent Title Format:
```
Title: Clear, Action-Oriented Titles
Examples:
- "Document Classification Status Over Time"
- "Top 10 Most Used Tags"
- "Parent-Child Document Relationships"
- "Unknown Tags Requiring Review"

Description: 
- What: Brief explanation of what the chart shows
- Why: Why this metric matters
- How: How to interact with the chart

Example:
"This chart displays the distribution of classification statuses across all documents. 
Use the filters above to narrow down by department or date range. 
Click on any segment to drill down into specific documents."
```

---

## 10. DASHBOARD-LEVEL SETTINGS

### Dashboard Metadata:
```json
{
  "color_scheme": "Custom",
  "label_colors": {
    "Classified": "#4CAF50",
    "Pending": "#FF9800",
    "Unknown": "#F44336",
    "Archived": "#6c757d"
  },
  "shared_label_colors": true,
  "color_scheme_domain": [
    "#667eea",
    "#764ba2", 
    "#4CAF50",
    "#FF9800",
    "#F44336",
    "#2196F3"
  ],
  "refresh_frequency": 300,
  "timed_refresh_immune_slices": [],
  "filter_configs_expanded": false
}
```

### Global Filters:
```json
{
  "native_filter_configuration": [
    {
      "id": "filter_1",
      "controlValues": {
        "enableEmptyFilter": true,
        "defaultToFirstItem": false,
        "multiSelect": true,
        "searchAllOptions": true,
        "inverseSelection": false
      },
      "name": "Classification Status",
      "filterType": "filter_select",
      "targets": [
        {
          "datasetId": "your_dataset_id",
          "column": {
            "name": "classification_status"
          }
        }
      ],
      "defaultDataMask": {
        "extraFormData": {},
        "filterState": {}
      }
    },
    {
      "id": "filter_2",
      "controlValues": {
        "enableEmptyFilter": true,
        "defaultToFirstItem": false,
        "multiSelect": true,
        "searchAllOptions": true
      },
      "name": "Date Range",
      "filterType": "filter_timecolumn",
      "targets": [
        {
          "datasetId": "your_dataset_id",
          "column": {
            "name": "__time"
          }
        }
      ],
      "defaultDataMask": {
        "extraFormData": {
          "time_range": "Last month"
        }
      }
    }
  ]
}
```

---

## 11. SQL TEMPLATES FOR CUSTOM DATASETS

### Document Classification Summary:
```sql
SELECT 
    d.document_id,
    d.document_name,
    d.document_type,
    d.created_date,
    CASE 
        WHEN COUNT(t.tag_id) = 0 THEN 'Untagged'
        WHEN SUM(CASE WHEN t.classification_status = 'Unknown' THEN 1 ELSE 0 END) > 0 
            THEN 'Unknown'
        WHEN SUM(CASE WHEN t.classification_status = 'Pending' THEN 1 ELSE 0 END) > 0 
            THEN 'Pending'
        ELSE 'Classified'
    END as overall_status,
    COUNT(DISTINCT t.tag_id) as tag_count,
    STRING_AGG(t.tag_name, ', ') as tags,
    MAX(t.last_updated) as last_tag_update
FROM documents d
LEFT JOIN document_tags dt ON d.document_id = dt.document_id
LEFT JOIN tags t ON dt.tag_id = t.tag_id
GROUP BY d.document_id, d.document_name, d.document_type, d.created_date
```

### Tag Usage Statistics:
```sql
SELECT 
    t.tag_id,
    t.tag_name,
    t.tag_category,
    t.classification_status,
    COUNT(DISTINCT dt.document_id) as document_count,
    COUNT(DISTINCT CASE WHEN d.document_type = 'Parent' THEN d.document_id END) as parent_count,
    COUNT(DISTINCT CASE WHEN d.document_type = 'Child' THEN d.document_id END) as child_count,
    AVG(DATEDIFF(day, d.created_date, dt.tagged_date)) as avg_days_to_tag,
    MIN(dt.tagged_date) as first_used,
    MAX(dt.tagged_date) as last_used
FROM tags t
LEFT JOIN document_tags dt ON t.tag_id = dt.tag_id
LEFT JOIN documents d ON dt.document_id = d.document_id
GROUP BY t.tag_id, t.tag_name, t.tag_category, t.classification_status
HAVING COUNT(DISTINCT dt.document_id) > 0
ORDER BY document_count DESC
```

### Parent-Child Relationships:
```sql
SELECT 
    parent.document_id as parent_id,
    parent.document_name as parent_name,
    child.document_id as child_id,
    child.document_name as child_name,
    COUNT(DISTINCT ct.tag_id) as shared_tags,
    STRING_AGG(DISTINCT t.tag_name, ', ') as tag_list
FROM documents parent
INNER JOIN document_relationships dr ON parent.document_id = dr.parent_doc_id
INNER JOIN documents child ON dr.child_doc_id = child.document_id
LEFT JOIN document_tags pt ON parent.document_id = pt.document_id
LEFT JOIN document_tags ct ON child.document_id = ct.document_id AND pt.tag_id = ct.tag_id
LEFT JOIN tags t ON ct.tag_id = t.tag_id
GROUP BY parent.document_id, parent.document_name, child.document_id, child.document_name
```

---

## 12. QUICK REFERENCE GUIDE

### Chart Type Selection:
```
Use Case                          → Recommended Chart Type
─────────────────────────────────────────────────────────
Show exact values                 → Table
Compare categories                → Bar Chart
Show trends over time             → Line Chart
Show proportions/percentages      → Pie/Donut Chart
Display single metric             → Big Number/KPI
Show multiple KPIs                → Multi-Row Card
Filter data                       → Filter Box
Show distribution                 → Histogram
Compare two measures              → Scatter Plot
Show relationships                → Sankey Diagram
Geographic data                   → Map
```

### Color Usage Guidelines:
```
Context                → Color
─────────────────────────────────
Success/Completed      → #4CAF50 (Green)
Warning/Pending        → #FF9800 (Orange)
Error/Unknown          → #F44336 (Red)
Info/General           → #2196F3 (Blue)
Primary Action         → #667eea (Purple)
Secondary Action       → #764ba2 (Dark Purple)
Neutral/Inactive       → #6c757d (Gray)
```

---

## IMPLEMENTATION CHECKLIST

□ Apply consistent color scheme across all charts
□ Set appropriate number formats (,d for integers, .2f for decimals)
□ Add clear titles and descriptions
□ Configure tooltips for better UX
□ Enable cross-filtering where relevant
□ Set appropriate row limits
□ Configure drill-down options
□ Add legends where needed
□ Set proper axis titles and labels
□ Apply conditional formatting to tables
□ Configure refresh intervals
□ Test on mobile viewport
□ Add help text/instructions
□ Set up appropriate default filters
□ Configure export options

---

Ready to create professional charts! 📊
