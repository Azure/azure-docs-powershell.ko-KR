---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 547b38fd30f09a305c63054b2f27d33db5ae6a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533355"
---
# <span data-ttu-id="5930c-101">Get-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5930c-101">Get-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="5930c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5930c-102">SYNOPSIS</span></span>
<span data-ttu-id="5930c-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="5930c-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5930c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5930c-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5930c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5930c-105">DESCRIPTION</span></span>
<span data-ttu-id="5930c-106">**Get-AzureRmServiceEndpointPolicyDefinition** cmdlet은 서비스 끝점 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5930c-106">The **Get-AzureRmServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="5930c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5930c-107">EXAMPLES</span></span>

### <span data-ttu-id="5930c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5930c-108">Example 1</span></span>
```
$policydef= Get-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="5930c-109">이 명령은 ServiceEndpointPolicy의 ServiceEndpointPolicyDefinition1 라는 서비스 끝점 정책 정의를 가져와 $policydef 변수에 저장 $Policy.</span><span class="sxs-lookup"><span data-stu-id="5930c-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="5930c-110">변수</span><span class="sxs-lookup"><span data-stu-id="5930c-110">PARAMETERS</span></span>

### <span data-ttu-id="5930c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5930c-111">-DefaultProfile</span></span>
<span data-ttu-id="5930c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5930c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5930c-113">-이름</span><span class="sxs-lookup"><span data-stu-id="5930c-113">-Name</span></span>
<span data-ttu-id="5930c-114">서비스 끝점 정책 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5930c-114">The name of the service endpoint policy definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5930c-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5930c-115">-ResourceId</span></span>
<span data-ttu-id="5930c-116">{{ResourceId: 채우기 설명}}</span><span class="sxs-lookup"><span data-stu-id="5930c-116">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5930c-117">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5930c-117">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="5930c-118">서비스 끝점 정책</span><span class="sxs-lookup"><span data-stu-id="5930c-118">The Service endpoint policy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5930c-119">-확인</span><span class="sxs-lookup"><span data-stu-id="5930c-119">-Confirm</span></span>
<span data-ttu-id="5930c-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5930c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5930c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5930c-121">-WhatIf</span></span>
<span data-ttu-id="5930c-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5930c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5930c-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5930c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5930c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5930c-124">CommonParameters</span></span>
<span data-ttu-id="5930c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5930c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5930c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5930c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5930c-127">입력</span><span class="sxs-lookup"><span data-stu-id="5930c-127">INPUTS</span></span>

### <span data-ttu-id="5930c-128">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5930c-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="5930c-129">출력</span><span class="sxs-lookup"><span data-stu-id="5930c-129">OUTPUTS</span></span>

### <span data-ttu-id="5930c-130">Microsoft. m a w. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5930c-130">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="5930c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="5930c-131">NOTES</span></span>

## <span data-ttu-id="5930c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5930c-132">RELATED LINKS</span></span>
