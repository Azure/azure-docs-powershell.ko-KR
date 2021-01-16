---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 38530b5e4034286d623c82b841064760fe2e49e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344205"
---
# <span data-ttu-id="2a863-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2a863-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="2a863-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a863-102">SYNOPSIS</span></span>
<span data-ttu-id="2a863-103">가상 네트워크 피어링을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2a863-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="2a863-104">구문</span><span class="sxs-lookup"><span data-stu-id="2a863-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a863-105">설명</span><span class="sxs-lookup"><span data-stu-id="2a863-105">DESCRIPTION</span></span>
<span data-ttu-id="2a863-106">가상 네트워크 피어링을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2a863-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="2a863-107">예제</span><span class="sxs-lookup"><span data-stu-id="2a863-107">EXAMPLES</span></span>

### <span data-ttu-id="2a863-108">예제 1: 가상 네트워크 피어링 제거</span><span class="sxs-lookup"><span data-stu-id="2a863-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="2a863-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a863-109">PARAMETERS</span></span>

### <span data-ttu-id="2a863-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a863-110">-AsJob</span></span>
<span data-ttu-id="2a863-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2a863-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a863-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a863-112">-DefaultProfile</span></span>
<span data-ttu-id="2a863-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a863-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a863-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2a863-114">-Force</span></span>
<span data-ttu-id="2a863-115">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2a863-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2a863-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2a863-116">-Name</span></span>
<span data-ttu-id="2a863-117">가상 네트워크 피어링 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a863-117">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a863-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a863-118">-PassThru</span></span>
<span data-ttu-id="2a863-119">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2a863-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2a863-120">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2a863-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2a863-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a863-121">-ResourceGroupName</span></span>
<span data-ttu-id="2a863-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2a863-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a863-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="2a863-123">-VirtualNetworkName</span></span>
<span data-ttu-id="2a863-124">가상 네트워크 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a863-124">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a863-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a863-125">-Confirm</span></span>
<span data-ttu-id="2a863-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2a863-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a863-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a863-127">-WhatIf</span></span>
<span data-ttu-id="2a863-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2a863-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a863-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2a863-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a863-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a863-130">CommonParameters</span></span>
<span data-ttu-id="2a863-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2a863-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a863-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2a863-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a863-133">입력</span><span class="sxs-lookup"><span data-stu-id="2a863-133">INPUTS</span></span>

### <span data-ttu-id="2a863-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2a863-134">System.String</span></span>

## <span data-ttu-id="2a863-135">출력</span><span class="sxs-lookup"><span data-stu-id="2a863-135">OUTPUTS</span></span>

### <span data-ttu-id="2a863-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a863-136">System.Boolean</span></span>

## <span data-ttu-id="2a863-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2a863-137">NOTES</span></span>

## <span data-ttu-id="2a863-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a863-138">RELATED LINKS</span></span>

[<span data-ttu-id="2a863-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2a863-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="2a863-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2a863-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="2a863-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2a863-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)