---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: e17c6b226f7ed4fe17842c93d03828d53c0bb22c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877405"
---
# <span data-ttu-id="fcc19-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fcc19-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="fcc19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcc19-102">SYNOPSIS</span></span>
<span data-ttu-id="fcc19-103">Azure SQL 데이터베이스 관리 인스턴스의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="fcc19-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fcc19-104">SYNTAX</span></span>

### <span data-ttu-id="fcc19-105">SetInstanceFromInputParameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="fcc19-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcc19-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="fcc19-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcc19-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="fcc19-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcc19-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fcc19-108">DESCRIPTION</span></span>
<span data-ttu-id="fcc19-109">**AzSqlInstance** Cmdlet은 Azure SQL Database 관리 인스턴스의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="fcc19-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fcc19-110">EXAMPLES</span></span>

### <span data-ttu-id="fcc19-111">예제 1:-관리자 암호,-LicenseType,-StorageSizeInGB,-VCore 및-Edition에 대 한 새 값을 사용 하 여 기존 인스턴스 설정</span><span class="sxs-lookup"><span data-stu-id="fcc19-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
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

### <span data-ttu-id="fcc19-112">예제 2: 새 값을 사용 하 여 기존 인스턴스 하드웨어 생성 변경</span><span class="sxs-lookup"><span data-stu-id="fcc19-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
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

<span data-ttu-id="fcc19-113">이 명령은-관리자 암호,-LicenseType,-StorageSizeInGB 및-VCore에 대 한 새 값을 사용 하 여 기존 인스턴스를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="fcc19-114">예제 3:-관리자 암호,-LicenseType,-StorageSizeInGB 및-VCore에 대 한 새 값을 사용 하 여 인스턴스 풀 내의 인스턴스에 대 한 기존 인스턴스 설정</span><span class="sxs-lookup"><span data-stu-id="fcc19-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="fcc19-115">이 명령은-관리자 암호,-LicenseType,-StorageSizeInGB 및-VCore에 대 한 새 값을 사용 하 여 인스턴스 풀 내의 인스턴스에 대 한 기존 인스턴스를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="fcc19-116">변수</span><span class="sxs-lookup"><span data-stu-id="fcc19-116">PARAMETERS</span></span>

### <span data-ttu-id="fcc19-117">-관리자 암호</span><span class="sxs-lookup"><span data-stu-id="fcc19-117">-AdministratorPassword</span></span>
<span data-ttu-id="fcc19-118">인스턴스에 대 한 새 SQL 관리자 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-118">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="fcc19-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fcc19-119">-AsJob</span></span>
<span data-ttu-id="fcc19-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fcc19-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fcc19-121">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="fcc19-121">-AssignIdentity</span></span>
<span data-ttu-id="fcc19-122">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 인스턴스에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="fcc19-123">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="fcc19-123">-ComputeGeneration</span></span>
<span data-ttu-id="fcc19-124">인스턴스에 대 한 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="fcc19-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc19-125">-DefaultProfile</span></span>
<span data-ttu-id="fcc19-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcc19-127">-에디션</span><span class="sxs-lookup"><span data-stu-id="fcc19-127">-Edition</span></span>
<span data-ttu-id="fcc19-128">인스턴스에 할당할 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="fcc19-129">-Force</span><span class="sxs-lookup"><span data-stu-id="fcc19-129">-Force</span></span>
<span data-ttu-id="fcc19-130">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="fcc19-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="fcc19-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcc19-131">-InputObject</span></span>
<span data-ttu-id="fcc19-132">제거할 AzureSqlManagedInstanceModel 개체</span><span class="sxs-lookup"><span data-stu-id="fcc19-132">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="fcc19-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="fcc19-133">-InstancePoolName</span></span>
<span data-ttu-id="fcc19-134">인스턴스 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-134">The instance pool name.</span></span>

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

### <span data-ttu-id="fcc19-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fcc19-135">-LicenseType</span></span>
<span data-ttu-id="fcc19-136">사용할 라이선스 종류를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-136">Determines which License Type to use.</span></span> <span data-ttu-id="fcc19-137">사용할 수 있는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-137">Possible values are:</span></span>
- <span data-ttu-id="fcc19-138">BasePrice-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="fcc19-139">관리 되는 인스턴스 서비스 가격은 기존 SQL Server 라이선스 소유자에 게 할인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="fcc19-140">LicenseIncluded-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="fcc19-141">관리 되는 인스턴스 서비스 가격에는 새로운 SQL Server 라이선스 비용이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="fcc19-142">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="fcc19-142">-MinimalTlsVersion</span></span>
<span data-ttu-id="fcc19-143">관리 되는 인스턴스에 적용 되는 최소 TLS 버전</span><span class="sxs-lookup"><span data-stu-id="fcc19-143">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="fcc19-144">-이름</span><span class="sxs-lookup"><span data-stu-id="fcc19-144">-Name</span></span>
<span data-ttu-id="fcc19-145">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-145">Instance name.</span></span>

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

### <span data-ttu-id="fcc19-146">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="fcc19-146">-ProxyOverride</span></span>
<span data-ttu-id="fcc19-147">인스턴스에 연결 하는 데 사용 되는 연결 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-147">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="fcc19-148">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="fcc19-148">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="fcc19-149">인스턴스에 대 한 공용 데이터 끝점을 사용할 수 있는지 여부</span><span class="sxs-lookup"><span data-stu-id="fcc19-149">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="fcc19-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcc19-150">-ResourceGroupName</span></span>
<span data-ttu-id="fcc19-151">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="fcc19-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fcc19-152">-ResourceId</span></span>
<span data-ttu-id="fcc19-153">제거할 인스턴스의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-153">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="fcc19-154">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="fcc19-154">-StorageSizeInGB</span></span>
<span data-ttu-id="fcc19-155">인스턴스와 연결할 저장소 크기의 양을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-155">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="fcc19-156">태그</span><span class="sxs-lookup"><span data-stu-id="fcc19-156">-Tag</span></span>
<span data-ttu-id="fcc19-157">인스턴스와 연결할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-157">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="fcc19-158">-VCore</span><span class="sxs-lookup"><span data-stu-id="fcc19-158">-VCore</span></span>
<span data-ttu-id="fcc19-159">인스턴스와 연결할 VCore의 양을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-159">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="fcc19-160">-확인</span><span class="sxs-lookup"><span data-stu-id="fcc19-160">-Confirm</span></span>
<span data-ttu-id="fcc19-161">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcc19-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcc19-162">-WhatIf</span></span>
<span data-ttu-id="fcc19-163">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcc19-164">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcc19-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc19-165">CommonParameters</span></span>
<span data-ttu-id="fcc19-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc19-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc19-167">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fcc19-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc19-168">입력</span><span class="sxs-lookup"><span data-stu-id="fcc19-168">INPUTS</span></span>

### <span data-ttu-id="fcc19-169">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="fcc19-169">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="fcc19-170">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fcc19-170">System.String</span></span>

## <span data-ttu-id="fcc19-171">출력</span><span class="sxs-lookup"><span data-stu-id="fcc19-171">OUTPUTS</span></span>

### <span data-ttu-id="fcc19-172">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="fcc19-172">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="fcc19-173">상속자</span><span class="sxs-lookup"><span data-stu-id="fcc19-173">NOTES</span></span>

## <span data-ttu-id="fcc19-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcc19-174">RELATED LINKS</span></span>
