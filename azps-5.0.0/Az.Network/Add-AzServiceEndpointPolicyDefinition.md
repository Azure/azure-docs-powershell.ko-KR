---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: eaab1bdf26fb1cb99bfa7e947a4b7140971fda53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226609"
---
# <span data-ttu-id="37450-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="37450-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="37450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37450-102">SYNOPSIS</span></span>
<span data-ttu-id="37450-103">지정 된 정책에 서비스 끝점 정책 정의를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="37450-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="37450-104">구문과</span><span class="sxs-lookup"><span data-stu-id="37450-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37450-105">설명은</span><span class="sxs-lookup"><span data-stu-id="37450-105">DESCRIPTION</span></span>
<span data-ttu-id="37450-106">**Add-AzServiceEndpointPolicyDefinition** cmdlet은 서비스 끝점 정책 정의를 정책에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="37450-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="37450-107">예제의</span><span class="sxs-lookup"><span data-stu-id="37450-107">EXAMPLES</span></span>

### <span data-ttu-id="37450-108">예제 1: 서비스 끝점 정책에서 서비스 끝점 정책 정의 업데이트</span><span class="sxs-lookup"><span data-stu-id="37450-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="37450-109">이 명령은 이름 ServiceEndpointPolicyDefinition1, 서비스 Microsoft 저장소, 서비스 리소스 구독/e 3 및 설명 "새 정의"를 업데이트 하 여 ResourceGroup01 이라는 리소스 그룹에 속하고이를 $policydef 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="37450-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="37450-110">변수</span><span class="sxs-lookup"><span data-stu-id="37450-110">PARAMETERS</span></span>

### <span data-ttu-id="37450-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37450-111">-DefaultProfile</span></span>
<span data-ttu-id="37450-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37450-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37450-113">-설명</span><span class="sxs-lookup"><span data-stu-id="37450-113">-Description</span></span>
<span data-ttu-id="37450-114">정의에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="37450-114">The description of the definition</span></span>

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

### <span data-ttu-id="37450-115">-이름</span><span class="sxs-lookup"><span data-stu-id="37450-115">-Name</span></span>
<span data-ttu-id="37450-116">서비스 끝점 정책 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37450-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="37450-117">-서비스</span><span class="sxs-lookup"><span data-stu-id="37450-117">-Service</span></span>
<span data-ttu-id="37450-118">서비스 이름</span><span class="sxs-lookup"><span data-stu-id="37450-118">Name of the service</span></span>

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

### <span data-ttu-id="37450-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="37450-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="37450-120">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="37450-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="37450-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="37450-121">-ServiceResource</span></span>
<span data-ttu-id="37450-122">서비스 리소스 목록</span><span class="sxs-lookup"><span data-stu-id="37450-122">List of service resources</span></span>

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

### <span data-ttu-id="37450-123">-확인</span><span class="sxs-lookup"><span data-stu-id="37450-123">-Confirm</span></span>
<span data-ttu-id="37450-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="37450-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37450-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37450-125">-WhatIf</span></span>
<span data-ttu-id="37450-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="37450-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37450-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37450-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37450-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37450-128">CommonParameters</span></span>
<span data-ttu-id="37450-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37450-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37450-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37450-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37450-131">입력</span><span class="sxs-lookup"><span data-stu-id="37450-131">INPUTS</span></span>

### <span data-ttu-id="37450-132">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="37450-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="37450-133">출력</span><span class="sxs-lookup"><span data-stu-id="37450-133">OUTPUTS</span></span>

### <span data-ttu-id="37450-134">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="37450-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="37450-135">상속자</span><span class="sxs-lookup"><span data-stu-id="37450-135">NOTES</span></span>

## <span data-ttu-id="37450-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37450-136">RELATED LINKS</span></span>

[<span data-ttu-id="37450-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="37450-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="37450-138">새로운 AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="37450-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="37450-139">제거-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="37450-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="37450-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="37450-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
