---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: 34b12387ef7c967349b6c5f8599d5be361ae43e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043690"
---
# <span data-ttu-id="a67c7-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a67c7-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="a67c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a67c7-102">SYNOPSIS</span></span>
<span data-ttu-id="a67c7-103">Azure SQL 데이터베이스 관리 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="a67c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a67c7-104">SYNTAX</span></span>

### <span data-ttu-id="a67c7-105">NewByEditionAndComputeGenerationParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a67c7-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-AsJob] [-MinimalTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a67c7-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a67c7-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a67c7-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a67c7-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a67c7-108">Newbya Unameparameterset매개 변수</span><span class="sxs-lookup"><span data-stu-id="a67c7-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a67c7-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a67c7-109">DESCRIPTION</span></span>
<span data-ttu-id="a67c7-110">**AzSqlInstance** Cmdlet은 Azure SQL Database 관리 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="a67c7-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a67c7-111">EXAMPLES</span></span>

### <span data-ttu-id="a67c7-112">예제 1: 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="a67c7-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="a67c7-113">이 명령은 새 인스턴스를 만들고,이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="a67c7-114">예제 2: 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="a67c7-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="a67c7-115">이 명령은 Edition 및 지 각 생성 매개 변수를 사용 하 여 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="a67c7-116">예제 3: 인스턴스 풀 개체를 사용 하 여 인스턴스 풀에 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="a67c7-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="a67c7-117">이 명령은 인스턴스 풀 개체를 사용 하 여 인스턴스 풀에 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="a67c7-118">예제 4: instance 풀 리소스 식별자를 사용 하 여 인스턴스 풀에 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="a67c7-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="a67c7-119">이 명령은 인스턴스 풀의 리소스 식별자를 사용 하 여 인스턴스 풀에 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="a67c7-120">예제 5: 인스턴스 풀에서 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="a67c7-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="a67c7-121">이 명령은 name instancePool0를 사용 하 여 인스턴스 풀에 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="a67c7-122">변수</span><span class="sxs-lookup"><span data-stu-id="a67c7-122">PARAMETERS</span></span>

### <span data-ttu-id="a67c7-123">-관리자 자격 증명</span><span class="sxs-lookup"><span data-stu-id="a67c7-123">-AdministratorCredential</span></span>
<span data-ttu-id="a67c7-124">인스턴스의 SQL 인증 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="a67c7-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a67c7-125">-AsJob</span></span>
<span data-ttu-id="a67c7-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a67c7-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a67c7-127">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="a67c7-127">-AssignIdentity</span></span>
<span data-ttu-id="a67c7-128">Azure KeyVault 같은 키 관리 서비스에 사용할이 관리 되는 인스턴스에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="a67c7-129">-데이터 정렬</span><span class="sxs-lookup"><span data-stu-id="a67c7-129">-Collation</span></span>
<span data-ttu-id="a67c7-130">사용할 Azure SQL 관리 되는 인스턴스의 데이터 정렬입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-130">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="a67c7-131">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="a67c7-131">-ComputeGeneration</span></span>
<span data-ttu-id="a67c7-132">인스턴스에 대 한 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-132">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="a67c7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a67c7-133">-DefaultProfile</span></span>
<span data-ttu-id="a67c7-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a67c7-135">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="a67c7-135">-DnsZonePartner</span></span>
<span data-ttu-id="a67c7-136">관리 되는 인스턴스 만들기에 대해 DnsZone 속성을 상속 받을 파트너 관리 서버의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="a67c7-136">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="a67c7-137">-에디션</span><span class="sxs-lookup"><span data-stu-id="a67c7-137">-Edition</span></span>
<span data-ttu-id="a67c7-138">인스턴스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-138">The edition for the instance.</span></span>

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

### <span data-ttu-id="a67c7-139">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="a67c7-139">-InstancePool</span></span>
<span data-ttu-id="a67c7-140">인스턴스 풀 부모 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-140">The instance pool parent object.</span></span>

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

### <span data-ttu-id="a67c7-141">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a67c7-141">-MinimalTlsVersion</span></span>
<span data-ttu-id="a67c7-142">관리 되는 인스턴스에 적용 되는 최소 TLS 버전</span><span class="sxs-lookup"><span data-stu-id="a67c7-142">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="a67c7-143">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="a67c7-143">-InstancePoolName</span></span>
<span data-ttu-id="a67c7-144">이 인스턴스를 배치할 인스턴스 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-144">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="a67c7-145">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="a67c7-145">-InstancePoolResourceId</span></span>
<span data-ttu-id="a67c7-146">인스턴스 풀 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-146">The instance pool resource id.</span></span>

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

