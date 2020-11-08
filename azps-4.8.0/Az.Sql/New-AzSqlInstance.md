---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: bb9ae3ba225c67a98b6c3588e1dc0c63f02170ae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048645"
---
# <span data-ttu-id="12d3f-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="12d3f-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="12d3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="12d3f-103">Azure SQL 데이터베이스 관리 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="12d3f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="12d3f-104">SYNTAX</span></span>

### <span data-ttu-id="12d3f-105">NewByEditionAndComputeGenerationParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="12d3f-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12d3f-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12d3f-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12d3f-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12d3f-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12d3f-108">Newbya Unameparameterset매개 변수</span><span class="sxs-lookup"><span data-stu-id="12d3f-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12d3f-109">설명은</span><span class="sxs-lookup"><span data-stu-id="12d3f-109">DESCRIPTION</span></span>
<span data-ttu-id="12d3f-110">**AzSqlInstance** Cmdlet은 Azure SQL Database 관리 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="12d3f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="12d3f-111">EXAMPLES</span></span>

### <span data-ttu-id="12d3f-112">예제 1: 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="12d3f-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="12d3f-113">이 명령은 새 인스턴스를 만들고,이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="12d3f-114">예제 2: 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="12d3f-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="12d3f-115">이 명령은 Edition 및 지 각 생성 매개 변수를 사용 하 여 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="12d3f-116">예제 3: 인스턴스 풀 개체를 사용 하 여 인스턴스 풀에 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="12d3f-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="12d3f-117">이 명령은 인스턴스 풀 개체를 사용 하 여 인스턴스 풀에 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="12d3f-118">예제 4: instance 풀 리소스 식별자를 사용 하 여 인스턴스 풀에 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="12d3f-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="12d3f-119">이 명령은 인스턴스 풀의 리소스 식별자를 사용 하 여 인스턴스 풀에 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="12d3f-120">예제 5: 인스턴스 풀에서 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="12d3f-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="12d3f-121">이 명령은 name instancePool0를 사용 하 여 인스턴스 풀에 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="12d3f-122">변수</span><span class="sxs-lookup"><span data-stu-id="12d3f-122">PARAMETERS</span></span>

### <span data-ttu-id="12d3f-123">-관리자 자격 증명</span><span class="sxs-lookup"><span data-stu-id="12d3f-123">-AdministratorCredential</span></span>
<span data-ttu-id="12d3f-124">인스턴스의 SQL 인증 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="12d3f-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12d3f-125">-AsJob</span></span>
<span data-ttu-id="12d3f-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="12d3f-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12d3f-127">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="12d3f-127">-AssignIdentity</span></span>
<span data-ttu-id="12d3f-128">Azure KeyVault 같은 키 관리 서비스에 사용할이 관리 되는 인스턴스에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="12d3f-129">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="12d3f-129">-BackupStorageRedundancy</span></span>
<span data-ttu-id="12d3f-130">Sql Azure 관리 인스턴스에 대 한 백업을 저장 하는 데 사용 되는 백업 저장소 중복성.</span><span class="sxs-lookup"><span data-stu-id="12d3f-130">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="12d3f-131">옵션: 지역, Zone 및 Geo</span><span class="sxs-lookup"><span data-stu-id="12d3f-131">Options are: Local, Zone and Geo</span></span>

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

### <span data-ttu-id="12d3f-132">-데이터 정렬</span><span class="sxs-lookup"><span data-stu-id="12d3f-132">-Collation</span></span>
<span data-ttu-id="12d3f-133">사용할 Azure SQL 관리 되는 인스턴스의 데이터 정렬입니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-133">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="12d3f-134">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="12d3f-134">-ComputeGeneration</span></span>
<span data-ttu-id="12d3f-135">인스턴스에 대 한 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-135">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="12d3f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d3f-136">-DefaultProfile</span></span>
<span data-ttu-id="12d3f-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12d3f-138">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="12d3f-138">-DnsZonePartner</span></span>
<span data-ttu-id="12d3f-139">관리 되는 인스턴스 만들기에 대해 DnsZone 속성을 상속 받을 파트너 관리 서버의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="12d3f-139">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="12d3f-140">-에디션</span><span class="sxs-lookup"><span data-stu-id="12d3f-140">-Edition</span></span>
<span data-ttu-id="12d3f-141">인스턴스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-141">The edition for the instance.</span></span>

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

### <span data-ttu-id="12d3f-142">-Force</span><span class="sxs-lookup"><span data-stu-id="12d3f-142">-Force</span></span>
<span data-ttu-id="12d3f-143">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="12d3f-143">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="12d3f-144">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="12d3f-144">-InstancePool</span></span>
<span data-ttu-id="12d3f-145">인스턴스 풀 부모 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-145">The instance pool parent object.</span></span>

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

### <span data-ttu-id="12d3f-146">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="12d3f-146">-InstancePoolName</span></span>
<span data-ttu-id="12d3f-147">이 인스턴스를 배치할 인스턴스 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-147">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="12d3f-148">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="12d3f-148">-InstancePoolResourceId</span></span>
<span data-ttu-id="12d3f-149">인스턴스 풀 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-149">The instance pool resource id.</span></span>

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

