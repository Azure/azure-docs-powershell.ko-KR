---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 634beeaf33515ac5e89011ab47eaea34eccaa581
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700275"
---
# <span data-ttu-id="29c2f-101">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="29c2f-101">New-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="29c2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="29c2f-103">서비스 끝점 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="29c2f-103">Creates a service endpoint policy definition.</span></span>

## <span data-ttu-id="29c2f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="29c2f-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicyDefinition -Name <String> [-Description <String>] [-ServiceResource <String[]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29c2f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="29c2f-105">DESCRIPTION</span></span>
<span data-ttu-id="29c2f-106">**새 AzServiceEndpointPolicyDefinition** cmdlet은 서비스 끝점 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="29c2f-106">The **New-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="29c2f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="29c2f-107">EXAMPLES</span></span>

### <span data-ttu-id="29c2f-108">예제 1: 서비스 끝점 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="29c2f-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="29c2f-109">이 명령은 name ServiceEndpointPolicyDefinition1, 서비스 리소스 구독/e 5 및 설명 "새 정의"가 ResourceGroup01 이라는 리소스 그룹에 속하고이를 $policydef 변수에 저장 하는 서비스 끝점 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="29c2f-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="29c2f-110">변수</span><span class="sxs-lookup"><span data-stu-id="29c2f-110">PARAMETERS</span></span>

### <span data-ttu-id="29c2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c2f-111">-DefaultProfile</span></span>
<span data-ttu-id="29c2f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29c2f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29c2f-113">-설명</span><span class="sxs-lookup"><span data-stu-id="29c2f-113">-Description</span></span>
<span data-ttu-id="29c2f-114">정의에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="29c2f-114">The description of the definition</span></span>

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

### <span data-ttu-id="29c2f-115">-이름</span><span class="sxs-lookup"><span data-stu-id="29c2f-115">-Name</span></span>
<span data-ttu-id="29c2f-116">서비스 끝점 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29c2f-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="29c2f-117">-서비스</span><span class="sxs-lookup"><span data-stu-id="29c2f-117">-Service</span></span>
<span data-ttu-id="29c2f-118">서비스 이름</span><span class="sxs-lookup"><span data-stu-id="29c2f-118">Name of the service</span></span>

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

### <span data-ttu-id="29c2f-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="29c2f-119">-ServiceResource</span></span>
<span data-ttu-id="29c2f-120">서비스 리소스 목록</span><span class="sxs-lookup"><span data-stu-id="29c2f-120">List of service resources</span></span>

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

### <span data-ttu-id="29c2f-121">-확인</span><span class="sxs-lookup"><span data-stu-id="29c2f-121">-Confirm</span></span>
<span data-ttu-id="29c2f-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="29c2f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29c2f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29c2f-123">-WhatIf</span></span>
<span data-ttu-id="29c2f-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="29c2f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29c2f-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29c2f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29c2f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c2f-126">CommonParameters</span></span>
<span data-ttu-id="29c2f-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29c2f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c2f-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29c2f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c2f-129">입력</span><span class="sxs-lookup"><span data-stu-id="29c2f-129">INPUTS</span></span>

### <span data-ttu-id="29c2f-130">않아야</span><span class="sxs-lookup"><span data-stu-id="29c2f-130">None</span></span>

## <span data-ttu-id="29c2f-131">출력</span><span class="sxs-lookup"><span data-stu-id="29c2f-131">OUTPUTS</span></span>

### <span data-ttu-id="29c2f-132">Microsoft. m a w. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="29c2f-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="29c2f-133">상속자</span><span class="sxs-lookup"><span data-stu-id="29c2f-133">NOTES</span></span>

## <span data-ttu-id="29c2f-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29c2f-134">RELATED LINKS</span></span>

[<span data-ttu-id="29c2f-135">추가-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="29c2f-135">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="29c2f-136">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="29c2f-136">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="29c2f-137">제거-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="29c2f-137">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="29c2f-138">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="29c2f-138">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)