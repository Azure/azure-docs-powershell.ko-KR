---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 1b51b7d086af738e356d7a6b65c17bdb45cbb518
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359738"
---
# <span data-ttu-id="f963c-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f963c-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="f963c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f963c-102">SYNOPSIS</span></span>
<span data-ttu-id="f963c-103">NetworkInterface에 연결된 TapConfiguration 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f963c-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="f963c-104">기존 VirtualNetworkTap 리소스를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="f963c-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="f963c-105">구문</span><span class="sxs-lookup"><span data-stu-id="f963c-105">SYNTAX</span></span>

### <span data-ttu-id="f963c-106">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="f963c-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f963c-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f963c-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f963c-108">설명</span><span class="sxs-lookup"><span data-stu-id="f963c-108">DESCRIPTION</span></span>
<span data-ttu-id="f963c-109">**Add-AzNetworkInterfaceTapConfig** cmdlet은 NetworkInterface에 연결된 TapConfiguration 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f963c-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="f963c-110">기존 VirtualNetworkTap 리소스를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="f963c-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="f963c-111">예제</span><span class="sxs-lookup"><span data-stu-id="f963c-111">EXAMPLES</span></span>

### <span data-ttu-id="f963c-112">예제 1: 주어진 NetworkInterface에 TapConfiguration 추가</span><span class="sxs-lookup"><span data-stu-id="f963c-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="f963c-113">sourceNic에 TapConfiguration을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f963c-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="f963c-114">sourceNic VM의 트래픽은 vVirtualNetworkTap 리소스에 참조된 대상 VM으로 미러링됩니다.</span><span class="sxs-lookup"><span data-stu-id="f963c-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="f963c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f963c-115">PARAMETERS</span></span>

### <span data-ttu-id="f963c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f963c-116">-DefaultProfile</span></span>
<span data-ttu-id="f963c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f963c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f963c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f963c-118">-Name</span></span>
<span data-ttu-id="f963c-119">탭 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f963c-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="f963c-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f963c-120">-NetworkInterface</span></span>
<span data-ttu-id="f963c-121">네트워크 인터페이스 리소스에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="f963c-121">The reference of the network interface resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f963c-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f963c-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="f963c-123">가상 네트워크 탭 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="f963c-123">The reference of the virtual network tap resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f963c-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="f963c-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="f963c-125">가상 네트워크 탭 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="f963c-125">The reference of the virtual network tap resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f963c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f963c-126">-Confirm</span></span>
<span data-ttu-id="f963c-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f963c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f963c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f963c-128">-WhatIf</span></span>
<span data-ttu-id="f963c-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f963c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f963c-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f963c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f963c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f963c-131">CommonParameters</span></span>
<span data-ttu-id="f963c-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f963c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f963c-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f963c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f963c-134">입력</span><span class="sxs-lookup"><span data-stu-id="f963c-134">INPUTS</span></span>

### <span data-ttu-id="f963c-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f963c-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="f963c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f963c-136">System.String</span></span>

### <span data-ttu-id="f963c-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f963c-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="f963c-138">출력</span><span class="sxs-lookup"><span data-stu-id="f963c-138">OUTPUTS</span></span>

### <span data-ttu-id="f963c-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f963c-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="f963c-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f963c-140">NOTES</span></span>

## <span data-ttu-id="f963c-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f963c-141">RELATED LINKS</span></span>

[<span data-ttu-id="f963c-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f963c-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="f963c-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f963c-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="f963c-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f963c-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
