---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 164fc5edb4bac3b90debde0aaf6205c719f5c95c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043285"
---
# <span data-ttu-id="07c2d-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="07c2d-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="07c2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="07c2d-103">서비스 끝점 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07c2d-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="07c2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07c2d-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07c2d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="07c2d-105">DESCRIPTION</span></span>
<span data-ttu-id="07c2d-106">**Get-AzServiceEndpointPolicyDefinition** cmdlet은 서비스 끝점 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07c2d-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="07c2d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="07c2d-107">EXAMPLES</span></span>

### <span data-ttu-id="07c2d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="07c2d-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="07c2d-109">이 명령은 ServiceEndpointPolicy의 ServiceEndpointPolicyDefinition1 라는 서비스 끝점 정책 정의를 가져와 $policydef 변수에 저장 $Policy.</span><span class="sxs-lookup"><span data-stu-id="07c2d-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="07c2d-110">변수</span><span class="sxs-lookup"><span data-stu-id="07c2d-110">PARAMETERS</span></span>

### <span data-ttu-id="07c2d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c2d-111">-DefaultProfile</span></span>
<span data-ttu-id="07c2d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07c2d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07c2d-113">-이름</span><span class="sxs-lookup"><span data-stu-id="07c2d-113">-Name</span></span>
<span data-ttu-id="07c2d-114">서비스 끝점 정책 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07c2d-114">The name of the service endpoint policy definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07c2d-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="07c2d-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="07c2d-116">서비스 끝점 정책</span><span class="sxs-lookup"><span data-stu-id="07c2d-116">The Service endpoint policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07c2d-117">-확인</span><span class="sxs-lookup"><span data-stu-id="07c2d-117">-Confirm</span></span>
<span data-ttu-id="07c2d-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="07c2d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07c2d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07c2d-119">-WhatIf</span></span>
<span data-ttu-id="07c2d-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="07c2d-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07c2d-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07c2d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07c2d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c2d-122">CommonParameters</span></span>
<span data-ttu-id="07c2d-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07c2d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c2d-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="07c2d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c2d-125">입력</span><span class="sxs-lookup"><span data-stu-id="07c2d-125">INPUTS</span></span>

### <span data-ttu-id="07c2d-126">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="07c2d-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="07c2d-127">출력</span><span class="sxs-lookup"><span data-stu-id="07c2d-127">OUTPUTS</span></span>

### <span data-ttu-id="07c2d-128">Microsoft. m a w. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="07c2d-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="07c2d-129">상속자</span><span class="sxs-lookup"><span data-stu-id="07c2d-129">NOTES</span></span>

## <span data-ttu-id="07c2d-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07c2d-130">RELATED LINKS</span></span>

[<span data-ttu-id="07c2d-131">추가-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="07c2d-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="07c2d-132">새로운 AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="07c2d-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="07c2d-133">제거-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="07c2d-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="07c2d-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="07c2d-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
