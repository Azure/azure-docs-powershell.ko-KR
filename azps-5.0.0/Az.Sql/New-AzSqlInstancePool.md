---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 1b4f405e9bf6377855439d1f6d3cad9f0538920f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216669"
---
# <span data-ttu-id="a15c7-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="a15c7-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="a15c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a15c7-102">SYNOPSIS</span></span>
<span data-ttu-id="a15c7-103">Azure SQL 인스턴스 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="a15c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a15c7-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a15c7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a15c7-105">DESCRIPTION</span></span>
<span data-ttu-id="a15c7-106">**새 AzSqlInstancePool** Cmdlet은 Azure SQL 인스턴스 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="a15c7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a15c7-107">EXAMPLES</span></span>

### <span data-ttu-id="a15c7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a15c7-108">Example 1</span></span>
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

<span data-ttu-id="a15c7-109">이 명령은 새 Azure SQL 인스턴스 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="a15c7-110">변수</span><span class="sxs-lookup"><span data-stu-id="a15c7-110">PARAMETERS</span></span>

### <span data-ttu-id="a15c7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a15c7-111">-AsJob</span></span>
<span data-ttu-id="a15c7-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a15c7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a15c7-113">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="a15c7-113">-ComputeGeneration</span></span>
<span data-ttu-id="a15c7-114">인스턴스 풀에 대 한 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="a15c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a15c7-115">-DefaultProfile</span></span>
<span data-ttu-id="a15c7-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a15c7-117">-에디션</span><span class="sxs-lookup"><span data-stu-id="a15c7-117">-Edition</span></span>
<span data-ttu-id="a15c7-118">인스턴스 풀에 대 한 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="a15c7-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a15c7-119">-LicenseType</span></span>
<span data-ttu-id="a15c7-120">사용할 라이선스 종류를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-120">Determines which License Type to use.</span></span>
<span data-ttu-id="a15c7-121">사용할 수 있는 값은 BasePrice (AHB 할인율 포함)이 고 LicenseIncluded (AHB 할인 없음)입니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="a15c7-122">-위치</span><span class="sxs-lookup"><span data-stu-id="a15c7-122">-Location</span></span>
<span data-ttu-id="a15c7-123">인스턴스 풀을 만들 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="a15c7-124">-이름</span><span class="sxs-lookup"><span data-stu-id="a15c7-124">-Name</span></span>
<span data-ttu-id="a15c7-125">인스턴스 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-125">The name of the instance pool.</span></span>

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

### <span data-ttu-id="a15c7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a15c7-126">-ResourceGroupName</span></span>
<span data-ttu-id="a15c7-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="a15c7-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a15c7-128">-SubnetId</span></span>
<span data-ttu-id="a15c7-129">인스턴스 풀 만들기에 사용할 서브넷 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="a15c7-130">태그</span><span class="sxs-lookup"><span data-stu-id="a15c7-130">-Tag</span></span>
<span data-ttu-id="a15c7-131">인스턴스와 연결할 태그</span><span class="sxs-lookup"><span data-stu-id="a15c7-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="a15c7-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="a15c7-132">-VCore</span></span>
<span data-ttu-id="a15c7-133">인스턴스와 연결할 VCore의 양을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-133">Determines how much VCore to associate with instance.</span></span>

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

### <span data-ttu-id="a15c7-134">-확인</span><span class="sxs-lookup"><span data-stu-id="a15c7-134">-Confirm</span></span>
<span data-ttu-id="a15c7-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a15c7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a15c7-136">-WhatIf</span></span>
<span data-ttu-id="a15c7-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a15c7-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a15c7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a15c7-139">CommonParameters</span></span>
<span data-ttu-id="a15c7-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a15c7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a15c7-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a15c7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a15c7-142">입력</span><span class="sxs-lookup"><span data-stu-id="a15c7-142">INPUTS</span></span>

### <span data-ttu-id="a15c7-143">않아야</span><span class="sxs-lookup"><span data-stu-id="a15c7-143">None</span></span>

## <span data-ttu-id="a15c7-144">출력</span><span class="sxs-lookup"><span data-stu-id="a15c7-144">OUTPUTS</span></span>

### <span data-ttu-id="a15c7-145">System. 개체</span><span class="sxs-lookup"><span data-stu-id="a15c7-145">System.Object</span></span>
## <span data-ttu-id="a15c7-146">상속자</span><span class="sxs-lookup"><span data-stu-id="a15c7-146">NOTES</span></span>

## <span data-ttu-id="a15c7-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a15c7-147">RELATED LINKS</span></span>
