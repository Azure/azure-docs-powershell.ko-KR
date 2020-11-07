---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 1b51b7d086af738e356d7a6b65c17bdb45cbb518
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877473"
---
# <span data-ttu-id="684c5-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="684c5-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="684c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="684c5-102">SYNOPSIS</span></span>
<span data-ttu-id="684c5-103">NetworkInterface와 연결 된 TapConfiguration 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="684c5-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="684c5-104">기존 VirtualNetworkTap 리소스를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="684c5-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="684c5-105">구문과</span><span class="sxs-lookup"><span data-stu-id="684c5-105">SYNTAX</span></span>

### <span data-ttu-id="684c5-106">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="684c5-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="684c5-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="684c5-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="684c5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="684c5-108">DESCRIPTION</span></span>
<span data-ttu-id="684c5-109">**AzNetworkInterfaceTapConfig** Cmdlet은 NetworkInterface와 연결 된 TapConfiguration 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="684c5-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="684c5-110">기존 VirtualNetworkTap 리소스를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="684c5-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="684c5-111">예제의</span><span class="sxs-lookup"><span data-stu-id="684c5-111">EXAMPLES</span></span>

### <span data-ttu-id="684c5-112">예제 1: 지정 된 NetworkInterface에 TapConfiguration 추가</span><span class="sxs-lookup"><span data-stu-id="684c5-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="684c5-113">TapConfiguration를 sourceNic에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="684c5-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="684c5-114">SourceNic VM의 트래픽이 vVirtualNetworkTap 리소스에서 참조 하는 대상 VM으로 미러링 됩니다.</span><span class="sxs-lookup"><span data-stu-id="684c5-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="684c5-115">변수</span><span class="sxs-lookup"><span data-stu-id="684c5-115">PARAMETERS</span></span>

### <span data-ttu-id="684c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="684c5-116">-DefaultProfile</span></span>
<span data-ttu-id="684c5-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="684c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="684c5-118">-이름</span><span class="sxs-lookup"><span data-stu-id="684c5-118">-Name</span></span>
<span data-ttu-id="684c5-119">탭 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="684c5-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="684c5-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="684c5-120">-NetworkInterface</span></span>
<span data-ttu-id="684c5-121">네트워크 인터페이스 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="684c5-121">The reference of the network interface resource.</span></span>

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

### <span data-ttu-id="684c5-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="684c5-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="684c5-123">가상 네트워크의 참조 리소스를 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="684c5-123">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="684c5-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="684c5-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="684c5-125">가상 네트워크의 참조 리소스를 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="684c5-125">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="684c5-126">-확인</span><span class="sxs-lookup"><span data-stu-id="684c5-126">-Confirm</span></span>
<span data-ttu-id="684c5-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="684c5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="684c5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="684c5-128">-WhatIf</span></span>
<span data-ttu-id="684c5-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="684c5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="684c5-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="684c5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="684c5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="684c5-131">CommonParameters</span></span>
<span data-ttu-id="684c5-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="684c5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="684c5-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="684c5-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="684c5-134">입력</span><span class="sxs-lookup"><span data-stu-id="684c5-134">INPUTS</span></span>

### <span data-ttu-id="684c5-135">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="684c5-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="684c5-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="684c5-136">System.String</span></span>

### <span data-ttu-id="684c5-137">PSVirtualNetworkTap에 대 한.</span><span class="sxs-lookup"><span data-stu-id="684c5-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="684c5-138">출력</span><span class="sxs-lookup"><span data-stu-id="684c5-138">OUTPUTS</span></span>

### <span data-ttu-id="684c5-139">PSNetworkInterface에 대 한.</span><span class="sxs-lookup"><span data-stu-id="684c5-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="684c5-140">상속자</span><span class="sxs-lookup"><span data-stu-id="684c5-140">NOTES</span></span>

## <span data-ttu-id="684c5-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="684c5-141">RELATED LINKS</span></span>

[<span data-ttu-id="684c5-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="684c5-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="684c5-143">제거-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="684c5-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="684c5-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="684c5-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
