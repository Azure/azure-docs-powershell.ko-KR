---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 554d3285c80370559bbedfb91430d2b6801a6f51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959499"
---
# <span data-ttu-id="c2e91-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c2e91-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="c2e91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2e91-102">SYNOPSIS</span></span>
<span data-ttu-id="c2e91-103">서비스 엔드포인트 정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c2e91-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="c2e91-104">구문</span><span class="sxs-lookup"><span data-stu-id="c2e91-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2e91-105">설명</span><span class="sxs-lookup"><span data-stu-id="c2e91-105">DESCRIPTION</span></span>
<span data-ttu-id="c2e91-106">**Get-AzServiceEndpointPolicyDefinition** cmdlet은 서비스 엔드포인트 정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c2e91-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="c2e91-107">예제</span><span class="sxs-lookup"><span data-stu-id="c2e91-107">EXAMPLES</span></span>

### <span data-ttu-id="c2e91-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c2e91-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="c2e91-109">이 명령은 ServiceEndpointPolicy에서 ServiceEndpointPolicyDefinition1이라는 서비스 엔드포인트 정책 정의를 $Policy 변수에 $policydef 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e91-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="c2e91-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c2e91-110">PARAMETERS</span></span>

### <span data-ttu-id="c2e91-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2e91-111">-DefaultProfile</span></span>
<span data-ttu-id="c2e91-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2e91-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2e91-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c2e91-113">-Name</span></span>
<span data-ttu-id="c2e91-114">서비스 엔드포인트 정책 정의의 이름</span><span class="sxs-lookup"><span data-stu-id="c2e91-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="c2e91-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c2e91-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="c2e91-116">서비스 엔드포인트 정책</span><span class="sxs-lookup"><span data-stu-id="c2e91-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="c2e91-117">-확인</span><span class="sxs-lookup"><span data-stu-id="c2e91-117">-Confirm</span></span>
<span data-ttu-id="c2e91-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2e91-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2e91-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2e91-119">-WhatIf</span></span>
<span data-ttu-id="c2e91-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2e91-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2e91-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2e91-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2e91-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2e91-122">CommonParameters</span></span>
<span data-ttu-id="c2e91-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c2e91-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2e91-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2e91-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2e91-125">입력</span><span class="sxs-lookup"><span data-stu-id="c2e91-125">INPUTS</span></span>

### <span data-ttu-id="c2e91-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c2e91-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="c2e91-127">출력</span><span class="sxs-lookup"><span data-stu-id="c2e91-127">OUTPUTS</span></span>

### <span data-ttu-id="c2e91-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c2e91-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="c2e91-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c2e91-129">NOTES</span></span>

## <span data-ttu-id="c2e91-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2e91-130">RELATED LINKS</span></span>

[<span data-ttu-id="c2e91-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c2e91-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="c2e91-132">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c2e91-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="c2e91-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c2e91-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="c2e91-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c2e91-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
