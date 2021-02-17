---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 1b4f405e9bf6377855439d1f6d3cad9f0538920f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197697"
---
# <span data-ttu-id="84594-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="84594-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="84594-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84594-102">SYNOPSIS</span></span>
<span data-ttu-id="84594-103">Azure SQL 인스턴스 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="84594-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="84594-104">구문</span><span class="sxs-lookup"><span data-stu-id="84594-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84594-105">설명</span><span class="sxs-lookup"><span data-stu-id="84594-105">DESCRIPTION</span></span>
<span data-ttu-id="84594-106">**New-AzSqlInstancePool** cmdlet은 Azure SQL 인스턴스 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="84594-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="84594-107">예제</span><span class="sxs-lookup"><span data-stu-id="84594-107">EXAMPLES</span></span>

### <span data-ttu-id="84594-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="84594-108">Example 1</span></span>
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

<span data-ttu-id="84594-109">이 명령은 새 Azure SQL 인스턴스 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="84594-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="84594-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84594-110">PARAMETERS</span></span>

### <span data-ttu-id="84594-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84594-111">-AsJob</span></span>
<span data-ttu-id="84594-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="84594-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84594-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="84594-113">-ComputeGeneration</span></span>
<span data-ttu-id="84594-114">인스턴스 풀에 대한 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="84594-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="84594-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84594-115">-DefaultProfile</span></span>
<span data-ttu-id="84594-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84594-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84594-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="84594-117">-Edition</span></span>
<span data-ttu-id="84594-118">인스턴스 풀에 대한 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="84594-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="84594-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="84594-119">-LicenseType</span></span>
<span data-ttu-id="84594-120">사용할 라이선스 유형을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84594-120">Determines which License Type to use.</span></span>
<span data-ttu-id="84594-121">가능한 값은 BasePrice(AHB 할인 포함) 및 LicenseIncluded(AHB 할인 제외)입니다.</span><span class="sxs-lookup"><span data-stu-id="84594-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="84594-122">-Location</span><span class="sxs-lookup"><span data-stu-id="84594-122">-Location</span></span>
<span data-ttu-id="84594-123">인스턴스 풀을 만들 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="84594-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="84594-124">-Name</span><span class="sxs-lookup"><span data-stu-id="84594-124">-Name</span></span>
<span data-ttu-id="84594-125">인스턴스 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84594-125">The name of the instance pool.</span></span>

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

### <span data-ttu-id="84594-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84594-126">-ResourceGroupName</span></span>
<span data-ttu-id="84594-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84594-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="84594-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="84594-128">-SubnetId</span></span>
<span data-ttu-id="84594-129">인스턴스 풀 생성에 사용할 서브넷 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="84594-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="84594-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="84594-130">-Tag</span></span>
<span data-ttu-id="84594-131">인스턴스와 연결하기 위해 태그</span><span class="sxs-lookup"><span data-stu-id="84594-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="84594-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="84594-132">-VCore</span></span>
<span data-ttu-id="84594-133">인스턴스와 연결되는 VCore의 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84594-133">Determines how much VCore to associate with instance.</span></span>

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

### <span data-ttu-id="84594-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84594-134">-Confirm</span></span>
<span data-ttu-id="84594-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="84594-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84594-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84594-136">-WhatIf</span></span>
<span data-ttu-id="84594-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="84594-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84594-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84594-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84594-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84594-139">CommonParameters</span></span>
<span data-ttu-id="84594-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="84594-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84594-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="84594-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84594-142">입력</span><span class="sxs-lookup"><span data-stu-id="84594-142">INPUTS</span></span>

### <span data-ttu-id="84594-143">없음</span><span class="sxs-lookup"><span data-stu-id="84594-143">None</span></span>

## <span data-ttu-id="84594-144">출력</span><span class="sxs-lookup"><span data-stu-id="84594-144">OUTPUTS</span></span>

### <span data-ttu-id="84594-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="84594-145">System.Object</span></span>
## <span data-ttu-id="84594-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="84594-146">NOTES</span></span>

## <span data-ttu-id="84594-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84594-147">RELATED LINKS</span></span>
