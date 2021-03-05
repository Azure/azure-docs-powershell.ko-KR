---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 1fc1d2f9269bf48d6f6dfd79caa8e34b3de51fee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989338"
---
# <span data-ttu-id="2f11a-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="2f11a-101">New-AzPeeringService</span></span>

## <span data-ttu-id="2f11a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f11a-102">SYNOPSIS</span></span>
<span data-ttu-id="2f11a-103">새 피어링 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f11a-103">Creates a new peering service.</span></span>

## <span data-ttu-id="2f11a-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f11a-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f11a-105">설명</span><span class="sxs-lookup"><span data-stu-id="2f11a-105">DESCRIPTION</span></span>
<span data-ttu-id="2f11a-106">피어링 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f11a-106">Creates peering service.</span></span>

## <span data-ttu-id="2f11a-107">예제</span><span class="sxs-lookup"><span data-stu-id="2f11a-107">EXAMPLES</span></span>

### <span data-ttu-id="2f11a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2f11a-108">Example 1</span></span>
```powershell
PS C:\> New-AzPeeringService -ResourceGroupName $resourceGroup -Name $name -Location $loc -PeeringServiceProvider $provider

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="2f11a-109">공급자 및 피어링 위치를 통해 피어링 서비스 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f11a-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="2f11a-110">를 사용하여 에 사용 `Get-AzPeeringServiceProvider``Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="2f11a-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="2f11a-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2f11a-111">PARAMETERS</span></span>

### <span data-ttu-id="2f11a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f11a-112">-AsJob</span></span>
<span data-ttu-id="2f11a-113">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2f11a-113">Run in the background.</span></span>

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

### <span data-ttu-id="2f11a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f11a-114">-DefaultProfile</span></span>
<span data-ttu-id="2f11a-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f11a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f11a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2f11a-116">-Name</span></span>
<span data-ttu-id="2f11a-117">PSPeering의 고유한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f11a-117">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="2f11a-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="2f11a-118">-PeeringLocation</span></span>
<span data-ttu-id="2f11a-119">Azure 지역과 다른 물리적 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2f11a-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="2f11a-120">Get-AzPeeringServiceLocation [-Country] 사용 <country></span><span class="sxs-lookup"><span data-stu-id="2f11a-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

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

### <span data-ttu-id="2f11a-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="2f11a-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="2f11a-122">피어링 서비스 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f11a-122">The peering service provider name.</span></span>
<span data-ttu-id="2f11a-123">목록에 Get-AzPeeringServiceProvider cmdlet 사용</span><span class="sxs-lookup"><span data-stu-id="2f11a-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f11a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f11a-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f11a-125">기존 리소스 그룹 이름을 만들거나 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f11a-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="2f11a-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="2f11a-126">-Tag</span></span>
<span data-ttu-id="2f11a-127">Microsoft InputObject 서비스에 연결되는 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="2f11a-127">The tags to associate with the Microsoft InputObject Service.</span></span>

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

### <span data-ttu-id="2f11a-128">-확인</span><span class="sxs-lookup"><span data-stu-id="2f11a-128">-Confirm</span></span>
<span data-ttu-id="2f11a-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f11a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f11a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f11a-130">-WhatIf</span></span>
<span data-ttu-id="2f11a-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2f11a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f11a-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f11a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f11a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f11a-133">CommonParameters</span></span>
<span data-ttu-id="2f11a-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f11a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f11a-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f11a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f11a-136">입력</span><span class="sxs-lookup"><span data-stu-id="2f11a-136">INPUTS</span></span>

### <span data-ttu-id="2f11a-137">없음</span><span class="sxs-lookup"><span data-stu-id="2f11a-137">None</span></span>

## <span data-ttu-id="2f11a-138">출력</span><span class="sxs-lookup"><span data-stu-id="2f11a-138">OUTPUTS</span></span>

### <span data-ttu-id="2f11a-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="2f11a-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="2f11a-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f11a-140">NOTES</span></span>

## <span data-ttu-id="2f11a-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f11a-141">RELATED LINKS</span></span>
