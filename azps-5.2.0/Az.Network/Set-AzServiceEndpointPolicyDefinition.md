---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 46d86b6a910abcd00257277f61bb44dd426ab945
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357477"
---
# <span data-ttu-id="f130b-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f130b-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="f130b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f130b-102">SYNOPSIS</span></span>
<span data-ttu-id="f130b-103">서비스 엔드포인트 정책 정의를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f130b-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="f130b-104">구문</span><span class="sxs-lookup"><span data-stu-id="f130b-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f130b-105">설명</span><span class="sxs-lookup"><span data-stu-id="f130b-105">DESCRIPTION</span></span>
<span data-ttu-id="f130b-106">**Set-AzServiceEndpointPolicyDefinition** cmdlet은 서비스 엔드포인트 정책 정의를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f130b-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="f130b-107">예제</span><span class="sxs-lookup"><span data-stu-id="f130b-107">EXAMPLES</span></span>

### <span data-ttu-id="f130b-108">예제 1: 서비스 엔드포인트 정책에서 서비스 엔드포인트 정책 정의 업데이트</span><span class="sxs-lookup"><span data-stu-id="f130b-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="f130b-109">이 명령은 개체가 정의한 서비스 엔드포인트 정책에서 Policydef1이라는 서비스 엔드포인트 정책 정의를 $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="f130b-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="f130b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f130b-110">PARAMETERS</span></span>

### <span data-ttu-id="f130b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f130b-111">-DefaultProfile</span></span>
<span data-ttu-id="f130b-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f130b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f130b-113">-Description</span><span class="sxs-lookup"><span data-stu-id="f130b-113">-Description</span></span>
<span data-ttu-id="f130b-114">정의에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="f130b-114">The description of the definition</span></span>

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

### <span data-ttu-id="f130b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f130b-115">-Name</span></span>
<span data-ttu-id="f130b-116">규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="f130b-116">The name of the rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f130b-117">-Service</span><span class="sxs-lookup"><span data-stu-id="f130b-117">-Service</span></span>
<span data-ttu-id="f130b-118">서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="f130b-118">Name of the service</span></span>

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

### <span data-ttu-id="f130b-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f130b-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="f130b-120">The NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f130b-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="f130b-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="f130b-121">-ServiceResource</span></span>
<span data-ttu-id="f130b-122">서비스 리소스 목록</span><span class="sxs-lookup"><span data-stu-id="f130b-122">List of service resources</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f130b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f130b-123">-Confirm</span></span>
<span data-ttu-id="f130b-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f130b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f130b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f130b-125">-WhatIf</span></span>
<span data-ttu-id="f130b-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f130b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f130b-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f130b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f130b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f130b-128">CommonParameters</span></span>
<span data-ttu-id="f130b-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f130b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f130b-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f130b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f130b-131">입력</span><span class="sxs-lookup"><span data-stu-id="f130b-131">INPUTS</span></span>

### <span data-ttu-id="f130b-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f130b-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f130b-133">출력</span><span class="sxs-lookup"><span data-stu-id="f130b-133">OUTPUTS</span></span>

### <span data-ttu-id="f130b-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f130b-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f130b-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f130b-135">NOTES</span></span>

## <span data-ttu-id="f130b-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f130b-136">RELATED LINKS</span></span>

[<span data-ttu-id="f130b-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f130b-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f130b-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f130b-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f130b-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f130b-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f130b-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f130b-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
