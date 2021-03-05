---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 818e76c9ea46b2593b3bdd3871f417dbaca044a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977680"
---
# <span data-ttu-id="ecf51-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="ecf51-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="ecf51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecf51-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf51-103">Azure SQL 인스턴스 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="ecf51-104">구문</span><span class="sxs-lookup"><span data-stu-id="ecf51-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecf51-105">설명</span><span class="sxs-lookup"><span data-stu-id="ecf51-105">DESCRIPTION</span></span>
<span data-ttu-id="ecf51-106">**New-AzSqlInstancePool** cmdlet은 Azure SQL 인스턴스 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="ecf51-107">예제</span><span class="sxs-lookup"><span data-stu-id="ecf51-107">EXAMPLES</span></span>

### <span data-ttu-id="ecf51-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ecf51-108">Example 1</span></span>
```powershell
PS C:\> New-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0 -Location canadacentral -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -Edition GeneralPurpose -ComputeGeneration Gen5 -LicenseType LicenseIncluded
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

<span data-ttu-id="ecf51-109">이 명령은 새 Azure SQL 인스턴스 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="ecf51-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ecf51-110">PARAMETERS</span></span>

### <span data-ttu-id="ecf51-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecf51-111">-AsJob</span></span>
<span data-ttu-id="ecf51-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ecf51-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ecf51-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="ecf51-113">-ComputeGeneration</span></span>
<span data-ttu-id="ecf51-114">인스턴스 풀에 대한 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="ecf51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf51-115">-DefaultProfile</span></span>
<span data-ttu-id="ecf51-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecf51-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="ecf51-117">-Edition</span></span>
<span data-ttu-id="ecf51-118">인스턴스 풀에 대한 에디션입니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="ecf51-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ecf51-119">-LicenseType</span></span>
<span data-ttu-id="ecf51-120">사용할 라이선스 유형을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-120">Determines which License Type to use.</span></span>
<span data-ttu-id="ecf51-121">가능한 값은 BasePrice(AHB 할인 포함) 및 LicenseIncluded(AHB 할인 제외)입니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="ecf51-122">-Location</span><span class="sxs-lookup"><span data-stu-id="ecf51-122">-Location</span></span>
<span data-ttu-id="ecf51-123">인스턴스 풀을 만들 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="ecf51-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ecf51-124">-Name</span></span>
<span data-ttu-id="ecf51-125">인스턴스 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-125">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf51-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf51-126">-ResourceGroupName</span></span>
<span data-ttu-id="ecf51-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf51-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ecf51-128">-SubnetId</span></span>
<span data-ttu-id="ecf51-129">인스턴스 풀 만들기에 사용할 서브넷 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="ecf51-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="ecf51-130">-Tag</span></span>
<span data-ttu-id="ecf51-131">인스턴스와 연결되는 태그</span><span class="sxs-lookup"><span data-stu-id="ecf51-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="ecf51-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="ecf51-132">-VCore</span></span>
<span data-ttu-id="ecf51-133">인스턴스와 연결할 VCore의 수를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-133">Determines how much VCore to associate with instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: VCores

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf51-134">-확인</span><span class="sxs-lookup"><span data-stu-id="ecf51-134">-Confirm</span></span>
<span data-ttu-id="ecf51-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecf51-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecf51-136">-WhatIf</span></span>
<span data-ttu-id="ecf51-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecf51-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecf51-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf51-139">CommonParameters</span></span>
<span data-ttu-id="ecf51-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ecf51-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf51-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecf51-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf51-142">입력</span><span class="sxs-lookup"><span data-stu-id="ecf51-142">INPUTS</span></span>

### <span data-ttu-id="ecf51-143">없음</span><span class="sxs-lookup"><span data-stu-id="ecf51-143">None</span></span>

## <span data-ttu-id="ecf51-144">출력</span><span class="sxs-lookup"><span data-stu-id="ecf51-144">OUTPUTS</span></span>

### <span data-ttu-id="ecf51-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="ecf51-145">System.Object</span></span>
## <span data-ttu-id="ecf51-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ecf51-146">NOTES</span></span>

## <span data-ttu-id="ecf51-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecf51-147">RELATED LINKS</span></span>
