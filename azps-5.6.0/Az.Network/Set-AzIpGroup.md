---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 8f8e40f5b2209b75c52376c08b69dff8946add77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976528"
---
# <span data-ttu-id="d909c-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d909c-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="d909c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d909c-102">SYNOPSIS</span></span>
<span data-ttu-id="d909c-103">수정된 방화벽을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d909c-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="d909c-104">구문</span><span class="sxs-lookup"><span data-stu-id="d909c-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d909c-105">설명</span><span class="sxs-lookup"><span data-stu-id="d909c-105">DESCRIPTION</span></span>
<span data-ttu-id="d909c-106">**Set-AzIpGroup** cmdlet은 Azure IpGroup을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d909c-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="d909c-107">예제</span><span class="sxs-lookup"><span data-stu-id="d909c-107">EXAMPLES</span></span>

### <span data-ttu-id="d909c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d909c-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="d909c-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d909c-109">PARAMETERS</span></span>

### <span data-ttu-id="d909c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d909c-110">-AsJob</span></span>
<span data-ttu-id="d909c-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d909c-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d909c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d909c-112">-DefaultProfile</span></span>
<span data-ttu-id="d909c-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d909c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d909c-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="d909c-114">-IpGroup</span></span>
<span data-ttu-id="d909c-115">The IpGroup</span><span class="sxs-lookup"><span data-stu-id="d909c-115">The IpGroup</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d909c-116">-확인</span><span class="sxs-lookup"><span data-stu-id="d909c-116">-Confirm</span></span>
<span data-ttu-id="d909c-117">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d909c-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d909c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d909c-118">-WhatIf</span></span>
<span data-ttu-id="d909c-119">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d909c-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d909c-120">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d909c-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d909c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d909c-121">CommonParameters</span></span>
<span data-ttu-id="d909c-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d909c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d909c-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d909c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d909c-124">입력</span><span class="sxs-lookup"><span data-stu-id="d909c-124">INPUTS</span></span>

### <span data-ttu-id="d909c-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="d909c-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="d909c-126">출력</span><span class="sxs-lookup"><span data-stu-id="d909c-126">OUTPUTS</span></span>

### <span data-ttu-id="d909c-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="d909c-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="d909c-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d909c-128">NOTES</span></span>

## <span data-ttu-id="d909c-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d909c-129">RELATED LINKS</span></span>
