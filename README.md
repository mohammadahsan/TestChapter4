| Parameter     | Description |
|---------------|----------------------------------|
| **-Name**     | Account unique name for your resource group.    |
| **-Location** | Geographic region associated with all assets in the group. For a full list of locations, invoke `Get-AzureRmLocation`. |

3.  **Creating an Azure Storage Account:** Creating an Azure Storage Account will require a resource group. Use `New-AzureRmStorageAccount` to create a new Azure Storage. The parameters can be given in a single line. If not given it will prompt you for each parameter. The following are the possible parameters:


<table>
    <thead>
        <tr>
        <th width = "22%" >Parameter</th>
        <th style="width:70%">Description </th>
        </tr>
        <tr>
        <th align ="left">-ResourceGroupName</th>
        <td>A resource group to group this Azure asset into.</td>
        </tr>
        <tr>
        <th align ="left">-Name</th>
        <td>Globally unique name for your blob storage. Name must be between 3 and 24 characters in length and use numbers and lower-case letters only.</td>
        </tr>
        <tr>
        <th align ="left">-SkuName</th>
        <td>he replication desired in your storage account. A full table is listed below of storage SKUs.</td>
        </tr>
        <tr>
        <th align ="left">-Location</th>
        <td>Geographic region that you want your Azure Storage to reside. This should be the same as the cluster geographic location. For a full list of locations, invoke <code>Get-AzureRmLocation</code>.</td>
        </tr>
</thead>
</table>



| Parameter                | Description                |
|--------------------------|----------------------------|
| **-ResourceGroupName**  | A resource group to group this Azure asset into.    |
| **-Name**                | Globally unique name for your blob storage. Name must be between 3 and 24 characters in length and use numbers and lower-case letters only.     |
| **-SkuName**             | The replication desired in your storage account. A full table is listed below of storage SKUs. |
| **-Location**            | Geographic region that you want your Azure Storage to reside. This should be the same as the cluster geographic location. For a full list of locations, invoke `Get-AzureRmLocation`.   |

| Storage SkuNames       | Description       |
|--------------|-----------------|
| Standard_LRS          | Locally-redundant storage. Makes multiple synchronous copies of your data within a single datacenter      |
| Standard_ZRS          | Zone-redundant storage. Stores three copies of data across multiple datacenters within or across regions. For block blobs only. |
| Standard_GRS          | Geo-redundant storage. Same as LRS, plus multiple asynchronous copies to a second datacenter hundreds of miles away.   |
| Standard_RAGRS    | Read access geo-redundant storage. Same as GRS, plus read access to the secondary datacenter.  |