### <span data-ttu-id="12d3f-150">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="12d3f-150">-LicenseType</span></span>
<span data-ttu-id="12d3f-151">사용할 라이선스 종류를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-151">Determines which License Type to use.</span></span> <span data-ttu-id="12d3f-152">사용할 수 있는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-152">Possible values are:</span></span>
- <span data-ttu-id="12d3f-153">BasePrice-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-153">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="12d3f-154">관리 되는 인스턴스 서비스 가격은 기존 SQL Server 라이선스 소유자에 게 할인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-154">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="12d3f-155">LicenseIncluded-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-155">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="12d3f-156">관리 되는 인스턴스 서비스 가격에는 새로운 SQL Server 라이선스 비용이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-156">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="12d3f-157">-위치</span><span class="sxs-lookup"><span data-stu-id="12d3f-157">-Location</span></span>
<span data-ttu-id="12d3f-158">인스턴스를 만들 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-158">The location in which to create the instance</span></span>

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

### <span data-ttu-id="12d3f-159">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="12d3f-159">-MinimalTlsVersion</span></span>
<span data-ttu-id="12d3f-160">관리 되는 인스턴스에 적용 되는 최소 TLS 버전</span><span class="sxs-lookup"><span data-stu-id="12d3f-160">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="12d3f-161">-이름</span><span class="sxs-lookup"><span data-stu-id="12d3f-161">-Name</span></span>
<span data-ttu-id="12d3f-162">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-162">Instance name.</span></span>

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

### <span data-ttu-id="12d3f-163">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="12d3f-163">-ProxyOverride</span></span>
<span data-ttu-id="12d3f-164">인스턴스에 연결 하는 데 사용 되는 연결 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-164">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="12d3f-165">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="12d3f-165">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="12d3f-166">인스턴스에 대 한 공용 데이터 끝점을 사용할 수 있는지 여부</span><span class="sxs-lookup"><span data-stu-id="12d3f-166">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="12d3f-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12d3f-167">-ResourceGroupName</span></span>
<span data-ttu-id="12d3f-168">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-168">The name of the resource group.</span></span>

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

### <span data-ttu-id="12d3f-169">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="12d3f-169">-SkuName</span></span>
<span data-ttu-id="12d3f-170">인스턴스에 대 한 SKU 이름 (예: ' GP_Gen4 ', ' BC_Gen4 ')입니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-170">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="12d3f-171">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="12d3f-171">-StorageSizeInGB</span></span>
<span data-ttu-id="12d3f-172">인스턴스와 연결할 저장소 크기의 양을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-172">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="12d3f-173">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="12d3f-173">-SubnetId</span></span>
<span data-ttu-id="12d3f-174">인스턴스 만들기에 사용할 서브넷 Id</span><span class="sxs-lookup"><span data-stu-id="12d3f-174">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="12d3f-175">태그</span><span class="sxs-lookup"><span data-stu-id="12d3f-175">-Tag</span></span>
<span data-ttu-id="12d3f-176">인스턴스와 연결할 태그</span><span class="sxs-lookup"><span data-stu-id="12d3f-176">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="12d3f-177">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="12d3f-177">-TimezoneId</span></span>
<span data-ttu-id="12d3f-178">설정할 인스턴스의 표준 시간대 id입니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-178">The time zone id for the instance to set.</span></span> <span data-ttu-id="12d3f-179">표준 시간대 id 목록은 sys.time_zone_info (Transact-sql) 보기를 통해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-179">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="12d3f-180">-VCore</span><span class="sxs-lookup"><span data-stu-id="12d3f-180">-VCore</span></span>
<span data-ttu-id="12d3f-181">인스턴스와 연결할 VCore의 양을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-181">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="12d3f-182">-확인</span><span class="sxs-lookup"><span data-stu-id="12d3f-182">-Confirm</span></span>
<span data-ttu-id="12d3f-183">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12d3f-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12d3f-184">-WhatIf</span></span>
<span data-ttu-id="12d3f-185">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12d3f-186">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12d3f-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d3f-187">CommonParameters</span></span>
<span data-ttu-id="12d3f-188">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="12d3f-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d3f-189">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="12d3f-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d3f-190">입력</span><span class="sxs-lookup"><span data-stu-id="12d3f-190">INPUTS</span></span>

### <span data-ttu-id="12d3f-191">않아야</span><span class="sxs-lookup"><span data-stu-id="12d3f-191">None</span></span>

## <span data-ttu-id="12d3f-192">출력</span><span class="sxs-lookup"><span data-stu-id="12d3f-192">OUTPUTS</span></span>

### <span data-ttu-id="12d3f-193">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="12d3f-193">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="12d3f-194">상속자</span><span class="sxs-lookup"><span data-stu-id="12d3f-194">NOTES</span></span>

## <span data-ttu-id="12d3f-195">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12d3f-195">RELATED LINKS</span></span>
