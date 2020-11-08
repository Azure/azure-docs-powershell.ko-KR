---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 38530b5e4034286d623c82b841064760fe2e49e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218299"
---
# <span data-ttu-id="002ef-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="002ef-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="002ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="002ef-102">SYNOPSIS</span></span>
<span data-ttu-id="002ef-103">가상 네트워크 피어 링을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="002ef-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="002ef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="002ef-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="002ef-105">설명은</span><span class="sxs-lookup"><span data-stu-id="002ef-105">DESCRIPTION</span></span>
<span data-ttu-id="002ef-106">가상 네트워크 피어 링을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="002ef-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="002ef-107">예제의</span><span class="sxs-lookup"><span data-stu-id="002ef-107">EXAMPLES</span></span>

### <span data-ttu-id="002ef-108">예제 1: 가상 네트워크 피어 링 제거</span><span class="sxs-lookup"><span data-stu-id="002ef-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="002ef-109">변수</span><span class="sxs-lookup"><span data-stu-id="002ef-109">PARAMETERS</span></span>

### <span data-ttu-id="002ef-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="002ef-110">-AsJob</span></span>
<span data-ttu-id="002ef-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="002ef-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="002ef-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="002ef-112">-DefaultProfile</span></span>
<span data-ttu-id="002ef-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="002ef-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="002ef-114">-Force</span><span class="sxs-lookup"><span data-stu-id="002ef-114">-Force</span></span>
<span data-ttu-id="002ef-115">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="002ef-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="002ef-116">-이름</span><span class="sxs-lookup"><span data-stu-id="002ef-116">-Name</span></span>
<span data-ttu-id="002ef-117">가상 네트워크 피어 링 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="002ef-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="002ef-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="002ef-118">-PassThru</span></span>
<span data-ttu-id="002ef-119">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="002ef-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="002ef-120">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="002ef-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="002ef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="002ef-121">-ResourceGroupName</span></span>
<span data-ttu-id="002ef-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="002ef-122">The resource group name</span></span>

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

### <span data-ttu-id="002ef-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="002ef-123">-VirtualNetworkName</span></span>
<span data-ttu-id="002ef-124">가상 네트워크 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="002ef-124">The virtual network name.</span></span>

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

### <span data-ttu-id="002ef-125">-확인</span><span class="sxs-lookup"><span data-stu-id="002ef-125">-Confirm</span></span>
<span data-ttu-id="002ef-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="002ef-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="002ef-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="002ef-127">-WhatIf</span></span>
<span data-ttu-id="002ef-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="002ef-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="002ef-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="002ef-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="002ef-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="002ef-130">CommonParameters</span></span>
<span data-ttu-id="002ef-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="002ef-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="002ef-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="002ef-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="002ef-133">입력</span><span class="sxs-lookup"><span data-stu-id="002ef-133">INPUTS</span></span>

### <span data-ttu-id="002ef-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="002ef-134">System.String</span></span>

## <span data-ttu-id="002ef-135">출력</span><span class="sxs-lookup"><span data-stu-id="002ef-135">OUTPUTS</span></span>

### <span data-ttu-id="002ef-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="002ef-136">System.Boolean</span></span>

## <span data-ttu-id="002ef-137">상속자</span><span class="sxs-lookup"><span data-stu-id="002ef-137">NOTES</span></span>

## <span data-ttu-id="002ef-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="002ef-138">RELATED LINKS</span></span>

[<span data-ttu-id="002ef-139">추가-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="002ef-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="002ef-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="002ef-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="002ef-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="002ef-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
