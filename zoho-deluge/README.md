# Zoho Deluge Codes

This folder contains all Deluge automation codes for FuseIT Global's Zoho ecosystem.

## Folder Structure

```
zoho-deluge/
├── recruit/          # Zoho Recruit automation codes
├── crm/              # Zoho CRM automation codes
├── flow/             # Zoho Flow automation codes
└── creator/          # Zoho Creator automation codes
```

## Recruit Codes

### 1. Application Update Workflow
- **Workflow Name**: `WF_Application_Update_CandidateJobAndApplication`
- **Function Name**: `fn_Application_UpdateCandidateJobAndApplication`
- **Trigger**: On Application creation
- **Purpose**: Updates candidate record with Application ID and Job ID

### 2. Interview Name Update Workflow
- **Workflow Name**: `wf_Interview_AddCandidateIdToInterviewName`
- **Function Name**: `fn_Interview_UpdateInterviewNameWithCandidateId`
- **Trigger**: On Interview creation
- **Purpose**: Appends candidate ID to interview name

### 3. Screening Feedback Job Association
- **Workflow Name**: `WF_ScreeningFeedback_OnCreate_AssociateJob`
- **Function Name**: `fn_UpdateJobLookupFromApplication`
- **Trigger**: On Screening Feedback creation
- **Purpose**: Associates job lookup from application to screening feedback

### 4. Interview Booking Button
- **Button Name**: `Invite to Schedule Call`
- **Module**: Candidate
- **Function Name**: `Send Interview Booking Link`
- **Purpose**: Sends scheduling link to candidates with personalized booking forms

### 5. Resume Approval Button
- **Button Name**: `Send Resume for Approval`
- **Module**: Candidate
- **Function Name**: `Send_Resume_Approval_Request`
- **Purpose**: Sends resume approval request email with formatted resume attachment

## Connection Requirements

- **Zoho Recruit Connection**: `zrecruit`
- All API calls use Zoho Recruit REST API v2

## Notes

- Resume Approval uses Zoho Creator form for candidate approval
- Interview Booking links are personalized per recruiter
- All emails include HTML formatted templates