### <span data-ttu-id="a67c7-147">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a67c7-147">-LicenseType</span></span>
<span data-ttu-id="a67c7-148">사용할 라이선스 종류를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-148">Determines which License Type to use.</span></span> <span data-ttu-id="a67c7-149">사용할 수 있는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-149">Possible values are:</span></span>
- <span data-ttu-id="a67c7-150">BasePrice-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-150">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="a67c7-151">관리 되는 인스턴스 서비스 가격은 기존 SQL Server 라이선스 소유자에 게 할인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-151">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="a67c7-152">LicenseIncluded-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-152">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="a67c7-153">관리 되는 인스턴스 서비스 가격에는 새로운 SQL Server 라이선스 비용이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-153">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="a67c7-154">-위치</span><span class="sxs-lookup"><span data-stu-id="a67c7-154">-Location</span></span>
<span data-ttu-id="a67c7-155">인스턴스를 만들 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-155">The location in which to create the instance</span></span>

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

### <span data-ttu-id="a67c7-156">-이름</span><span class="sxs-lookup"><span data-stu-id="a67c7-156">-Name</span></span>
<span data-ttu-id="a67c7-157">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-157">Instance name.</span></span>

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

### <span data-ttu-id="a67c7-158">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="a67c7-158">-ProxyOverride</span></span>
<span data-ttu-id="a67c7-159">인스턴스에 연결 하는 데 사용 되는 연결 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-159">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="a67c7-160">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="a67c7-160">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="a67c7-161">인스턴스에 대 한 공용 데이터 끝점을 사용할 수 있는지 여부</span><span class="sxs-lookup"><span data-stu-id="a67c7-161">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="a67c7-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a67c7-162">-ResourceGroupName</span></span>
<span data-ttu-id="a67c7-163">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-163">The name of the resource group.</span></span>

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

### <span data-ttu-id="a67c7-164">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="a67c7-164">-SkuName</span></span>
<span data-ttu-id="a67c7-165">인스턴스에 대 한 SKU 이름 (예: ' GP_Gen4 ', ' BC_Gen4 ')입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-165">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="a67c7-166">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="a67c7-166">-StorageSizeInGB</span></span>
<span data-ttu-id="a67c7-167">인스턴스와 연결할 저장소 크기의 양을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-167">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="a67c7-168">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a67c7-168">-SubnetId</span></span>
<span data-ttu-id="a67c7-169">인스턴스 만들기에 사용할 서브넷 Id</span><span class="sxs-lookup"><span data-stu-id="a67c7-169">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="a67c7-170">태그</span><span class="sxs-lookup"><span data-stu-id="a67c7-170">-Tag</span></span>
<span data-ttu-id="a67c7-171">인스턴스와 연결할 태그</span><span class="sxs-lookup"><span data-stu-id="a67c7-171">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="a67c7-172">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="a67c7-172">-TimezoneId</span></span>
<span data-ttu-id="a67c7-173">설정할 인스턴스의 표준 시간대 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-173">The time zone id for the instance to set.</span></span> <span data-ttu-id="a67c7-174">표준 시간대 id 목록은 sys.time_zone_info (Transact-sql) 보기를 통해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-174">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="a67c7-175">-VCore</span><span class="sxs-lookup"><span data-stu-id="a67c7-175">-VCore</span></span>
<span data-ttu-id="a67c7-176">인스턴스와 연결할 VCore의 양을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-176">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="a67c7-177">-확인</span><span class="sxs-lookup"><span data-stu-id="a67c7-177">-Confirm</span></span>
<span data-ttu-id="a67c7-178">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a67c7-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a67c7-179">-WhatIf</span></span>
<span data-ttu-id="a67c7-180">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a67c7-181">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a67c7-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a67c7-182">CommonParameters</span></span>
<span data-ttu-id="a67c7-183">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a67c7-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a67c7-184">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a67c7-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a67c7-185">입력</span><span class="sxs-lookup"><span data-stu-id="a67c7-185">INPUTS</span></span>

### <span data-ttu-id="a67c7-186">않아야</span><span class="sxs-lookup"><span data-stu-id="a67c7-186">None</span></span>

## <span data-ttu-id="a67c7-187">출력</span><span class="sxs-lookup"><span data-stu-id="a67c7-187">OUTPUTS</span></span>

### <span data-ttu-id="a67c7-188">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="a67c7-188">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="a67c7-189">상속자</span><span class="sxs-lookup"><span data-stu-id="a67c7-189">NOTES</span></span>

## <span data-ttu-id="a67c7-190">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a67c7-190">RELATED LINKS</span></span>
