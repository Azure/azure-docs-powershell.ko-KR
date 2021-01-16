---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: ef809acdf8b78eb0d1203a901b3b44028c79733e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336897"
---
# <span data-ttu-id="01f32-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="01f32-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="01f32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01f32-102">SYNOPSIS</span></span>
<span data-ttu-id="01f32-103">Azure SQL Database Managed Instance를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="01f32-104">구문</span><span class="sxs-lookup"><span data-stu-id="01f32-104">SYNTAX</span></span>

### <span data-ttu-id="01f32-105">NewByEditionAndComputeGenerationParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="01f32-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01f32-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01f32-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01f32-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01f32-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01f32-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="01f32-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01f32-109">설명</span><span class="sxs-lookup"><span data-stu-id="01f32-109">DESCRIPTION</span></span>
<span data-ttu-id="01f32-110">**New-AzSqlInstance** cmdlet은 Azure SQL 데이터베이스 관리되는 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="01f32-111">예제</span><span class="sxs-lookup"><span data-stu-id="01f32-111">EXAMPLES</span></span>

### <span data-ttu-id="01f32-112">예제 1: 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="01f32-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="01f32-113">이 명령은 SkuName 매개 변수를 사용하여 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="01f32-114">예제 2: 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="01f32-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="01f32-115">이 명령은 Edition 및 ComputeGeneration 매개 변수를 사용하여 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="01f32-116">예제 3: 인스턴스 풀 개체를 사용하여 인스턴스 풀에 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="01f32-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="01f32-117">이 명령은 인스턴스 풀 개체를 사용하여 인스턴스 풀에 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="01f32-118">예제 4: 인스턴스 풀 리소스 식별자를 사용하여 인스턴스 풀에 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="01f32-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="01f32-119">이 명령은 인스턴스 풀의 리소스 식별자를 사용하여 인스턴스 풀에 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="01f32-120">예제 5: 인스턴스 풀에서 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="01f32-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="01f32-121">이 명령은 이름 instancePool0을 사용하여 인스턴스 풀에 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="01f32-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01f32-122">PARAMETERS</span></span>

### <span data-ttu-id="01f32-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="01f32-123">-AdministratorCredential</span></span>
<span data-ttu-id="01f32-124">인스턴스의 SQL 인증 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="01f32-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01f32-125">-AsJob</span></span>
<span data-ttu-id="01f32-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="01f32-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01f32-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="01f32-127">-AssignIdentity</span></span>
<span data-ttu-id="01f32-128">Azure KeyVault와 같은 키 관리 서비스에서 사용할 이 Managed Instance에 대한 Azure Active Directory ID를 생성하고 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="01f32-129">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="01f32-129">-BackupStorageRedundancy</span></span>
<span data-ttu-id="01f32-130">Sql Azure Managed Instance에 대한 백업을 저장하는 데 사용되는 Backup 저장소 중복성입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-130">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="01f32-131">옵션은 로컬, 영역 및 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-131">Options are: Local, Zone and Geo</span></span>

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

### <span data-ttu-id="01f32-132">-Collation</span><span class="sxs-lookup"><span data-stu-id="01f32-132">-Collation</span></span>
<span data-ttu-id="01f32-133">사용할 Azure SQL Managed Instance의 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-133">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="01f32-134">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="01f32-134">-ComputeGeneration</span></span>
<span data-ttu-id="01f32-135">인스턴스에 대한 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-135">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="01f32-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f32-136">-DefaultProfile</span></span>
<span data-ttu-id="01f32-137">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01f32-138">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="01f32-138">-DnsZonePartner</span></span>
<span data-ttu-id="01f32-139">Managed Instance 생성에서 DnsZone 속성을 상속하는 파트너 Managed Server의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-139">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="01f32-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="01f32-140">-Edition</span></span>
<span data-ttu-id="01f32-141">인스턴스에 대한 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-141">The edition for the instance.</span></span>

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

### <span data-ttu-id="01f32-142">-Force</span><span class="sxs-lookup"><span data-stu-id="01f32-142">-Force</span></span>
<span data-ttu-id="01f32-143">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="01f32-143">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="01f32-144">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="01f32-144">-InstancePool</span></span>
<span data-ttu-id="01f32-145">인스턴스 풀 부모 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-145">The instance pool parent object.</span></span>

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

### <span data-ttu-id="01f32-146">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="01f32-146">-InstancePoolName</span></span>
<span data-ttu-id="01f32-147">이 인스턴스를 두는 인스턴스 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-147">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="01f32-148">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="01f32-148">-InstancePoolResourceId</span></span>
<span data-ttu-id="01f32-149">인스턴스 풀 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-149">The instance pool resource id.</span></span>

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

