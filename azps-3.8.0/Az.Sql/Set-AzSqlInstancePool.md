---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: db7d9165b8aec6a69f31850f7a37eddb2450e53b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878801"
---
# <span data-ttu-id="c2697-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="c2697-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="c2697-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2697-102">SYNOPSIS</span></span>
<span data-ttu-id="c2697-103">Azure SQL 인스턴스 풀에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="c2697-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2697-104">SYNTAX</span></span>

### <span data-ttu-id="c2697-105">DefaultSetInstancePoolParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c2697-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2697-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2697-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2697-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2697-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2697-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c2697-108">DESCRIPTION</span></span>
<span data-ttu-id="c2697-109">**Set-AzSqlInstancePool** Cmdlet은 Azure SQL 인스턴스 풀의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="c2697-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c2697-110">EXAMPLES</span></span>

### <span data-ttu-id="c2697-111">예제 1: 인스턴스 풀 라이선스 형식 설정</span><span class="sxs-lookup"><span data-stu-id="c2697-111">Example 1 : Set an instance pool license type</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0 -LicenseType LicenseIncluded
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="c2697-112">이 명령은 instancePool0 이라는 인스턴스 풀에 대 한 라이선스 유형 및/또는 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="c2697-113">예제 2: 인스턴스 풀 개체를 사용 하 여 인스턴스 풀 라이선스 유형 설정</span><span class="sxs-lookup"><span data-stu-id="c2697-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
PS C:\> Set-AzSqlInstancePool -InputObject $instancePool -LicenseType LicenseIncluded
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="c2697-114">이 명령은 인스턴스 풀 개체를 사용 하 여 인스턴스 풀에 대 한 라이선스 유형 및/또는 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="c2697-115">예제 3: 인스턴스 풀 리소스 id를 사용 하 여 인스턴스 풀 라이선스 유형 설정</span><span class="sxs-lookup"><span data-stu-id="c2697-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0" -LicenseType LicenseIncluded
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="c2697-116">이 명령은 instancePool0 이라는 인스턴스 풀에 대 한 라이선스 유형 및/또는 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="c2697-117">변수</span><span class="sxs-lookup"><span data-stu-id="c2697-117">PARAMETERS</span></span>

### <span data-ttu-id="c2697-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2697-118">-AsJob</span></span>
<span data-ttu-id="c2697-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c2697-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2697-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2697-120">-DefaultProfile</span></span>
<span data-ttu-id="c2697-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2697-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2697-122">-InputObject</span></span>
<span data-ttu-id="c2697-123">인스턴스 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-123">The instance pool input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InputObjectSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2697-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c2697-124">-LicenseType</span></span>
<span data-ttu-id="c2697-125">사용할 라이선스 종류를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-125">Determines which License Type to use.</span></span>
<span data-ttu-id="c2697-126">사용할 수 있는 값은 BasePrice (AHB 할인율 포함)이 고 LicenseIncluded (AHB 할인 없음)입니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="c2697-127">-이름</span><span class="sxs-lookup"><span data-stu-id="c2697-127">-Name</span></span>
<span data-ttu-id="c2697-128">인스턴스 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-128">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2697-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2697-129">-ResourceGroupName</span></span>
<span data-ttu-id="c2697-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2697-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2697-131">-ResourceId</span></span>
<span data-ttu-id="c2697-132">인스턴스 풀 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-132">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2697-133">태그</span><span class="sxs-lookup"><span data-stu-id="c2697-133">-Tag</span></span>
<span data-ttu-id="c2697-134">인스턴스와 연결할 태그</span><span class="sxs-lookup"><span data-stu-id="c2697-134">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="c2697-135">-확인</span><span class="sxs-lookup"><span data-stu-id="c2697-135">-Confirm</span></span>
<span data-ttu-id="c2697-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2697-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2697-137">-WhatIf</span></span>
<span data-ttu-id="c2697-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2697-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2697-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2697-140">CommonParameters</span></span>
<span data-ttu-id="c2697-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2697-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2697-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2697-143">입력</span><span class="sxs-lookup"><span data-stu-id="c2697-143">INPUTS</span></span>

### <span data-ttu-id="c2697-144">Microsoft.Azure.Commands.Sql.Instance_Pools AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="c2697-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="c2697-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c2697-145">System.String</span></span>

## <span data-ttu-id="c2697-146">출력</span><span class="sxs-lookup"><span data-stu-id="c2697-146">OUTPUTS</span></span>

### <span data-ttu-id="c2697-147">System. 개체</span><span class="sxs-lookup"><span data-stu-id="c2697-147">System.Object</span></span>
## <span data-ttu-id="c2697-148">상속자</span><span class="sxs-lookup"><span data-stu-id="c2697-148">NOTES</span></span>

## <span data-ttu-id="c2697-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2697-149">RELATED LINKS</span></span>
