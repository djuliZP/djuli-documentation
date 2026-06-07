# Navigation

Contextual help content for the **left-hand sidebar** of the Djuli web application - the cluster, project and report tree the user uses to move around their workspace.

## Documented elements

| Folder | What it documents |
|---|---|
| [`activeClusters/`](./activeClusters) | Filter that shows only the clusters you are currently working with |
| [`archiveCluster/`](./archiveCluster) | Move the selected cluster to *Archived* |
| [`addCluster/`](./addCluster) | The Clusters header and the "+" icon to create a new cluster |
| [`addProject/`](./addProject) | The "+" icon to add a new project under a cluster |
| [`addReport/`](./addReport) | The "+" icon to add a new report under a project |
| [`approveCluster/`](./approveCluster) | Approve an incoming access request for a cluster |
| [`approveProject/`](./approveProject) | Approve an incoming access request for a project |
| [`approveReport/`](./approveReport) | Approve an incoming access request for a report |
| [`allClusters/`](./allClusters) | Filter that shows every cluster regardless of status |
| [`archivedClusters/`](./archivedClusters) | Filter that shows only archived clusters |
| [`combineReports/`](./combineReports) | Merge data lines from several reports into one working set |
| [`compareReports/`](./compareReports) | Selecting two reports for side-by-side comparison |
| [`deleteClusters/`](./deleteClusters) | Cancel your outgoing cluster access requests |
| [`deleteProjects/`](./deleteProjects) | Cancel your outgoing project access requests |
| [`deleteReports/`](./deleteReports) | Cancel your outgoing report access requests |
| [`detailCluster/`](./detailCluster) | Open the details of an incoming cluster access request |
| [`detailProject/`](./detailProject) | Open the details of an incoming project access request |
| [`detailReport/`](./detailReport) | Open the details of an incoming report access request |
| [`downloadRawFiles/`](./downloadRawFiles) | Download the original raw data files for the selected report(s) |
| [`editCluster/`](./editCluster) | Rename a cluster or edit its description |
| [`editProject/`](./editProject) | Rename a project or edit its description |
| [`editReport/`](./editReport) | Rename a report or edit its top-level metadata |
| [`favouriteCluster/`](./favouriteCluster) | Mark the selected cluster as a favourite |
| [`favouriteClusters/`](./favouriteClusters) | Filter that shows only clusters you marked as favourites |
| [`hyperlinkReport/`](./hyperlinkReport) | Link an existing report from another project into this one |
| [`navigationTree/`](./navigationTree) | The accordion tree of clusters and projects you own |
| [`navigationTreeShared/`](./navigationTreeShared) | The accordion tree of items shared *with* you by others |
| [`optOutSharedCluster/`](./optOutSharedCluster) | Remove your access to a cluster someone shared with you |
| [`projectName/`](./projectName) | A project row in the tree |
| [`refreshCluster/`](./refreshCluster) | Refresh icon while viewing clusters |
| [`refreshProject/`](./refreshProject) | Refresh icon while viewing projects under a cluster |
| [`refreshReport/`](./refreshReport) | Refresh icon while viewing reports under a project |
| [`refreshTree/`](./refreshTree) | *(legacy)* Historical route - superseded by the three per-view refresh entries above |
| [`rejectClusters/`](./rejectClusters) | Reject incoming cluster access requests |
| [`rejectProjects/`](./rejectProjects) | Reject incoming project access requests |
| [`rejectReports/`](./rejectReports) | Reject incoming report access requests |
| [`removeReports/`](./removeReports) | Deleting a report from a project |
| [`restoreCluster/`](./restoreCluster) | Move an archived cluster back to *Active* |
| [`shareCluster/`](./shareCluster) | Share a whole cluster with another user |
| [`shareReport/`](./shareReport) | Sharing a report with another user |
| [`tableReports/`](./tableReports) | The table view that lists reports inside a project |
| [`unfavouriteCluster/`](./unfavouriteCluster) | Remove the selected cluster from your favourites |

## UI hierarchy

```
Cluster
  └─ Project
       └─ Report
            └─ Study (analysis applied to the report's data)
```

A user can own clusters (`navigationTree`) and also see clusters shared by collaborators (`navigationTreeShared`). All write actions (add, remove, share) act on the currently-selected node in the tree.

## Adding a new entry

If you are documenting a new element in this area:

1. Create `Navigation/<elementName>/main.md`.
2. Add any referenced images (PNG, GIF) in the same folder using **relative** paths.
3. Make sure the matching `setContextualHelp('Navigation/<elementName>')` call exists in `djuli-webapp` - otherwise the panel will never load this content.