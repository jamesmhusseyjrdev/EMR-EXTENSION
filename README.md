# EMR-EXTENSION
# EMR Notes Helper

## Overview

**EMR Notes Helper** is a Chrome extension designed to assist healthcare providers with **CDI (Clinical Documentation Improvement)** and **InterQual criteria documentation** while writing notes in the EMR.

When a diagnosis such as **CHF** or **COPD** is detected in the Notes editor, the extension automatically displays a **slide-out documentation panel** that allows the provider to select appropriate clinical criteria. The selected criteria are then inserted directly into the note with one click.

The extension helps ensure documentation supports **medical necessity, level of care, and CDI requirements**.

---

# Installation

## Method 1 – Install from Local Folder (Recommended for Internal Use)

1. Download or copy the extension folder to your computer.
2. Open **Google Chrome**.
3. Navigate to:

```
chrome://extensions
```

4. Enable **Developer Mode** (top-right corner).
5. Click **Load unpacked**.
6. Select the folder containing the extension files.

The extension will now appear in Chrome and automatically activate on supported EMR pages.

---

# Supported Environment

The extension is designed for EMR systems hosted under:

```
https://*.plt.trubridge.com
```

It activates when the **Notes editor (CKEditor)** is detected.

---

# Features

## Automatic Diagnosis Detection

The extension monitors the Notes editor. When a supported diagnosis keyword is detected (examples below), the documentation panel automatically appears.

Example triggers:

* CHF
* Congestive Heart Failure
* COPD
* Chronic Obstructive Pulmonary Disease

Detection is configurable via the **diagnoses configuration file**.

---

## Slide-Out Documentation Panel

When a diagnosis is detected, a **right-side slide-out panel** opens automatically.

The panel contains documentation criteria organized into collapsible sections:

* CDI Documentation
* Observation Criteria
* Acute Inpatient Criteria
* Intermediate Inpatient Criteria
* Critical Care Criteria

Providers select the criteria that apply to the patient.

---

## One-Click Note Insertion

After selecting the applicable criteria, click:

```
Insert into Note
```

The extension will automatically insert structured documentation into the note editor.

Example output:

```
CHF – CDI Documentation
- Acuity: Acute
- Type: Systolic

CHF – Observation Criteria
- Trigger: Shortness of breath
- Findings: Pulmonary edema

CHF – Acute Inpatient Criteria
- Symptoms: Severe dyspnea
- Interventions: IV diuretics
```

---

## Validation Protection

Before inserting documentation, the extension verifies that required criteria are selected.

If required selections are missing, a message will appear indicating which criteria must be completed.

---

## Diagnosis-Specific Snooze

If the provider dismisses the panel, the extension will temporarily suppress the popup for that diagnosis to avoid interruptions while charting.

---

## Popup Position Preferences

Users can control where the slide-out panel appears:

* Right side
* Left side
* Bottom-right
* Bottom-left

Preferences are saved automatically using Chrome's local storage.

---

# Diagnosis Builder (Administrative Tool)

The extension includes a **Diagnosis Builder** for administrators or CDI teams to manage diagnoses without editing code.

The builder allows you to:

* Add new diagnoses
* Define trigger keywords
* Create documentation sections
* Add criteria fields
* Define validation rules
* Export updated configuration files

The builder stores settings locally but can export a new **diagnoses.json** file for distribution.

---

# Supported Diagnoses

Current configuration includes:

* Congestive Heart Failure (CHF)
* Chronic Obstructive Pulmonary Disease (COPD)

Additional diagnoses can be added through the builder.

---

# Workflow Example

1. Provider begins writing a note.
2. The provider documents:

```
Patient admitted with acute CHF exacerbation.
```

3. The extension detects **CHF**.
4. The documentation panel slides out.
5. Provider selects applicable criteria.
6. Provider clicks **Insert into Note**.
7. Documentation is automatically added to the note.

---

# Privacy & Security

The extension:

* Does **not transmit patient data externally**
* Runs entirely inside the browser
* Uses **Chrome local storage** for configuration and preferences
* Only activates on approved EMR domains

---

# Troubleshooting

## Extension Does Not Appear

Verify:

* Chrome Developer Mode is enabled
* Extension folder was loaded correctly
* Page URL matches:

```
*.plt.trubridge.com
```

---

## Panel Does Not Open

Confirm the diagnosis keyword exists in the note text.

Example:

```
CHF
COPD
Congestive heart failure
```

---

## Criteria Not Inserting

Make sure all required criteria selections are completed before clicking **Insert into Note**.

---

# Version

Current Version: **0.1.1**

---

# Future Enhancements

Planned improvements include:

* Central configuration server
* Role-based diagnosis management
* Provider-specific preferences
* Expanded diagnosis library
* Improved CDI narrative formatting

---

# Support

For technical support or configuration updates, contact your IT department or the extension administrator.

