---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 1d767677c547c2418ca19e3206f3ca5a25638de0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536552"
---
# <span data-ttu-id="be88a-101">Set-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="be88a-101">Set-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="be88a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be88a-102">SYNOPSIS</span></span>
<span data-ttu-id="be88a-103">가상 네트워크에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be88a-103">Sets the goal state for a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be88a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be88a-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be88a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="be88a-105">DESCRIPTION</span></span>
<span data-ttu-id="be88a-106">**AzureRmVirtualNetworkTap** 는 Azure 가상 네트워크를 탭 하는 데 필요한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be88a-106">The **Set-AzureRmVirtualNetworkTap** sets the goal state for an Azure virtual network tap.</span></span>

## <span data-ttu-id="be88a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="be88a-107">EXAMPLES</span></span>

### <span data-ttu-id="be88a-108">예제 1: 가상 네트워크 구성 탭</span><span class="sxs-lookup"><span data-stu-id="be88a-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzureRmVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="be88a-109">명령이 대상 IpConfiguration을 업데이트 하 고 가상 네트워크 탭을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="be88a-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="be88a-110">이를 참조 하는 탭 구성이 있으면 모든 원본 트래픽이 새 대상 ip 구성 사후 업데이트로 미러링 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be88a-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="be88a-111">변수</span><span class="sxs-lookup"><span data-stu-id="be88a-111">PARAMETERS</span></span>

### <span data-ttu-id="be88a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be88a-112">-AsJob</span></span>
<span data-ttu-id="be88a-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="be88a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="be88a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be88a-114">-DefaultProfile</span></span>
<span data-ttu-id="be88a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="be88a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be88a-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="be88a-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="be88a-117">가상 네트워크 탭</span><span class="sxs-lookup"><span data-stu-id="be88a-117">The virtual network tap</span></span>

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

### <span data-ttu-id="be88a-118">-확인</span><span class="sxs-lookup"><span data-stu-id="be88a-118">-Confirm</span></span>
<span data-ttu-id="be88a-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="be88a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be88a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be88a-120">-WhatIf</span></span>
<span data-ttu-id="be88a-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="be88a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be88a-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be88a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be88a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be88a-123">CommonParameters</span></span>
<span data-ttu-id="be88a-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be88a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be88a-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be88a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be88a-126">입력</span><span class="sxs-lookup"><span data-stu-id="be88a-126">INPUTS</span></span>

### <span data-ttu-id="be88a-127">PSVirtualNetworkTap에 대 한.</span><span class="sxs-lookup"><span data-stu-id="be88a-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="be88a-128">출력</span><span class="sxs-lookup"><span data-stu-id="be88a-128">OUTPUTS</span></span>

### <span data-ttu-id="be88a-129">PSVirtualNetworkTap에 대 한.</span><span class="sxs-lookup"><span data-stu-id="be88a-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="be88a-130">상속자</span><span class="sxs-lookup"><span data-stu-id="be88a-130">NOTES</span></span>

## <span data-ttu-id="be88a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be88a-131">RELATED LINKS</span></span>
