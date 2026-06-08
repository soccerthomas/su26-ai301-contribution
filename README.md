# su26-ai301-contribution
# Contribution 1: Add Update Download Status to UI

**Contribution Number:** 1
**Student:** Thomas Lavadinho
**Issue:** https://github.com/session-foundation/session-desktop/issues/904
**Status:** Phase I Complete

---

## Why I Chose This Issue

I chose this issue because it seemed like a good first contribution that is pretty specific and not too huge. I wanted something where I could actually understand what is going on without needing to learn the entire codebase first.

It also seemed interesting because it involves improving the user experience. Right now the app updates in the background but the user does not really know if anything is happening. I also thought it would be a good way to learn more about Electron apps and how desktop applications handle updates.

---

## Understanding the Issue

### Problem Description

When a user updates Session Desktop, the update downloads in the background, but there is no message or progress shown in the UI. This can make it seem like nothing is happening.

### Expected Behavior

The app should show some kind of notice or indicator that an update is downloading.

### Current Behavior

The update downloads silently in the background after clicking the update button.

### Affected Components

Based on the issue discussion, this likely involves:

* Update handling logic (`electron-updater`)
* UI components related to update notifications
* Possibly communication between the updater and frontend state

---

## Reproduction Process

### Environment Setup

I forked the repository and started setting up the project locally. I installed Node.js, pnpm, Visual Studio build tools, CMake, Git LFS, and initialized submodules. I ran into some Windows setup issues related to native dependencies and build configuration, so local setup is still in progress.

### Steps to Reproduce

1. Open Session Desktop.
2. Get the “update available” popup.
3. Click to download the update.
4. Notice there is no visible UI feedback while it downloads.

### Reproduction Evidence

* **Commit showing reproduction:** Setup still in progress
* **Screenshots/logs:** N/A
* **My findings:** From the issue discussion, it seems the update works in the background but there is no visible progress shown to the user.

---

## Solution Approach

### Analysis

It looks like the updater already downloads updates, but the UI is not showing any status or progress to the user.

### Proposed Solution

My plan is to look into how update events are handled and see if download progress can be shown somewhere in the UI, either through a small notification or status indicator.

### Implementation Plan

**Understand:** Figure out how updates currently work in Session Desktop.

**Match:** Look at maintainer comments and any existing updater-related code.

**Plan:**

1. Find where update downloads are handled.
2. Look for UI components related to updates or notifications.
3. Add a way to show download status in the UI.
4. Test the update flow locally.

**Implement:** Local branch created: `feature/update-download-status-ui`

**Review:** Make sure the change is small, clean, and follows the project style.

**Evaluate:** Verify the user sees some feedback when an update is downloading.

---

## Testing Strategy

### Unit Tests

* [ ] Update status appears when download starts
* [ ] UI updates correctly during download
* [ ] Status disappears after completion

### Integration Tests

* [ ] Verify update events reach the UI
* [ ] Test update flow end-to-end

### Manual Testing

Try triggering an update and confirm the UI shows that the download is happening.

---

## Pull Request

**PR Link:** Not submitted yet

**Status:** Phase I Complete

---

## Learnings & Reflections

### Technical Skills Gained

Learned more about setting up a large open-source project and desktop app tooling.

### Challenges Overcome

Had to work through Windows setup issues with build tools, CMake, submodules, and dependencies.

### What I'd Do Differently Next Time

Probably verify setup requirements earlier before spending a lot of time troubleshooting environment issues.

---

## Resources Used

* GitHub issue discussion
* Session Desktop README / CONTRIBUTING docs
* Electron updater documentation
