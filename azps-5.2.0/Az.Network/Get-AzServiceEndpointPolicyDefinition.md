---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 164fc5edb4bac3b90debde0aaf6205c719f5c95c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342825"
---
# <span data-ttu-id="57b2e-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="57b2e-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="57b2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="57b2e-103">서비스 엔드포인트 정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57b2e-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="57b2e-104">구문</span><span class="sxs-lookup"><span data-stu-id="57b2e-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57b2e-105">설명</span><span class="sxs-lookup"><span data-stu-id="57b2e-105">DESCRIPTION</span></span>
<span data-ttu-id="57b2e-106">**Get-AzServiceEndpointPolicyDefinition** cmdlet은 서비스 엔드포인트 정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57b2e-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="57b2e-107">예제</span><span class="sxs-lookup"><span data-stu-id="57b2e-107">EXAMPLES</span></span>

### <span data-ttu-id="57b2e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="57b2e-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="57b2e-109">이 명령은 ServiceEndpointPolicy에서 ServiceEndpointPolicyDefinition1이라는 서비스 엔드포인트 정책 정의를 $Policy 변수에 $policydef 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="57b2e-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="57b2e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57b2e-110">PARAMETERS</span></span>

### <span data-ttu-id="57b2e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57b2e-111">-DefaultProfile</span></span>
<span data-ttu-id="57b2e-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57b2e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57b2e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="57b2e-113">-Name</span></span>
<span data-ttu-id="57b2e-114">서비스 엔드포인트 정책 정의의 이름</span><span class="sxs-lookup"><span data-stu-id="57b2e-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="57b2e-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="57b2e-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="57b2e-116">서비스 엔드포인트 정책</span><span class="sxs-lookup"><span data-stu-id="57b2e-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="57b2e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57b2e-117">-Confirm</span></span>
<span data-ttu-id="57b2e-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="57b2e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57b2e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57b2e-119">-WhatIf</span></span>
<span data-ttu-id="57b2e-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="57b2e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57b2e-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57b2e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57b2e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b2e-122">CommonParameters</span></span>
<span data-ttu-id="57b2e-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57b2e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b2e-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="57b2e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b2e-125">입력</span><span class="sxs-lookup"><span data-stu-id="57b2e-125">INPUTS</span></span>

### <span data-ttu-id="57b2e-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="57b2e-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="57b2e-127">출력</span><span class="sxs-lookup"><span data-stu-id="57b2e-127">OUTPUTS</span></span>

### <span data-ttu-id="57b2e-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="57b2e-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="57b2e-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="57b2e-129">NOTES</span></span>

## <span data-ttu-id="57b2e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57b2e-130">RELATED LINKS</span></span>

[<span data-ttu-id="57b2e-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="57b2e-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="57b2e-132">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="57b2e-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="57b2e-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="57b2e-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="57b2e-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="57b2e-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
