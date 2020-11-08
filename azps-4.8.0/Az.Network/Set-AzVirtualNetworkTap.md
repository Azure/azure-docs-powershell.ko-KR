---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 38995222182d120cd2067429d0f78798a9ebaaf8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048821"
---
# <span data-ttu-id="a68aa-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a68aa-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="a68aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a68aa-102">SYNOPSIS</span></span>
<span data-ttu-id="a68aa-103">가상 네트워크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a68aa-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="a68aa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a68aa-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a68aa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a68aa-105">DESCRIPTION</span></span>
<span data-ttu-id="a68aa-106">**AzVirtualNetworkTap** cmdlet은 가상 네트워크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a68aa-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="a68aa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a68aa-107">EXAMPLES</span></span>

### <span data-ttu-id="a68aa-108">예제 1: 가상 네트워크 구성 탭</span><span class="sxs-lookup"><span data-stu-id="a68aa-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="a68aa-109">명령이 대상 IpConfiguration을 업데이트 하 고 가상 네트워크 탭을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a68aa-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="a68aa-110">이를 참조 하는 탭 구성이 있으면 모든 원본 트래픽이 새 대상 ip 구성 사후 업데이트로 미러링 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a68aa-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="a68aa-111">변수</span><span class="sxs-lookup"><span data-stu-id="a68aa-111">PARAMETERS</span></span>

### <span data-ttu-id="a68aa-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a68aa-112">-AsJob</span></span>
<span data-ttu-id="a68aa-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a68aa-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a68aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a68aa-114">-DefaultProfile</span></span>
<span data-ttu-id="a68aa-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a68aa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a68aa-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a68aa-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="a68aa-117">가상 네트워크 탭</span><span class="sxs-lookup"><span data-stu-id="a68aa-117">The virtual network tap</span></span>

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

### <span data-ttu-id="a68aa-118">-확인</span><span class="sxs-lookup"><span data-stu-id="a68aa-118">-Confirm</span></span>
<span data-ttu-id="a68aa-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a68aa-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a68aa-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a68aa-120">-WhatIf</span></span>
<span data-ttu-id="a68aa-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a68aa-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a68aa-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a68aa-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a68aa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a68aa-123">CommonParameters</span></span>
<span data-ttu-id="a68aa-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a68aa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a68aa-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a68aa-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a68aa-126">입력</span><span class="sxs-lookup"><span data-stu-id="a68aa-126">INPUTS</span></span>

### <span data-ttu-id="a68aa-127">PSVirtualNetworkTap에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a68aa-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="a68aa-128">출력</span><span class="sxs-lookup"><span data-stu-id="a68aa-128">OUTPUTS</span></span>

### <span data-ttu-id="a68aa-129">PSVirtualNetworkTap에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a68aa-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="a68aa-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a68aa-130">NOTES</span></span>

## <span data-ttu-id="a68aa-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a68aa-131">RELATED LINKS</span></span>

[<span data-ttu-id="a68aa-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a68aa-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="a68aa-133">새로운 AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a68aa-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="a68aa-134">제거-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a68aa-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
