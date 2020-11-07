---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: bfa1785004e13400395bd6a6fc93bdec29a69809
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698891"
---
# <span data-ttu-id="62a68-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="62a68-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="62a68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62a68-102">SYNOPSIS</span></span>
<span data-ttu-id="62a68-103">Azure SQL 데이터베이스 관리 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="62a68-104">구문과</span><span class="sxs-lookup"><span data-stu-id="62a68-104">SYNTAX</span></span>

### <span data-ttu-id="62a68-105">NewByEditionAndComputeGenerationParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="62a68-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62a68-106">Newbya Unameparameterset매개 변수</span><span class="sxs-lookup"><span data-stu-id="62a68-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62a68-107">설명은</span><span class="sxs-lookup"><span data-stu-id="62a68-107">DESCRIPTION</span></span>
<span data-ttu-id="62a68-108">**AzSqlInstance** Cmdlet은 Azure SQL Database 관리 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-108">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="62a68-109">예제의</span><span class="sxs-lookup"><span data-stu-id="62a68-109">EXAMPLES</span></span>

### <span data-ttu-id="62a68-110">예제 1: 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="62a68-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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
```

<span data-ttu-id="62a68-111">이 명령은 Edition 및 지 각 생성 매개 변수를 사용 하 여 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="62a68-112">예제 2: 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="62a68-112">Example 2: Create a new instance</span></span>
```
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
```

<span data-ttu-id="62a68-113">이 명령은 Edition 및 지 각 생성 매개 변수를 사용 하 여 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="62a68-114">변수</span><span class="sxs-lookup"><span data-stu-id="62a68-114">PARAMETERS</span></span>

### <span data-ttu-id="62a68-115">-관리자 자격 증명</span><span class="sxs-lookup"><span data-stu-id="62a68-115">-AdministratorCredential</span></span>
<span data-ttu-id="62a68-116">인스턴스의 SQL 인증 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-116">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="62a68-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62a68-117">-AsJob</span></span>
<span data-ttu-id="62a68-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="62a68-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62a68-119">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="62a68-119">-AssignIdentity</span></span>
<span data-ttu-id="62a68-120">Azure KeyVault 같은 키 관리 서비스에 사용할이 관리 되는 인스턴스에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="62a68-121">-데이터 정렬</span><span class="sxs-lookup"><span data-stu-id="62a68-121">-Collation</span></span>
<span data-ttu-id="62a68-122">사용할 Azure SQL 관리 되는 인스턴스의 데이터 정렬입니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-122">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="62a68-123">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="62a68-123">-ComputeGeneration</span></span>
<span data-ttu-id="62a68-124">인스턴스에 대 한 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="62a68-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a68-125">-DefaultProfile</span></span>
<span data-ttu-id="62a68-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62a68-127">-에디션</span><span class="sxs-lookup"><span data-stu-id="62a68-127">-Edition</span></span>
<span data-ttu-id="62a68-128">인스턴스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-128">The edition for the instance.</span></span>

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

### <span data-ttu-id="62a68-129">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="62a68-129">-LicenseType</span></span>
<span data-ttu-id="62a68-130">사용할 라이선스 종류를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-130">Determines which License Type to use.</span></span> <span data-ttu-id="62a68-131">사용할 수 있는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-131">Possible values are:</span></span>
- <span data-ttu-id="62a68-132">BasePrice-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-132">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="62a68-133">관리 되는 인스턴스 서비스 가격은 기존 SQL Server 라이선스 소유자에 게 할인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-133">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="62a68-134">LicenseIncluded-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-134">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="62a68-135">관리 되는 인스턴스 서비스 가격에는 새로운 SQL Server 라이선스 비용이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-135">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a68-136">-위치</span><span class="sxs-lookup"><span data-stu-id="62a68-136">-Location</span></span>
<span data-ttu-id="62a68-137">인스턴스를 만들 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-137">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a68-138">-이름</span><span class="sxs-lookup"><span data-stu-id="62a68-138">-Name</span></span>
<span data-ttu-id="62a68-139">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-139">Instance name.</span></span>

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

### <span data-ttu-id="62a68-140">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="62a68-140">-ProxyOverride</span></span>
<span data-ttu-id="62a68-141">인스턴스에 연결 하는 데 사용 되는 연결 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-141">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="62a68-142">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="62a68-142">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="62a68-143">인스턴스에 대 한 공용 데이터 끝점을 사용할 수 있는지 여부</span><span class="sxs-lookup"><span data-stu-id="62a68-143">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="62a68-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62a68-144">-ResourceGroupName</span></span>
<span data-ttu-id="62a68-145">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a68-146">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="62a68-146">-SkuName</span></span>
<span data-ttu-id="62a68-147">인스턴스에 대 한 SKU 이름 (예: ' GP_Gen4 ', ' BC_Gen4 ')입니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-147">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="62a68-148">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="62a68-148">-StorageSizeInGB</span></span>
<span data-ttu-id="62a68-149">인스턴스와 연결할 저장소 크기의 양을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-149">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="62a68-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="62a68-150">-SubnetId</span></span>
<span data-ttu-id="62a68-151">인스턴스 만들기에 사용할 서브넷 Id</span><span class="sxs-lookup"><span data-stu-id="62a68-151">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a68-152">태그</span><span class="sxs-lookup"><span data-stu-id="62a68-152">-Tag</span></span>
<span data-ttu-id="62a68-153">인스턴스와 연결할 태그</span><span class="sxs-lookup"><span data-stu-id="62a68-153">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="62a68-154">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="62a68-154">-TimezoneId</span></span>
<span data-ttu-id="62a68-155">설정할 인스턴스의 표준 시간대 id입니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-155">The time zone id for the instance to set.</span></span> <span data-ttu-id="62a68-156">표준 시간대 id 목록은 sys.time_zone_info (Transact-sql) 보기를 통해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-156">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="62a68-157">-VCore</span><span class="sxs-lookup"><span data-stu-id="62a68-157">-VCore</span></span>
<span data-ttu-id="62a68-158">인스턴스와 연결할 VCore의 양을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-158">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="62a68-159">-확인</span><span class="sxs-lookup"><span data-stu-id="62a68-159">-Confirm</span></span>
<span data-ttu-id="62a68-160">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62a68-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62a68-161">-WhatIf</span></span>
<span data-ttu-id="62a68-162">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62a68-163">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62a68-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a68-164">CommonParameters</span></span>
<span data-ttu-id="62a68-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62a68-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a68-166">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="62a68-166">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a68-167">입력</span><span class="sxs-lookup"><span data-stu-id="62a68-167">INPUTS</span></span>

### <span data-ttu-id="62a68-168">않아야</span><span class="sxs-lookup"><span data-stu-id="62a68-168">None</span></span>

## <span data-ttu-id="62a68-169">출력</span><span class="sxs-lookup"><span data-stu-id="62a68-169">OUTPUTS</span></span>

### <span data-ttu-id="62a68-170">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="62a68-170">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="62a68-171">상속자</span><span class="sxs-lookup"><span data-stu-id="62a68-171">NOTES</span></span>

## <span data-ttu-id="62a68-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62a68-172">RELATED LINKS</span></span>
