---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 38995222182d120cd2067429d0f78798a9ebaaf8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493166"
---
# <span data-ttu-id="47775-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="47775-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="47775-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47775-102">SYNOPSIS</span></span>
<span data-ttu-id="47775-103">가상 네트워크 탭을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="47775-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="47775-104">구문</span><span class="sxs-lookup"><span data-stu-id="47775-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47775-105">설명</span><span class="sxs-lookup"><span data-stu-id="47775-105">DESCRIPTION</span></span>
<span data-ttu-id="47775-106">**Set-AzVirtualNetworkTap** cmdlet은 가상 네트워크 탭을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="47775-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="47775-107">예제</span><span class="sxs-lookup"><span data-stu-id="47775-107">EXAMPLES</span></span>

### <span data-ttu-id="47775-108">예제 1: 가상 네트워크 탭 구성</span><span class="sxs-lookup"><span data-stu-id="47775-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="47775-109">이 명령은 대상 IpConfiguration을 업데이트하고 가상 네트워크 탭을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="47775-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="47775-110">참조하는 탭 구성이 있는 경우 업데이트 후 모든 원본 트래픽이 새 대상 IP 구성으로 미러링되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47775-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="47775-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47775-111">PARAMETERS</span></span>

### <span data-ttu-id="47775-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47775-112">-AsJob</span></span>
<span data-ttu-id="47775-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="47775-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47775-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47775-114">-DefaultProfile</span></span>
<span data-ttu-id="47775-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47775-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47775-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="47775-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="47775-117">가상 네트워크 탭</span><span class="sxs-lookup"><span data-stu-id="47775-117">The virtual network tap</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47775-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47775-118">-Confirm</span></span>
<span data-ttu-id="47775-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="47775-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47775-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47775-120">-WhatIf</span></span>
<span data-ttu-id="47775-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="47775-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47775-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47775-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47775-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47775-123">CommonParameters</span></span>
<span data-ttu-id="47775-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="47775-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47775-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="47775-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47775-126">입력</span><span class="sxs-lookup"><span data-stu-id="47775-126">INPUTS</span></span>

### <span data-ttu-id="47775-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="47775-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="47775-128">출력</span><span class="sxs-lookup"><span data-stu-id="47775-128">OUTPUTS</span></span>

### <span data-ttu-id="47775-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="47775-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="47775-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="47775-130">NOTES</span></span>

## <span data-ttu-id="47775-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47775-131">RELATED LINKS</span></span>

[<span data-ttu-id="47775-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="47775-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="47775-133">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="47775-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="47775-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="47775-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
