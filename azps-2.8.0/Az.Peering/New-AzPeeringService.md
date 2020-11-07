---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 29062aa6ae5a69e44973fbdc29c6e9c6d2a583fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872353"
---
# <span data-ttu-id="7b554-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="7b554-101">New-AzPeeringService</span></span>

## <span data-ttu-id="7b554-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b554-102">SYNOPSIS</span></span>
<span data-ttu-id="7b554-103">새 피어 링 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7b554-103">Creates a new peering service.</span></span>

## <span data-ttu-id="7b554-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b554-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b554-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7b554-105">DESCRIPTION</span></span>
<span data-ttu-id="7b554-106">피어 링 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7b554-106">Creates peering service.</span></span>

## <span data-ttu-id="7b554-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7b554-107">EXAMPLES</span></span>

### <span data-ttu-id="7b554-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7b554-108">Example 1</span></span>
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

<span data-ttu-id="7b554-109">공급자 및 피어 링 위치를 사용 하 여 피어 링 서비스 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7b554-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="7b554-110">And를 사용 하 여 conjuction에서 `Get-AzPeeringServiceProvider``Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="7b554-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="7b554-111">변수</span><span class="sxs-lookup"><span data-stu-id="7b554-111">PARAMETERS</span></span>

### <span data-ttu-id="7b554-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b554-112">-AsJob</span></span>
<span data-ttu-id="7b554-113">백그라운드에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b554-113">Run in the background.</span></span>

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

### <span data-ttu-id="7b554-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b554-114">-DefaultProfile</span></span>
<span data-ttu-id="7b554-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b554-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b554-116">-이름</span><span class="sxs-lookup"><span data-stu-id="7b554-116">-Name</span></span>
<span data-ttu-id="7b554-117">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b554-117">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="7b554-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="7b554-118">-PeeringLocation</span></span>
<span data-ttu-id="7b554-119">Azure 지역과는 다른 실제 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7b554-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="7b554-120">Get-AzPeeringServiceLocation 사용 [-국가 <country> ]</span><span class="sxs-lookup"><span data-stu-id="7b554-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

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

### <span data-ttu-id="7b554-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="7b554-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="7b554-122">피어 링 서비스 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b554-122">The peering service provider name.</span></span>
<span data-ttu-id="7b554-123">목록에 Get-AzPeeringServiceProvider cmdlet 사용</span><span class="sxs-lookup"><span data-stu-id="7b554-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

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

### <span data-ttu-id="7b554-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b554-124">-ResourceGroupName</span></span>
<span data-ttu-id="7b554-125">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b554-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="7b554-126">태그</span><span class="sxs-lookup"><span data-stu-id="7b554-126">-Tag</span></span>
<span data-ttu-id="7b554-127">Microsoft InputObject 서비스와 연결할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="7b554-127">The tags to associate with the Microsoft InputObject Service.</span></span>

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

### <span data-ttu-id="7b554-128">-확인</span><span class="sxs-lookup"><span data-stu-id="7b554-128">-Confirm</span></span>
<span data-ttu-id="7b554-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b554-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b554-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b554-130">-WhatIf</span></span>
<span data-ttu-id="7b554-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b554-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b554-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b554-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b554-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b554-133">CommonParameters</span></span>
<span data-ttu-id="7b554-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b554-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b554-135">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7b554-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b554-136">입력</span><span class="sxs-lookup"><span data-stu-id="7b554-136">INPUTS</span></span>

### <span data-ttu-id="7b554-137">않아야</span><span class="sxs-lookup"><span data-stu-id="7b554-137">None</span></span>

## <span data-ttu-id="7b554-138">출력</span><span class="sxs-lookup"><span data-stu-id="7b554-138">OUTPUTS</span></span>

### <span data-ttu-id="7b554-139">PSPeeringService (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7b554-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="7b554-140">상속자</span><span class="sxs-lookup"><span data-stu-id="7b554-140">NOTES</span></span>

## <span data-ttu-id="7b554-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b554-141">RELATED LINKS</span></span>
