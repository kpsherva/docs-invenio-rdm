# Administration panel views

**Summary**

The following document is a reference guide to the commands provided by the
Invenio-CLI tool.

**Intended audience**

This guide is intended for system administrators and developers of InvenioRDM.

**Overview**

Invenio administration panel gives the administrator a set of tools to effectively manage an instance of InvenioRDM.

## Domain dictionary
    
The following terms are introduced to facilitate defining the problem

- `administration panel` - the interface panel enabling a `manager` to administrate the instance of InvenioRDM in a developer-independent way.
- `administrator` - a person with domain knowledge, with a special set of permissions, able to manage an InvenioRDM instance, not necessarily having developer skills.
- `frontsite` `end user interface` - currently known InvenioRDM interface, accessible by anonymous and logged in users, without administrator role.
- `administration view` - subpages of the administration panel

## Administration panel

### Permissions

Administration panel is accessible only to an user with `administrator` role.

### Customise

You can customise your individual permissions per view by overwriting `decorators` class attribute as shown below. 
For more details on configuring administration views, follow the rest of this guide.

```python
from flask_security import roles_required

class MyView:
        decorators = [roles_required("my-role")]
```

### Configuration

## Views

// TODO paste the wireframe image from the RFC
An instance developer can register new entries in the menu (see backend RFC). A menu entry will display the associated views in the panel section. The navbar menu layouts are customizable to meet the needs of the InvenioRDM instance.

### Create a resource based administration view

// TODO
// TODO add example: OAI-pmh views
// TODO highlight which view classes need to be inherited

#### List view

// TODO

#### Create view

// TODO

#### Edit view

// TODO

#### Details view

// TODO

## Create custom view

// TODO
// TODO

## Customisation: dashboard view

// TODO

## Customisation: jinja templates

// TODO
// TODO mention about which blocks we have available to override
// TODO include information about placing respective javascript blocks and using {{ super() }}
// TODO add link to jinja documentation for more details

## Customisation: React components

// TODO 
// example: how we overrode the oai-pmh list view rows
// TODO mention of keeping correct react root ids (unique)