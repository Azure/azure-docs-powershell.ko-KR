---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: f16e6f2dcbcf3ebd16926784ca84eef02740df7b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195964"
---
# <span data-ttu-id="16afd-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="16afd-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="16afd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16afd-102">SYNOPSIS</span></span>
<span data-ttu-id="16afd-103">Azure SQL Database Managed Instance에 대한 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="16afd-104">구문</span><span class="sxs-lookup"><span data-stu-id="16afd-104">SYNTAX</span></span>

### <span data-ttu-id="16afd-105">SetInstanceFromInputParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="16afd-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16afd-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="16afd-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16afd-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="16afd-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16afd-108">설명</span><span class="sxs-lookup"><span data-stu-id="16afd-108">DESCRIPTION</span></span>
<span data-ttu-id="16afd-109">**Set-AzSqlInstance** cmdlet은 Azure SQL 데이터베이스 관리되는 인스턴스의 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="16afd-110">예제</span><span class="sxs-lookup"><span data-stu-id="16afd-110">EXAMPLES</span></span>

### <span data-ttu-id="16afd-111">예제 1: -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore 및 -Edition에 대한 새 값을 사용하여 기존 인스턴스 설정</span><span class="sxs-lookup"><span data-stu-id="16afd-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
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

### <span data-ttu-id="16afd-112">예제 2: -ComputeGeneration에 대한 새 값을 사용하여 기존 인스턴스 하드웨어 생성 변경</span><span class="sxs-lookup"><span data-stu-id="16afd-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
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

<span data-ttu-id="16afd-113">이 명령은 -AdministratorPassword, -LicenseType, -StorageSizeInGB 및 -VCore에 대한 새 값을 사용하여 기존 인스턴스를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="16afd-114">예제 3: 인스턴스 풀 내의 인스턴스에 대해 -AdministratorPassword, -LicenseType, -StorageSizeInGB 및 -VCore에 대한 새 값을 사용하여 기존 인스턴스 설정</span><span class="sxs-lookup"><span data-stu-id="16afd-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="16afd-115">이 명령은 인스턴스 풀 내의 인스턴스에 대해 -AdministratorPassword, -LicenseType, -StorageSizeInGB 및 -VCore에 대한 새 값을 사용하여 기존 인스턴스를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="16afd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16afd-116">PARAMETERS</span></span>

### <span data-ttu-id="16afd-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="16afd-117">-AdministratorPassword</span></span>
<span data-ttu-id="16afd-118">새 SQL 대한 관리자 암호를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-118">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="16afd-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16afd-119">-AsJob</span></span>
<span data-ttu-id="16afd-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="16afd-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16afd-121">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="16afd-121">-AssignIdentity</span></span>
<span data-ttu-id="16afd-122">Azure KeyVault와 같은 키 관리 서비스에서 사용할 이 인스턴스에 대한 Azure Active Directory ID를 생성하고 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="16afd-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="16afd-123">-ComputeGeneration</span></span>
<span data-ttu-id="16afd-124">인스턴스에 대한 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="16afd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16afd-125">-DefaultProfile</span></span>
<span data-ttu-id="16afd-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16afd-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="16afd-127">-Edition</span></span>
<span data-ttu-id="16afd-128">인스턴스에 할당할 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="16afd-129">-Force</span><span class="sxs-lookup"><span data-stu-id="16afd-129">-Force</span></span>
<span data-ttu-id="16afd-130">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="16afd-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="16afd-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16afd-131">-InputObject</span></span>
<span data-ttu-id="16afd-132">제거할 AzureSqlManagedInstanceModel 개체</span><span class="sxs-lookup"><span data-stu-id="16afd-132">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="16afd-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="16afd-133">-InstancePoolName</span></span>
<span data-ttu-id="16afd-134">인스턴스 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-134">The instance pool name.</span></span>

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

### <span data-ttu-id="16afd-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="16afd-135">-LicenseType</span></span>
<span data-ttu-id="16afd-136">사용할 라이선스 유형을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-136">Determines which License Type to use.</span></span> <span data-ttu-id="16afd-137">가능한 값은</span><span class="sxs-lookup"><span data-stu-id="16afd-137">Possible values are:</span></span>
- <span data-ttu-id="16afd-138">BasePrice - 기존 라이선스 소유자에 대한 AHB(Azure 하이브리드 혜택) SQL Server 가격이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="16afd-139">Managed Instance 서비스 가격은 기존 라이선스 SQL Server 할인됩니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="16afd-140">LicenseIncluded - 기존 라이선스 소유자에 대한 AHB(Azure 하이브리드 혜택) SQL Server 가격은 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="16afd-141">Managed Instance 서비스 가격에는 새 라이선스 SQL Server 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="16afd-142">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="16afd-142">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="16afd-143">Sql Azure Managed Instance에 대한 유지 관리 구성 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-143">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="16afd-144">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="16afd-144">-MinimalTlsVersion</span></span>
<span data-ttu-id="16afd-145">Managed Instance에 적용할 최소 TLS 버전</span><span class="sxs-lookup"><span data-stu-id="16afd-145">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="16afd-146">-Name</span><span class="sxs-lookup"><span data-stu-id="16afd-146">-Name</span></span>
<span data-ttu-id="16afd-147">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-147">Instance name.</span></span>

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

### <span data-ttu-id="16afd-148">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="16afd-148">-ProxyOverride</span></span>
<span data-ttu-id="16afd-149">인스턴스에 연결하는 데 사용되는 연결 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-149">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="16afd-150">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="16afd-150">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="16afd-151">인스턴스에 대해 공용 데이터 엔드포인트를 사용하도록 설정되어 있는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-151">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="16afd-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16afd-152">-ResourceGroupName</span></span>
<span data-ttu-id="16afd-153">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="16afd-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16afd-154">-ResourceId</span></span>
<span data-ttu-id="16afd-155">제거할 인스턴스의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="16afd-155">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="16afd-156">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="16afd-156">-StorageSizeInGB</span></span>
<span data-ttu-id="16afd-157">인스턴스와 연결해야 하는 저장소 크기 결정</span><span class="sxs-lookup"><span data-stu-id="16afd-157">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="16afd-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="16afd-158">-Tag</span></span>
<span data-ttu-id="16afd-159">인스턴스와 연결되는 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-159">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="16afd-160">-VCore</span><span class="sxs-lookup"><span data-stu-id="16afd-160">-VCore</span></span>
<span data-ttu-id="16afd-161">인스턴스와 연결해야 하는 VCore의 수 결정</span><span class="sxs-lookup"><span data-stu-id="16afd-161">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="16afd-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16afd-162">-Confirm</span></span>
<span data-ttu-id="16afd-163">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16afd-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16afd-164">-WhatIf</span></span>
<span data-ttu-id="16afd-165">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="16afd-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16afd-166">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16afd-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16afd-167">CommonParameters</span></span>
<span data-ttu-id="16afd-168">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16afd-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16afd-169">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="16afd-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16afd-170">입력</span><span class="sxs-lookup"><span data-stu-id="16afd-170">INPUTS</span></span>

### <span data-ttu-id="16afd-171">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="16afd-171">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="16afd-172">System.String</span><span class="sxs-lookup"><span data-stu-id="16afd-172">System.String</span></span>

## <span data-ttu-id="16afd-173">출력</span><span class="sxs-lookup"><span data-stu-id="16afd-173">OUTPUTS</span></span>

### <span data-ttu-id="16afd-174">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="16afd-174">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="16afd-175">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16afd-175">NOTES</span></span>

## <span data-ttu-id="16afd-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16afd-176">RELATED LINKS</span></span>