### <span data-ttu-id="01f32-150">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="01f32-150">-LicenseType</span></span>
<span data-ttu-id="01f32-151">사용할 라이선스 유형을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-151">Determines which License Type to use.</span></span> <span data-ttu-id="01f32-152">가능한 값은</span><span class="sxs-lookup"><span data-stu-id="01f32-152">Possible values are:</span></span>
- <span data-ttu-id="01f32-153">BasePrice - 기존 라이선스 소유자에 대한 AHB(Azure 하이브리드 혜택) SQL Server 가격이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-153">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="01f32-154">Managed Instance 서비스 가격은 기존 라이선스 SQL Server 할인됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-154">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="01f32-155">LicenseIncluded - 기존 라이선스 소유자에 대한 AHB(Azure 하이브리드 혜택) SQL Server 가격은 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-155">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="01f32-156">Managed Instance 서비스 가격에는 새 라이선스 SQL Server 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-156">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="01f32-157">-Location</span><span class="sxs-lookup"><span data-stu-id="01f32-157">-Location</span></span>
<span data-ttu-id="01f32-158">인스턴스를 만들 위치</span><span class="sxs-lookup"><span data-stu-id="01f32-158">The location in which to create the instance</span></span>

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

### <span data-ttu-id="01f32-159">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="01f32-159">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="01f32-160">Sql Azure Managed Instance에 대한 유지 관리 구성 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-160">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="01f32-161">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="01f32-161">-MinimalTlsVersion</span></span>
<span data-ttu-id="01f32-162">Managed Instance에 적용할 최소 TLS 버전</span><span class="sxs-lookup"><span data-stu-id="01f32-162">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="01f32-163">-Name</span><span class="sxs-lookup"><span data-stu-id="01f32-163">-Name</span></span>
<span data-ttu-id="01f32-164">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-164">Instance name.</span></span>

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

### <span data-ttu-id="01f32-165">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="01f32-165">-ProxyOverride</span></span>
<span data-ttu-id="01f32-166">인스턴스에 연결하는 데 사용되는 연결 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-166">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="01f32-167">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="01f32-167">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="01f32-168">인스턴스에 대해 공용 데이터 엔드포인트를 사용하도록 설정되어 있는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-168">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="01f32-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01f32-169">-ResourceGroupName</span></span>
<span data-ttu-id="01f32-170">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-170">The name of the resource group.</span></span>

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

### <span data-ttu-id="01f32-171">-SkuName</span><span class="sxs-lookup"><span data-stu-id="01f32-171">-SkuName</span></span>
<span data-ttu-id="01f32-172">인스턴스의 SKU 이름(예: 'GP_Gen4', 'BC_Gen4').</span><span class="sxs-lookup"><span data-stu-id="01f32-172">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="01f32-173">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="01f32-173">-StorageSizeInGB</span></span>
<span data-ttu-id="01f32-174">인스턴스와 연결해야 하는 저장소 크기 결정</span><span class="sxs-lookup"><span data-stu-id="01f32-174">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="01f32-175">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="01f32-175">-SubnetId</span></span>
<span data-ttu-id="01f32-176">인스턴스 생성에 사용할 서브넷 ID</span><span class="sxs-lookup"><span data-stu-id="01f32-176">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="01f32-177">-Tag</span><span class="sxs-lookup"><span data-stu-id="01f32-177">-Tag</span></span>
<span data-ttu-id="01f32-178">인스턴스와 연결하기 위해 태그</span><span class="sxs-lookup"><span data-stu-id="01f32-178">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="01f32-179">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="01f32-179">-TimezoneId</span></span>
<span data-ttu-id="01f32-180">설정할 인스턴스의 표준 시간대 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-180">The time zone id for the instance to set.</span></span> <span data-ttu-id="01f32-181">표준 시간대 ID 목록은 sys.time_zone_info(Transact-SQL) 보기를 통해 노출됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-181">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="01f32-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="01f32-182">-VCore</span></span>
<span data-ttu-id="01f32-183">인스턴스와 연결해야 하는 VCore의 수 결정</span><span class="sxs-lookup"><span data-stu-id="01f32-183">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="01f32-184">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01f32-184">-Confirm</span></span>
<span data-ttu-id="01f32-185">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01f32-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01f32-186">-WhatIf</span></span>
<span data-ttu-id="01f32-187">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="01f32-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01f32-188">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01f32-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f32-189">CommonParameters</span></span>
<span data-ttu-id="01f32-190">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="01f32-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f32-191">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="01f32-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f32-192">입력</span><span class="sxs-lookup"><span data-stu-id="01f32-192">INPUTS</span></span>

### <span data-ttu-id="01f32-193">없음</span><span class="sxs-lookup"><span data-stu-id="01f32-193">None</span></span>

## <span data-ttu-id="01f32-194">출력</span><span class="sxs-lookup"><span data-stu-id="01f32-194">OUTPUTS</span></span>

### <span data-ttu-id="01f32-195">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="01f32-195">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="01f32-196">참고 사항</span><span class="sxs-lookup"><span data-stu-id="01f32-196">NOTES</span></span>

## <span data-ttu-id="01f32-197">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01f32-197">RELATED LINKS</span></span>
