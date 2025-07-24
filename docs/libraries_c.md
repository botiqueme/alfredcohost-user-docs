<div data-toc-depth="3"></div>

# Libraries

In the Alfred Co.Host platform, a **library** is the structured set of information Alfred uses to respond to guest questions for a specific property.

Each property has its own library. This library contains all the relevant information about the unit — from how to turn on the heating to where to eat nearby. When you build a property library, you collect and organize:

- **Accommodation information**: general descriptions of the property, such as its location, features, area, and style.  
- **Devices and appliances**: instructions and troubleshooting for devices in the property, such as Wi-Fi, TV, kitchen appliances, etc.  
- **Household systems & troubleshooting**: guidance and troubleshooting for systems like electricity, water, heating, or A/C.  
- **Local tips**: suggestions for food, transport, sightseeing, and other local insights.  
- **Policies & procedures**: house rules and instructions related to the guest stay and the relationship with the host.  
- **Staff-only info**: internal notes for maintenance or guest-related details. Only visible to staff — never shown to guests.

> **NOTE** The richer and clearer your library is, the more helpful Alfred becomes.

## How it works

Each property’s library is made of **information units**. Some are predefined (we mapped them for you), others can be fully customized.

When Alfred identifies the guest’s property, it uses the related library to answer questions — whether the guest is asking for practical help, descriptive details, or trying to reach a human host.

Information units come in two types: **Native**, which we provide as predefined fields, and **custom**, which you can fully define.

Information can also be either **textual** or **media-based**:

- [Native textual information](#native-textual-information)
- [Custom textual information](#custom-textual-information)
- [Native media information](#native-media-information)
- [Custom media information](#custom-media-information)

Alfred uses this information **as-is**, or combines it with other sources depending on the complexity of the guest’s request.

### Native textual information

Predefined fields where you can enter a text value.  
For example:

| Information unit | Description | Custom value |
| --- | --- | --- |
| Property address | Address to locate the property | `123 Oxford Street, London` |

Fill in only what you need — leave the rest blank.

### Custom textual information
Custom fields where you define both the label and the text value.  
For example:

| Custom information unit | Custom description | Custom value |
| --- | --- | --- |
| `Parking instructions` | `Procedure to trigger parking gate opening` | `Use the garage remote stored in the kitchen cupboard` |

### Native media information

Predefined fields where you can add media (e.g. photos or videos).  
For example:

|Information unit | Description | Value |
| --- | --- | --- |
| How to launch the washing machine | Tutorial to launch washing machine cycle | `washing_machine_tutorial.mp4`|
| Fridge shelves detail | Detail about assigned shelf | `roomA_fridge_shelf.png` |

Format supported:
- image: MP4, 3GP up to 25Mb
- video: JPG, JPEG, PNG up to 25Mb

### Custom media information

Custom fields where you define the label, an optional description, and the media file.  
For example:

|Custom information unit | Custom description | Custom value |
| --- | --- |--- |
|`How to unlock the backyard door` | `Procedure to unlock the backyard door` | `backyard_door_opening_demo.mp4`
|`How to open/close the terrace curtain` | `Detail of the curtain mechanism` | `curtain_lock.png`| 

Format supported:
- image: MP4, 3GP up to 25Mb
- video: JPG, JPEG, PNG up to 25Mb
