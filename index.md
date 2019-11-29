# Sphereon Alfresco Blockchain integration

## Alfreco configuration

### Model & site setup

- Open Alfresco share (http://alfresco.demo/share if Alfresco is available at http://alfresco.demo)
- Navigate to Admin tools → Model manager
- Import model: [sphereon-alfresco-blockchain-model.zip](model/sphereon-alfresco-blockchain-model.zip)
- Create new site (Share → Sites in top menu bar → Create Site)
  + Collaborator Site
  + Private
- Add blockchain-agent user as a collaborator on the site
- Add blockchain aspect to site
  + Sites → Open newly created site → Document library (Top right) → Documents (Top left of folder view) → Manage aspects (Right sidemenu)
  + In the left pane, click (plus) on Blockchain Registration State and apply changes
- Add a rule to automatically apply the blockchain aspect to files and folders
  + Sites → Open newly created site → Document library (Top right) → Documents (Top left of folder view) → Manage rules (Right sidemenu)
  + Create rules (link without text-underline on hover in left section)
  + Name: Apply Blockchain Aspect
  + When: Items are created or enter this folder
  + Criteria: All items
  + Perform action: Apply Aspect, "Blockchain Registration State"
  + Make sure "Run in background" and "Apply to subfolders" are selected
- To optionally make folders sign documents automatically, add a rule
  + Rule: New file → Set bc:BlockchainRegistrationState to PENDING_REGISTRATION