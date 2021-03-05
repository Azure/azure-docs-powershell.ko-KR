---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: a6dd059b7fdab3c2670e3b8902def148d88124d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015867"
---
# <span data-ttu-id="3e422-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3e422-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="3e422-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e422-102">SYNOPSIS</span></span>
<span data-ttu-id="3e422-103">Azure SQL Managed Instance에 대한 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="3e422-104">구문</span><span class="sxs-lookup"><span data-stu-id="3e422-104">SYNTAX</span></span>

### <span data-ttu-id="3e422-105">SetInstanceFromInputParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="3e422-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e422-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="3e422-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e422-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="3e422-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e422-108">설명</span><span class="sxs-lookup"><span data-stu-id="3e422-108">DESCRIPTION</span></span>
<span data-ttu-id="3e422-109">**Set-AzSqlInstance** cmdlet은 Azure SQL 데이터베이스 Managed 인스턴스의 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="3e422-110">예제</span><span class="sxs-lookup"><span data-stu-id="3e422-110">EXAMPLES</span></span>

### <span data-ttu-id="3e422-111">예제 1: -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore 및 -Edition에 대한 새 값을 사용하여 기존 인스턴스 설정</span><span class="sxs-lookup"><span data-stu-id="3e422-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition BusinessCritical
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
InstancePoolName         :
```

### <span data-ttu-id="3e422-112">예제 2: -ComputeGeneration에 대한 새 값을 사용하여 기존 인스턴스 하드웨어 생성 변경</span><span class="sxs-lookup"><span data-stu-id="3e422-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -ComputeGeneration Gen5
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
InstancePoolName         :
```

<span data-ttu-id="3e422-113">이 명령은 -AdministratorPassword, -LicenseType, -StorageSizeInGB 및 -VCore에 대한 새 값을 사용하여 기존 인스턴스를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="3e422-114">예제 3: 인스턴스 풀 내의 인스턴스에 대해 -AdministratorPassword, -LicenseType, -StorageSizeInGB 및 -VCore에 대한 새 값을 사용하여 기존 인스턴스 설정</span><span class="sxs-lookup"><span data-stu-id="3e422-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolName instancePool0
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
StorageSizeInGB          : 1024
InstancePoolName         : instancePool0
```

<span data-ttu-id="3e422-115">이 명령은 인스턴스 풀 내의 인스턴스에 대해 -AdministratorPassword, -LicenseType, -StorageSizeInGB 및 -VCore에 대한 새 값을 사용하여 기존 인스턴스를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

### <span data-ttu-id="3e422-116">예제 4: 기존 인스턴스에 대한 유지 관리 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="3e422-116">Example 4: Update maintenance configuration for existing instance</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "resourcegroup01" -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2"
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

<span data-ttu-id="3e422-117">이 명령은 유지 관리 구성을 사용하여 기존 인스턴스를 MI_2</span><span class="sxs-lookup"><span data-stu-id="3e422-117">This command updates existing instance with maintenance configuration MI_2</span></span>

### <span data-ttu-id="3e422-118">예제 5: 기존 인스턴스에서 유지 관리 구성 제거</span><span class="sxs-lookup"><span data-stu-id="3e422-118">Example 5: Remove maintenance configuration from existing instance</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managediInstance1" -ResourceGroupName "Resourcegroup01" -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_Default"
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
MaintenanceConfigurationId : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_Default
```

<span data-ttu-id="3e422-119">이 명령은 기존 인스턴스에 대한 유지 관리 구성을 기본값으로 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-119">This command resets maintenance configuration to default for existing instance</span></span>

## <span data-ttu-id="3e422-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3e422-120">PARAMETERS</span></span>

### <span data-ttu-id="3e422-121">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="3e422-121">-AdministratorPassword</span></span>
<span data-ttu-id="3e422-122">인스턴스에 SQL 관리자 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-122">The new SQL administrator password for the instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e422-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e422-123">-AsJob</span></span>
<span data-ttu-id="3e422-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3e422-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e422-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3e422-125">-AssignIdentity</span></span>
<span data-ttu-id="3e422-126">Azure KeyVault와 같은 주요 관리 서비스와 함께 사용할 이 인스턴스에 대한 Azure Active Directory ID를 생성하고 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-126">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="3e422-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="3e422-127">-ComputeGeneration</span></span>
<span data-ttu-id="3e422-128">인스턴스에 대한 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-128">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="3e422-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e422-129">-DefaultProfile</span></span>
<span data-ttu-id="3e422-130">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e422-131">-Edition</span><span class="sxs-lookup"><span data-stu-id="3e422-131">-Edition</span></span>
<span data-ttu-id="3e422-132">인스턴스에 할당할 에디션입니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-132">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="3e422-133">-Force</span><span class="sxs-lookup"><span data-stu-id="3e422-133">-Force</span></span>
<span data-ttu-id="3e422-134">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="3e422-134">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3e422-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e422-135">-InputObject</span></span>
<span data-ttu-id="3e422-136">제거할 AzureSqlManagedInstanceModel 개체</span><span class="sxs-lookup"><span data-stu-id="3e422-136">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e422-137">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="3e422-137">-InstancePoolName</span></span>
<span data-ttu-id="3e422-138">인스턴스 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-138">The instance pool name.</span></span>

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

