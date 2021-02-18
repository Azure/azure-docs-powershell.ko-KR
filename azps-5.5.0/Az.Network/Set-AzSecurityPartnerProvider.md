---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206496"
---
# <span data-ttu-id="2d61e-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d61e-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="2d61e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d61e-102">SYNOPSIS</span></span>
<span data-ttu-id="2d61e-103">수정된 Azure SecurityPartnerProvider를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2d61e-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="2d61e-104">구문</span><span class="sxs-lookup"><span data-stu-id="2d61e-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d61e-105">설명</span><span class="sxs-lookup"><span data-stu-id="2d61e-105">DESCRIPTION</span></span>
<span data-ttu-id="2d61e-106">**Set-AzSecurityPartnerProvider** cmdlet은 Azure SecurityPartnerProvider를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2d61e-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="2d61e-107">예제</span><span class="sxs-lookup"><span data-stu-id="2d61e-107">EXAMPLES</span></span>

### <span data-ttu-id="2d61e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2d61e-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="2d61e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d61e-109">PARAMETERS</span></span>

### <span data-ttu-id="2d61e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d61e-110">-AsJob</span></span>
<span data-ttu-id="2d61e-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2d61e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d61e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d61e-112">-DefaultProfile</span></span>
<span data-ttu-id="2d61e-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d61e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d61e-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d61e-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="2d61e-115">The SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d61e-115">The SecurityPartnerProvider</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d61e-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d61e-116">-Confirm</span></span>
<span data-ttu-id="2d61e-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2d61e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d61e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d61e-118">-WhatIf</span></span>
<span data-ttu-id="2d61e-119">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2d61e-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d61e-120">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d61e-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d61e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d61e-121">CommonParameters</span></span>
<span data-ttu-id="2d61e-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2d61e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d61e-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2d61e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d61e-124">입력</span><span class="sxs-lookup"><span data-stu-id="2d61e-124">INPUTS</span></span>

### <span data-ttu-id="2d61e-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d61e-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="2d61e-126">출력</span><span class="sxs-lookup"><span data-stu-id="2d61e-126">OUTPUTS</span></span>

### <span data-ttu-id="2d61e-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d61e-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="2d61e-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2d61e-128">NOTES</span></span>

## <span data-ttu-id="2d61e-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d61e-129">RELATED LINKS</span></span>
