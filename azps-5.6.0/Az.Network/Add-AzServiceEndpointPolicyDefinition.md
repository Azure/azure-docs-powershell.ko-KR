---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 9a9795547a1d9699a185ae8957852b41d26ca321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979771"
---
# <span data-ttu-id="07845-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="07845-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="07845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07845-102">SYNOPSIS</span></span>
<span data-ttu-id="07845-103">지정된 정책에 서비스 엔드포인트 정책 정의를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07845-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="07845-104">구문</span><span class="sxs-lookup"><span data-stu-id="07845-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07845-105">설명</span><span class="sxs-lookup"><span data-stu-id="07845-105">DESCRIPTION</span></span>
<span data-ttu-id="07845-106">**Add-AzServiceEndpointPolicyDefinition** cmdlet은 정책에 서비스 엔드포인트 정책 정의를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="07845-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="07845-107">예제</span><span class="sxs-lookup"><span data-stu-id="07845-107">EXAMPLES</span></span>

### <span data-ttu-id="07845-108">예제 1: 서비스 엔드포인트 정책에서 서비스 엔드포인트 정책 정의 업데이트</span><span class="sxs-lookup"><span data-stu-id="07845-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="07845-109">이 명령은 ServiceEndpointPolicyDefinition1, Service Microsoft.Storage, 서비스 리소스 구독/하위1 및 ResourceGroup01이라는 리소스 그룹에 속한 설명 "새 정의"라는 이름으로 서비스 엔드포인트 정책 정의를 업데이트하고 $policydef 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="07845-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="07845-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="07845-110">PARAMETERS</span></span>

### <span data-ttu-id="07845-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07845-111">-DefaultProfile</span></span>
<span data-ttu-id="07845-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07845-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07845-113">-Description</span><span class="sxs-lookup"><span data-stu-id="07845-113">-Description</span></span>
<span data-ttu-id="07845-114">정의에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="07845-114">The description of the definition</span></span>

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

### <span data-ttu-id="07845-115">-Name</span><span class="sxs-lookup"><span data-stu-id="07845-115">-Name</span></span>
<span data-ttu-id="07845-116">서비스 엔드포인트 정책 정의의 이름</span><span class="sxs-lookup"><span data-stu-id="07845-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="07845-117">-Service</span><span class="sxs-lookup"><span data-stu-id="07845-117">-Service</span></span>
<span data-ttu-id="07845-118">서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="07845-118">Name of the service</span></span>

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

### <span data-ttu-id="07845-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="07845-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="07845-120">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="07845-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="07845-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="07845-121">-ServiceResource</span></span>
<span data-ttu-id="07845-122">서비스 리소스 목록</span><span class="sxs-lookup"><span data-stu-id="07845-122">List of service resources</span></span>

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

### <span data-ttu-id="07845-123">-확인</span><span class="sxs-lookup"><span data-stu-id="07845-123">-Confirm</span></span>
<span data-ttu-id="07845-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="07845-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07845-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07845-125">-WhatIf</span></span>
<span data-ttu-id="07845-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="07845-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07845-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07845-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07845-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07845-128">CommonParameters</span></span>
<span data-ttu-id="07845-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07845-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07845-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07845-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07845-131">입력</span><span class="sxs-lookup"><span data-stu-id="07845-131">INPUTS</span></span>

### <span data-ttu-id="07845-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="07845-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="07845-133">출력</span><span class="sxs-lookup"><span data-stu-id="07845-133">OUTPUTS</span></span>

### <span data-ttu-id="07845-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="07845-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="07845-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="07845-135">NOTES</span></span>

## <span data-ttu-id="07845-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07845-136">RELATED LINKS</span></span>

[<span data-ttu-id="07845-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="07845-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="07845-138">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="07845-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="07845-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="07845-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="07845-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="07845-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
