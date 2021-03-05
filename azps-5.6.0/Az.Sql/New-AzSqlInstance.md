---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: 9f648f0e2ab15919f3caa849041846570d627df5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970203"
---
# <span data-ttu-id="c9d35-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c9d35-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="c9d35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9d35-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d35-103">Azure SQL Managed Instance를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="c9d35-104">구문</span><span class="sxs-lookup"><span data-stu-id="c9d35-104">SYNTAX</span></span>

### <span data-ttu-id="c9d35-105">NewByEditionAndComputeGenerationParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c9d35-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9d35-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9d35-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9d35-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9d35-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9d35-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="c9d35-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9d35-109">설명</span><span class="sxs-lookup"><span data-stu-id="c9d35-109">DESCRIPTION</span></span>
<span data-ttu-id="c9d35-110">**New-AzSqlInstance** cmdlet은 Azure SQL 데이터베이스 관리 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="c9d35-111">예제</span><span class="sxs-lookup"><span data-stu-id="c9d35-111">EXAMPLES</span></span>

### <span data-ttu-id="c9d35-112">예제 1: 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="c9d35-112">Example 1: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4 -DnsZonePartner "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/partnerServerForDnsZone"
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
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="c9d35-113">이 명령은 SkuName 매개 변수를 사용하여 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="c9d35-114">예제 2: 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="c9d35-114">Example 2: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="c9d35-115">이 명령은 Edition 및 ComputeGeneration 매개 변수를 사용하여 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="c9d35-116">예제 3: 인스턴스 풀 개체를 사용하여 인스턴스 풀에서 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="c9d35-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="c9d35-117">이 명령은 인스턴스 풀 개체를 사용하여 인스턴스 풀에 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="c9d35-118">예제 4: 인스턴스 풀 리소스 식별자를 사용하여 인스턴스 풀에서 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="c9d35-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
```powershell
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="c9d35-119">이 명령은 인스턴스 풀의 리소스 식별자를 사용하여 인스턴스 풀에 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="c9d35-120">예제 5: 인스턴스 풀에서 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="c9d35-120">Example 5: Create a new instance in an instance pool</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 32 -VCore 2 -ComputeGeneration Gen5 -Edition GeneralPurpose -InstancePoolName instancePool0
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
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 32
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="c9d35-121">이 명령은 name instancePool0을 사용하여 인스턴스 풀에 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

### <span data-ttu-id="c9d35-122">예제 6: 유지 관리 구성을 사용하여 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="c9d35-122">Example 6: Create a new instance with maintenance configuration</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourcegroup01 -Location "westus" -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -ComputeGeneration Gen5 -Edition GeneralPurpose -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2"
Location                   : westus
Id                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName          : resourcegroup01
ManagedInstanceName        : managedInstance1
Tags                       :
Identity                   :
Sku                        : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName   : managedInstance1.wusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin         : adminLogin1
AdministratorPassword      :
SubnetId                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType                : LicenseIncluded
VCores                     : 8
StorageSizeInGB            : 256
Collation                  : SQL_Latin1_General_CP1_CI_AS
PublicDataEndpointEnabled  : False
ProxyOverride              :
TimezoneId                 : UTC
DnsZonePartner             :
DnsZone                    : ad35cna0mw
InstancePoolName           :
MinimalTlsVersion          :
BackupStorageRedundancy    : Geo
MaintenanceConfigurationId : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2
```

<span data-ttu-id="c9d35-123">이 명령은 유지 관리 구성이 있는 새 인스턴스를 MI_2</span><span class="sxs-lookup"><span data-stu-id="c9d35-123">This command creates a new instance with maintenance configuration MI_2</span></span>

## <span data-ttu-id="c9d35-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c9d35-124">PARAMETERS</span></span>

