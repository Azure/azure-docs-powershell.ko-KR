---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203881"
---
# <span data-ttu-id="4996d-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4996d-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="4996d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4996d-102">SYNOPSIS</span></span>
<span data-ttu-id="4996d-103">수정 된 Azure SecurityPartnerProvider를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4996d-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="4996d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4996d-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4996d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4996d-105">DESCRIPTION</span></span>
<span data-ttu-id="4996d-106">**AzSecurityPartnerProvider** Cmdlet은 Azure SecurityPartnerProvider를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4996d-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="4996d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4996d-107">EXAMPLES</span></span>

### <span data-ttu-id="4996d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4996d-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="4996d-109">변수</span><span class="sxs-lookup"><span data-stu-id="4996d-109">PARAMETERS</span></span>

### <span data-ttu-id="4996d-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4996d-110">-AsJob</span></span>
<span data-ttu-id="4996d-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4996d-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4996d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4996d-112">-DefaultProfile</span></span>
<span data-ttu-id="4996d-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4996d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4996d-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4996d-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="4996d-115">SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4996d-115">The SecurityPartnerProvider</span></span>

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

### <span data-ttu-id="4996d-116">-확인</span><span class="sxs-lookup"><span data-stu-id="4996d-116">-Confirm</span></span>
<span data-ttu-id="4996d-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4996d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4996d-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4996d-118">-WhatIf</span></span>
<span data-ttu-id="4996d-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4996d-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4996d-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4996d-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4996d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4996d-121">CommonParameters</span></span>
<span data-ttu-id="4996d-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4996d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4996d-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4996d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4996d-124">입력</span><span class="sxs-lookup"><span data-stu-id="4996d-124">INPUTS</span></span>

### <span data-ttu-id="4996d-125">PSSecurityPartnerProvider에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4996d-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="4996d-126">출력</span><span class="sxs-lookup"><span data-stu-id="4996d-126">OUTPUTS</span></span>

### <span data-ttu-id="4996d-127">PSSecurityPartnerProvider에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4996d-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="4996d-128">상속자</span><span class="sxs-lookup"><span data-stu-id="4996d-128">NOTES</span></span>

## <span data-ttu-id="4996d-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4996d-129">RELATED LINKS</span></span>
