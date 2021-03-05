---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: f47b1bcc571337de8a64c591383367568cf7d67e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993524"
---
# <span data-ttu-id="d90c0-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d90c0-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="d90c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d90c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d90c0-103">가상 네트워크 피어링을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d90c0-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="d90c0-104">구문</span><span class="sxs-lookup"><span data-stu-id="d90c0-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d90c0-105">설명</span><span class="sxs-lookup"><span data-stu-id="d90c0-105">DESCRIPTION</span></span>
<span data-ttu-id="d90c0-106">가상 네트워크 피어링을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d90c0-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="d90c0-107">예제</span><span class="sxs-lookup"><span data-stu-id="d90c0-107">EXAMPLES</span></span>

### <span data-ttu-id="d90c0-108">예제 1: 가상 네트워크 피어링 제거</span><span class="sxs-lookup"><span data-stu-id="d90c0-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="d90c0-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d90c0-109">PARAMETERS</span></span>

### <span data-ttu-id="d90c0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d90c0-110">-AsJob</span></span>
<span data-ttu-id="d90c0-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d90c0-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d90c0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d90c0-112">-DefaultProfile</span></span>
<span data-ttu-id="d90c0-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d90c0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d90c0-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d90c0-114">-Force</span></span>
<span data-ttu-id="d90c0-115">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d90c0-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d90c0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d90c0-116">-Name</span></span>
<span data-ttu-id="d90c0-117">가상 네트워크 피어링 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d90c0-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="d90c0-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d90c0-118">-PassThru</span></span>
<span data-ttu-id="d90c0-119">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d90c0-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d90c0-120">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d90c0-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d90c0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d90c0-121">-ResourceGroupName</span></span>
<span data-ttu-id="d90c0-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d90c0-122">The resource group name</span></span>

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

### <span data-ttu-id="d90c0-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d90c0-123">-VirtualNetworkName</span></span>
<span data-ttu-id="d90c0-124">가상 네트워크 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d90c0-124">The virtual network name.</span></span>

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

### <span data-ttu-id="d90c0-125">-확인</span><span class="sxs-lookup"><span data-stu-id="d90c0-125">-Confirm</span></span>
<span data-ttu-id="d90c0-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d90c0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d90c0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d90c0-127">-WhatIf</span></span>
<span data-ttu-id="d90c0-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d90c0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d90c0-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d90c0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d90c0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d90c0-130">CommonParameters</span></span>
<span data-ttu-id="d90c0-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d90c0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d90c0-132">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d90c0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d90c0-133">입력</span><span class="sxs-lookup"><span data-stu-id="d90c0-133">INPUTS</span></span>

### <span data-ttu-id="d90c0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d90c0-134">System.String</span></span>

## <span data-ttu-id="d90c0-135">출력</span><span class="sxs-lookup"><span data-stu-id="d90c0-135">OUTPUTS</span></span>

### <span data-ttu-id="d90c0-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d90c0-136">System.Boolean</span></span>

## <span data-ttu-id="d90c0-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d90c0-137">NOTES</span></span>

## <span data-ttu-id="d90c0-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d90c0-138">RELATED LINKS</span></span>

[<span data-ttu-id="d90c0-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d90c0-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="d90c0-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d90c0-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="d90c0-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d90c0-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