### <span data-ttu-id="c9d35-125">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="c9d35-125">-AdministratorCredential</span></span>
<span data-ttu-id="c9d35-126">인스턴스의 SQL 인증 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-126">The SQL authentication credential of the instance.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9d35-127">-AsJob</span></span>
<span data-ttu-id="c9d35-128">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c9d35-128">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c9d35-129">-AssignIdentity</span></span>
<span data-ttu-id="c9d35-130">Azure KeyVault와 같은 주요 관리 서비스와 함께 사용할 이 Managed 인스턴스에 대한 Azure Active Directory ID를 생성하고 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-130">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-131">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="c9d35-131">-BackupStorageRedundancy</span></span>
<span data-ttu-id="c9d35-132">Sql Azure Managed Instance에 대한 백업을 저장하는 데 사용되는 Backup 저장소 중복성입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-132">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="c9d35-133">옵션은 로컬, 영역 및 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-133">Options are: Local, Zone and Geo</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-134">-Collation</span><span class="sxs-lookup"><span data-stu-id="c9d35-134">-Collation</span></span>
<span data-ttu-id="c9d35-135">사용할 Azure SQL Managed Instance의 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-135">The collation of the Azure SQL Managed Instance to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-136">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="c9d35-136">-ComputeGeneration</span></span>
<span data-ttu-id="c9d35-137">인스턴스에 대한 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-137">The compute generation for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d35-138">-DefaultProfile</span></span>
<span data-ttu-id="c9d35-139">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9d35-140">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="c9d35-140">-DnsZonePartner</span></span>
<span data-ttu-id="c9d35-141">Managed Instance 만들기에서 DnsZone 속성을 상속하는 파트너 Managed Server의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c9d35-141">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-142">-Edition</span><span class="sxs-lookup"><span data-stu-id="c9d35-142">-Edition</span></span>
<span data-ttu-id="c9d35-143">인스턴스에 대한 에디션입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-143">The edition for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-144">-Force</span><span class="sxs-lookup"><span data-stu-id="c9d35-144">-Force</span></span>
<span data-ttu-id="c9d35-145">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="c9d35-145">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-146">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="c9d35-146">-InstancePool</span></span>
<span data-ttu-id="c9d35-147">인스턴스 풀 부모 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-147">The instance pool parent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: NewByInstancePoolParentObjectParameterSet
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-148">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="c9d35-148">-InstancePoolName</span></span>
<span data-ttu-id="c9d35-149">이 인스턴스를 에 두는 인스턴스 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-149">The instance pool to place this instance in.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-150">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="c9d35-150">-InstancePoolResourceId</span></span>
<span data-ttu-id="c9d35-151">인스턴스 풀 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-151">The instance pool resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByInstancePoolResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-152">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c9d35-152">-LicenseType</span></span>
<span data-ttu-id="c9d35-153">사용할 라이선스 유형을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-153">Determines which License Type to use.</span></span> <span data-ttu-id="c9d35-154">가능한 값은:</span><span class="sxs-lookup"><span data-stu-id="c9d35-154">Possible values are:</span></span>
- <span data-ttu-id="c9d35-155">BasePrice - 기존 라이선스 소유자에 대한 AHB(Azure Hybrid Benefit) 할인된 가격 SQL Server 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-155">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="c9d35-156">Managed Instance 서비스 가격은 기존 라이선스 소유자에 SQL Server 할인됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-156">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="c9d35-157">LicenseIncluded - 기존 라이선스 소유자에 대한 AHB(Azure Hybrid Benefit) SQL Server 가격 책정은 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-157">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="c9d35-158">Managed Instance 서비스 가격에는 새 라이선스 SQL Server 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-158">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-159">-Location</span><span class="sxs-lookup"><span data-stu-id="c9d35-159">-Location</span></span>
<span data-ttu-id="c9d35-160">인스턴스를 만들 위치</span><span class="sxs-lookup"><span data-stu-id="c9d35-160">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-161">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c9d35-161">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="c9d35-162">Sql Azure Managed Instance에 대한 유지 관리 구성 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-162">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-163">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c9d35-163">-MinimalTlsVersion</span></span>
<span data-ttu-id="c9d35-164">Managed Instance에 적용할 최소 TLS 버전</span><span class="sxs-lookup"><span data-stu-id="c9d35-164">The minimal TLS version to enforce for Managed instance</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-165">-Name</span><span class="sxs-lookup"><span data-stu-id="c9d35-165">-Name</span></span>
<span data-ttu-id="c9d35-166">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-166">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-167">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="c9d35-167">-ProxyOverride</span></span>
<span data-ttu-id="c9d35-168">인스턴스에 연결하는 데 사용되는 연결 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-168">The connection type used for connecting to the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-169">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="c9d35-169">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="c9d35-170">인스턴스에 대해 공용 데이터 엔드포인트를 사용하도록 설정하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-170">Whether or not the public data endpoint is enabled for the instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9d35-171">-ResourceGroupName</span></span>
<span data-ttu-id="c9d35-172">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-172">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-173">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c9d35-173">-SkuName</span></span>
<span data-ttu-id="c9d35-174">인스턴스의 SKU 이름(예: 'GP_Gen4', 'BC_Gen4').</span><span class="sxs-lookup"><span data-stu-id="c9d35-174">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: System.String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-175">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="c9d35-175">-StorageSizeInGB</span></span>
<span data-ttu-id="c9d35-176">인스턴스와 연결할 저장소 크기 결정</span><span class="sxs-lookup"><span data-stu-id="c9d35-176">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-177">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c9d35-177">-SubnetId</span></span>
<span data-ttu-id="c9d35-178">인스턴스 만들기에 사용할 서브넷 ID</span><span class="sxs-lookup"><span data-stu-id="c9d35-178">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="c9d35-179">-Tag</span></span>
<span data-ttu-id="c9d35-180">인스턴스와 연결되는 태그</span><span class="sxs-lookup"><span data-stu-id="c9d35-180">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-181">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="c9d35-181">-TimezoneId</span></span>
<span data-ttu-id="c9d35-182">설정할 인스턴스의 표준 시간대 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-182">The time zone id for the instance to set.</span></span> <span data-ttu-id="c9d35-183">표준 시간대 ID 목록은 sys.time_zone_info(Transact-SQL) 보기를 통해 노출됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-183">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="c9d35-184">-VCore</span></span>
<span data-ttu-id="c9d35-185">인스턴스와 연결할 VCore의 수를 결정</span><span class="sxs-lookup"><span data-stu-id="c9d35-185">Determines how much VCore to associate with instance</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-186">-확인</span><span class="sxs-lookup"><span data-stu-id="c9d35-186">-Confirm</span></span>
<span data-ttu-id="c9d35-187">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-187">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9d35-188">-WhatIf</span></span>
<span data-ttu-id="c9d35-189">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9d35-190">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-190">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d35-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d35-191">CommonParameters</span></span>
<span data-ttu-id="c9d35-192">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d35-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d35-193">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9d35-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d35-194">입력</span><span class="sxs-lookup"><span data-stu-id="c9d35-194">INPUTS</span></span>

### <span data-ttu-id="c9d35-195">없음</span><span class="sxs-lookup"><span data-stu-id="c9d35-195">None</span></span>

## <span data-ttu-id="c9d35-196">출력</span><span class="sxs-lookup"><span data-stu-id="c9d35-196">OUTPUTS</span></span>

### <span data-ttu-id="c9d35-197">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="c9d35-197">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="c9d35-198">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c9d35-198">NOTES</span></span>

## <span data-ttu-id="c9d35-199">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9d35-199">RELATED LINKS</span></span>
