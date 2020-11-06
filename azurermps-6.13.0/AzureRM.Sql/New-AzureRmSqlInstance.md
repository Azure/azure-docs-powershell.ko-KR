---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
ms.openlocfilehash: 025a9acc53405aeb1e211473b5f8f13066791714
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536519"
---
# <span data-ttu-id="fa38b-101">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fa38b-101">New-AzureRmSqlInstance</span></span>

## <span data-ttu-id="fa38b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa38b-102">SYNOPSIS</span></span>
<span data-ttu-id="fa38b-103">Azure SQL 데이터베이스 관리 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-103">Creates an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa38b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fa38b-104">SYNTAX</span></span>

### <span data-ttu-id="fa38b-105">NewByEditionAndComputeGenerationParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fa38b-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa38b-106">Newbya Unameparameterset매개 변수</span><span class="sxs-lookup"><span data-stu-id="fa38b-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa38b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fa38b-107">DESCRIPTION</span></span>
<span data-ttu-id="fa38b-108">**AzureRmSqlInstance** Cmdlet은 Azure SQL Database 관리 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-108">The **New-AzureRmSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="fa38b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fa38b-109">EXAMPLES</span></span>

### <span data-ttu-id="fa38b-110">예제 1: 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="fa38b-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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

<span data-ttu-id="fa38b-111">이 명령은 Edition 및 지 각 생성 매개 변수를 사용 하 여 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="fa38b-112">예제 2: 새 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="fa38b-112">Example 2: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
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

<span data-ttu-id="fa38b-113">이 명령은 Edition 및 지 각 생성 매개 변수를 사용 하 여 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="fa38b-114">변수</span><span class="sxs-lookup"><span data-stu-id="fa38b-114">PARAMETERS</span></span>

### <span data-ttu-id="fa38b-115">-관리자 자격 증명</span><span class="sxs-lookup"><span data-stu-id="fa38b-115">-AdministratorCredential</span></span>
<span data-ttu-id="fa38b-116">인스턴스의 SQL 인증 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-116">The SQL authentication credential of the instance.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa38b-117">-AsJob</span></span>
<span data-ttu-id="fa38b-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fa38b-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-119">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="fa38b-119">-AssignIdentity</span></span>
<span data-ttu-id="fa38b-120">Azure KeyVault 같은 키 관리 서비스에 사용할이 관리 되는 인스턴스에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-121">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="fa38b-121">-ComputeGeneration</span></span>
<span data-ttu-id="fa38b-122">인스턴스에 대 한 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-122">The compute generation for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa38b-123">-DefaultProfile</span></span>
<span data-ttu-id="fa38b-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-125">-에디션</span><span class="sxs-lookup"><span data-stu-id="fa38b-125">-Edition</span></span>
<span data-ttu-id="fa38b-126">인스턴스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-126">The edition for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-127">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fa38b-127">-LicenseType</span></span>
<span data-ttu-id="fa38b-128">사용할 인스턴스의 라이선스 유형을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-128">Determines which License Type of instance to use</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-129">-위치</span><span class="sxs-lookup"><span data-stu-id="fa38b-129">-Location</span></span>
<span data-ttu-id="fa38b-130">인스턴스를 만들 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-130">The location in which to create the instance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-131">-이름</span><span class="sxs-lookup"><span data-stu-id="fa38b-131">-Name</span></span>
<span data-ttu-id="fa38b-132">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-132">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa38b-133">-ResourceGroupName</span></span>
<span data-ttu-id="fa38b-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-134">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-135">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="fa38b-135">-SkuName</span></span>
<span data-ttu-id="fa38b-136">인스턴스에 대 한 SKU 이름 (예: ' GP_Gen4 ', ' BC_Gen4 ')입니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-136">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-137">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="fa38b-137">-StorageSizeInGB</span></span>
<span data-ttu-id="fa38b-138">인스턴스와 연결할 저장소 크기의 양을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-138">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="fa38b-139">-SubnetId</span></span>
<span data-ttu-id="fa38b-140">인스턴스 만들기에 사용할 서브넷 Id</span><span class="sxs-lookup"><span data-stu-id="fa38b-140">The Subnet Id to use for instance creation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-141">태그</span><span class="sxs-lookup"><span data-stu-id="fa38b-141">-Tag</span></span>
<span data-ttu-id="fa38b-142">인스턴스와 연결할 태그</span><span class="sxs-lookup"><span data-stu-id="fa38b-142">The tags to associate with the instance</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-143">-VCore</span><span class="sxs-lookup"><span data-stu-id="fa38b-143">-VCore</span></span>
<span data-ttu-id="fa38b-144">인스턴스와 연결할 VCore의 양을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-144">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-145">-확인</span><span class="sxs-lookup"><span data-stu-id="fa38b-145">-Confirm</span></span>
<span data-ttu-id="fa38b-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa38b-147">-WhatIf</span></span>
<span data-ttu-id="fa38b-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa38b-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa38b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa38b-150">CommonParameters</span></span>
<span data-ttu-id="fa38b-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa38b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa38b-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa38b-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa38b-153">입력</span><span class="sxs-lookup"><span data-stu-id="fa38b-153">INPUTS</span></span>

### <span data-ttu-id="fa38b-154">않아야</span><span class="sxs-lookup"><span data-stu-id="fa38b-154">None</span></span>

## <span data-ttu-id="fa38b-155">출력</span><span class="sxs-lookup"><span data-stu-id="fa38b-155">OUTPUTS</span></span>

### <span data-ttu-id="fa38b-156">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="fa38b-156">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="fa38b-157">상속자</span><span class="sxs-lookup"><span data-stu-id="fa38b-157">NOTES</span></span>

## <span data-ttu-id="fa38b-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa38b-158">RELATED LINKS</span></span>
