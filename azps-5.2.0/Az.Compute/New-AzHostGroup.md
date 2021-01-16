---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 2fdb5317504bb1bc08ed45e8224a30a61cca8e8c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364554"
---
# <span data-ttu-id="6cce5-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="6cce5-101">New-AzHostGroup</span></span>

## <span data-ttu-id="6cce5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cce5-102">SYNOPSIS</span></span>
<span data-ttu-id="6cce5-103">호스트 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6cce5-103">Creates a host group.</span></span>

## <span data-ttu-id="6cce5-104">구문</span><span class="sxs-lookup"><span data-stu-id="6cce5-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cce5-105">설명</span><span class="sxs-lookup"><span data-stu-id="6cce5-105">DESCRIPTION</span></span>
<span data-ttu-id="6cce5-106">이 cmdlet은 호스트 그룹을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6cce5-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="6cce5-107">예제</span><span class="sxs-lookup"><span data-stu-id="6cce5-107">EXAMPLES</span></span>

### <span data-ttu-id="6cce5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6cce5-108">Example 1</span></span>
```
PS C:\> New-AzHostGroup -ResourceGroupName $resourceGroupName -Name $hostGroupName -Location $location -Zone $zone

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="6cce5-109">이 명령은 주어진 위치 및 영역의 호스트 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6cce5-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="6cce5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cce5-110">PARAMETERS</span></span>

### <span data-ttu-id="6cce5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cce5-111">-AsJob</span></span>
<span data-ttu-id="6cce5-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6cce5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6cce5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cce5-113">-DefaultProfile</span></span>
<span data-ttu-id="6cce5-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6cce5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cce5-115">-Location</span><span class="sxs-lookup"><span data-stu-id="6cce5-115">-Location</span></span>
<span data-ttu-id="6cce5-116">위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6cce5-116">Specifies location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cce5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6cce5-117">-Name</span></span>
<span data-ttu-id="6cce5-118">호스트 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6cce5-118">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cce5-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="6cce5-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="6cce5-120">호스트 그룹이 확장할 수 있는 장애 도메인의 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6cce5-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="6cce5-121">최소값은 1, 최대값은 3입니다.</span><span class="sxs-lookup"><span data-stu-id="6cce5-121">The minimum value is 1 and the maximum value is 3.</span></span>

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

### <span data-ttu-id="6cce5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cce5-122">-ResourceGroupName</span></span>
<span data-ttu-id="6cce5-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6cce5-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cce5-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="6cce5-124">-Tag</span></span>
<span data-ttu-id="6cce5-125">태그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6cce5-125">Specifies Tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cce5-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="6cce5-126">-Zone</span></span>
<span data-ttu-id="6cce5-127">호스트 그룹의 영역 지정</span><span class="sxs-lookup"><span data-stu-id="6cce5-127">Specifies Zones of the host group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cce5-128">-SupportAutomaticPlacement</span><span class="sxs-lookup"><span data-stu-id="6cce5-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="6cce5-129">HostGroup이 vm의 자동 배치를 사용하도록 설정할지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6cce5-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="6cce5-130">자동 배치는 이러한 VM이 전용 호스트 그룹에서 Azure에서 선택한 전용 호스트에 배치되는 것을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="6cce5-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="6cce5-131">지정하지 않으면 기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="6cce5-131">If not specified, default value will be true.</span></span>

```yaml
Type: bool
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="6cce5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cce5-132">-Confirm</span></span>
<span data-ttu-id="6cce5-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6cce5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cce5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cce5-134">-WhatIf</span></span>
<span data-ttu-id="6cce5-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6cce5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cce5-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6cce5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cce5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cce5-137">CommonParameters</span></span>
<span data-ttu-id="6cce5-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6cce5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cce5-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6cce5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cce5-140">입력</span><span class="sxs-lookup"><span data-stu-id="6cce5-140">INPUTS</span></span>

### <span data-ttu-id="6cce5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6cce5-141">System.String</span></span>

## <span data-ttu-id="6cce5-142">출력</span><span class="sxs-lookup"><span data-stu-id="6cce5-142">OUTPUTS</span></span>

### <span data-ttu-id="6cce5-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="6cce5-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="6cce5-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6cce5-144">NOTES</span></span>

## <span data-ttu-id="6cce5-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6cce5-145">RELATED LINKS</span></span>
