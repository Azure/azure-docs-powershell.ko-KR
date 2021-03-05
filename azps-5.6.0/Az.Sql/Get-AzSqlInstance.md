---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
ms.openlocfilehash: 53182c3f69359f654ee6f55ff679733b3b8c883f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999504"
---
# <span data-ttu-id="aeabf-101">Get-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="aeabf-101">Get-AzSqlInstance</span></span>

## <span data-ttu-id="aeabf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeabf-102">SYNOPSIS</span></span>
<span data-ttu-id="aeabf-103">Managed Database Instance에 대한 Azure SQL 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-103">Returns information about Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="aeabf-104">구문</span><span class="sxs-lookup"><span data-stu-id="aeabf-104">SYNTAX</span></span>

### <span data-ttu-id="aeabf-105">DefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="aeabf-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstance [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aeabf-106">ListByInstancePoolObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aeabf-106">ListByInstancePoolObjectParameterSet</span></span>
```
Get-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aeabf-107">ListByInstancePoolResourceIdentiferParameterSet</span><span class="sxs-lookup"><span data-stu-id="aeabf-107">ListByInstancePoolResourceIdentiferParameterSet</span></span>
```
Get-AzSqlInstance [-InstancePoolResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aeabf-108">GetByManagedInstanceResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="aeabf-108">GetByManagedInstanceResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstance [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aeabf-109">ListByInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="aeabf-109">ListByInstancePoolParameterSet</span></span>
```
Get-AzSqlInstance [-InstancePoolName] <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aeabf-110">설명</span><span class="sxs-lookup"><span data-stu-id="aeabf-110">DESCRIPTION</span></span>
<span data-ttu-id="aeabf-111">**Get-AzSqlInstance** cmdlet은 Managed Instances에 대한 하나 이상의 Azure SQL 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-111">The **Get-AzSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="aeabf-112">인스턴스의 이름을 지정하여 해당 인스턴스에 대한 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-112">Specify the name of an instance to see information for only that instance.</span></span>

## <span data-ttu-id="aeabf-113">예제</span><span class="sxs-lookup"><span data-stu-id="aeabf-113">EXAMPLES</span></span>

### <span data-ttu-id="aeabf-114">예제 1: 리소스 그룹에 할당된 모든 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-114">Example 1: Get all instances assigned to a resource group</span></span>
```powershell
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
```

<span data-ttu-id="aeabf-115">이 명령은 ResourceGroup01 리소스 그룹에 할당된 모든 인스턴스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-115">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="aeabf-116">예제 2: 인스턴스에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="aeabf-116">Example 2: Get information about an  instance</span></span>
```powershell
PS C:\> Get-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
```

<span data-ttu-id="aeabf-117">이 명령은 managedInstance1이라는 인스턴스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-117">This command gets information about the instance named managedInstance1.</span></span>

### <span data-ttu-id="aeabf-118">예제 3: 필터링을 사용하여 리소스 그룹에 할당된 모든 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-118">Example 3: Get all instances assigned to a resource group using filtering</span></span>
```powershell
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "managedInstance*"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
```

<span data-ttu-id="aeabf-119">이 명령은 "managedInstance"로 시작하는 리소스 그룹 ResourceGroup01에 할당된 모든 인스턴스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-119">This command gets information about all instances assigned to the resource group ResourceGroup01 that start with "managedInstance".</span></span>

### <span data-ttu-id="aeabf-120">예제 4: 인스턴스 풀 내의 모든 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-120">Example 4: Get all instances within an instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstancePoolName "instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="aeabf-121">이 명령은 인스턴스 풀 "instancePool0"내의 모든 인스턴스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-121">This command gets information about all instances within the instance pool "instancePool0".</span></span>

### <span data-ttu-id="aeabf-122">예제 5: 인스턴스 풀 개체를 사용하여 인스턴스 풀 내의 모든 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-122">Example 5: Get all instances within an instance pool using instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName "ResourceGroup01" -Name "instancePool0"
PS C:\> Get-AzSqlInstance -InstancePool $instancePool
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="aeabf-123">이 명령은 인스턴스 풀 "instancePool0"내의 모든 인스턴스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-123">This command gets information about all instances within the instance pool "instancePool0".</span></span>

### <span data-ttu-id="aeabf-124">예제 6: 인스턴스 풀 리소스 식별자를 사용하여 인스턴스 풀 내의 모든 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-124">Example 6: Get all instances within an instance pool using instance pool resource identifier</span></span>
```powershell
PS C:\> Get-AzSqlInstance -InstancePoolResourceIdentifier "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="aeabf-125">이 명령은 인스턴스 풀 "instancePool0"내의 모든 인스턴스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-125">This command gets information about all instances within the instance pool "instancePool0".</span></span>

### <span data-ttu-id="aeabf-126">예제 7: 리소스 식별자를 사용하여 관리되는 인스턴스를 얻다</span><span class="sxs-lookup"><span data-stu-id="aeabf-126">Example 7: Get a managed instance using its resource identifier</span></span>
```powershell
PS C:\> Get-AzSqlInstance -ResourceIdentifier "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="aeabf-127">이 명령은 managedInstance1이라는 인스턴스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-127">This command gets information about the instance named managedInstance1.</span></span>

## <span data-ttu-id="aeabf-128">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aeabf-128">PARAMETERS</span></span>

### <span data-ttu-id="aeabf-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeabf-129">-DefaultProfile</span></span>
<span data-ttu-id="aeabf-130">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeabf-131">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="aeabf-131">-InstancePool</span></span>
<span data-ttu-id="aeabf-132">인스턴스 풀 부모 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-132">The instance pool parent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: ListByInstancePoolObjectParameterSet
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aeabf-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="aeabf-133">-InstancePoolName</span></span>
<span data-ttu-id="aeabf-134">인스턴스 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-134">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeabf-135">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="aeabf-135">-InstancePoolResourceId</span></span>
<span data-ttu-id="aeabf-136">인스턴스 풀 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-136">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolResourceIdentiferParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeabf-137">-Name</span><span class="sxs-lookup"><span data-stu-id="aeabf-137">-Name</span></span>
<span data-ttu-id="aeabf-138">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-138">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: InstanceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeabf-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeabf-139">-ResourceGroupName</span></span>
<span data-ttu-id="aeabf-140">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-140">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeabf-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aeabf-141">-ResourceId</span></span>
<span data-ttu-id="aeabf-142">관리되는 인스턴스 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-142">The managed instance resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByManagedInstanceResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeabf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeabf-143">CommonParameters</span></span>
<span data-ttu-id="aeabf-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aeabf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeabf-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aeabf-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeabf-146">입력</span><span class="sxs-lookup"><span data-stu-id="aeabf-146">INPUTS</span></span>

### <span data-ttu-id="aeabf-147">없음</span><span class="sxs-lookup"><span data-stu-id="aeabf-147">None</span></span>

## <span data-ttu-id="aeabf-148">출력</span><span class="sxs-lookup"><span data-stu-id="aeabf-148">OUTPUTS</span></span>

### <span data-ttu-id="aeabf-149">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="aeabf-149">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="aeabf-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aeabf-150">NOTES</span></span>

## <span data-ttu-id="aeabf-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aeabf-151">RELATED LINKS</span></span>