### <span data-ttu-id="3e422-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3e422-139">-LicenseType</span></span>
<span data-ttu-id="3e422-140">사용할 라이선스 유형을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-140">Determines which License Type to use.</span></span> <span data-ttu-id="3e422-141">가능한 값은:</span><span class="sxs-lookup"><span data-stu-id="3e422-141">Possible values are:</span></span>
- <span data-ttu-id="3e422-142">BasePrice - 기존 라이선스 소유자에 대한 AHB(Azure Hybrid Benefit) 할인된 가격 SQL Server 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-142">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="3e422-143">Managed Instance 서비스 가격은 기존 라이선스 소유자에 SQL Server 할인됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-143">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="3e422-144">LicenseIncluded - 기존 라이선스 소유자에 대한 AHB(Azure Hybrid Benefit) SQL Server 가격 책정은 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-144">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="3e422-145">Managed Instance 서비스 가격에는 새 라이선스 SQL Server 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-145">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="3e422-146">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3e422-146">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="3e422-147">Sql Azure Managed Instance에 대한 유지 관리 구성 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-147">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="3e422-148">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="3e422-148">-MinimalTlsVersion</span></span>
<span data-ttu-id="3e422-149">Managed Instance에 적용할 최소 TLS 버전</span><span class="sxs-lookup"><span data-stu-id="3e422-149">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="3e422-150">-Name</span><span class="sxs-lookup"><span data-stu-id="3e422-150">-Name</span></span>
<span data-ttu-id="3e422-151">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-151">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e422-152">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="3e422-152">-ProxyOverride</span></span>
<span data-ttu-id="3e422-153">인스턴스에 연결하는 데 사용되는 연결 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-153">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="3e422-154">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="3e422-154">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="3e422-155">인스턴스에 대해 공용 데이터 엔드포인트를 사용하도록 설정하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-155">Whether or not the public data endpoint is enabled for the instance.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e422-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e422-156">-ResourceGroupName</span></span>
<span data-ttu-id="3e422-157">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e422-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e422-158">-ResourceId</span></span>
<span data-ttu-id="3e422-159">제거할 인스턴스의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="3e422-159">The resource id of instance to remove</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e422-160">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="3e422-160">-StorageSizeInGB</span></span>
<span data-ttu-id="3e422-161">인스턴스와 연결할 저장소 크기 결정</span><span class="sxs-lookup"><span data-stu-id="3e422-161">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e422-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="3e422-162">-Tag</span></span>
<span data-ttu-id="3e422-163">인스턴스와 연결되는 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-163">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="3e422-164">-VCore</span><span class="sxs-lookup"><span data-stu-id="3e422-164">-VCore</span></span>
<span data-ttu-id="3e422-165">인스턴스와 연결할 VCore의 수를 결정</span><span class="sxs-lookup"><span data-stu-id="3e422-165">Determines how much VCore to associate with instance</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e422-166">-확인</span><span class="sxs-lookup"><span data-stu-id="3e422-166">-Confirm</span></span>
<span data-ttu-id="3e422-167">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e422-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e422-168">-WhatIf</span></span>
<span data-ttu-id="3e422-169">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e422-170">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e422-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e422-171">CommonParameters</span></span>
<span data-ttu-id="3e422-172">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3e422-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e422-173">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e422-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e422-174">입력</span><span class="sxs-lookup"><span data-stu-id="3e422-174">INPUTS</span></span>

### <span data-ttu-id="3e422-175">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="3e422-175">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="3e422-176">System.String</span><span class="sxs-lookup"><span data-stu-id="3e422-176">System.String</span></span>

## <span data-ttu-id="3e422-177">출력</span><span class="sxs-lookup"><span data-stu-id="3e422-177">OUTPUTS</span></span>

### <span data-ttu-id="3e422-178">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="3e422-178">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="3e422-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3e422-179">NOTES</span></span>

## <span data-ttu-id="3e422-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e422-180">RELATED LINKS</span></span>
