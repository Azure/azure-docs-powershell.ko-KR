---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 46d86b6a910abcd00257277f61bb44dd426ab945
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309143"
---
# <span data-ttu-id="19822-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19822-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="19822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19822-102">SYNOPSIS</span></span>
<span data-ttu-id="19822-103">서비스 끝점 정책 정의를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="19822-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="19822-104">구문과</span><span class="sxs-lookup"><span data-stu-id="19822-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19822-105">설명은</span><span class="sxs-lookup"><span data-stu-id="19822-105">DESCRIPTION</span></span>
<span data-ttu-id="19822-106">**AzServiceEndpointPolicyDefinition** cmdlet은 서비스 끝점 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="19822-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="19822-107">예제의</span><span class="sxs-lookup"><span data-stu-id="19822-107">EXAMPLES</span></span>

### <span data-ttu-id="19822-108">예제 1: 서비스 끝점 정책에서 서비스 끝점 정책 정의 업데이트</span><span class="sxs-lookup"><span data-stu-id="19822-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="19822-109">이 명령은 $ServiceEndpointPolicy 개체에 정의 된 서비스 끝점 정책의 Policydef1 이라는 서비스 끝점 정책 정의를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="19822-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="19822-110">변수</span><span class="sxs-lookup"><span data-stu-id="19822-110">PARAMETERS</span></span>

### <span data-ttu-id="19822-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19822-111">-DefaultProfile</span></span>
<span data-ttu-id="19822-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19822-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19822-113">-설명</span><span class="sxs-lookup"><span data-stu-id="19822-113">-Description</span></span>
<span data-ttu-id="19822-114">정의에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="19822-114">The description of the definition</span></span>

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

### <span data-ttu-id="19822-115">-이름</span><span class="sxs-lookup"><span data-stu-id="19822-115">-Name</span></span>
<span data-ttu-id="19822-116">규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19822-116">The name of the rule</span></span>

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

### <span data-ttu-id="19822-117">-서비스</span><span class="sxs-lookup"><span data-stu-id="19822-117">-Service</span></span>
<span data-ttu-id="19822-118">서비스 이름</span><span class="sxs-lookup"><span data-stu-id="19822-118">Name of the service</span></span>

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

### <span data-ttu-id="19822-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19822-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="19822-120">NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="19822-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="19822-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="19822-121">-ServiceResource</span></span>
<span data-ttu-id="19822-122">서비스 리소스 목록</span><span class="sxs-lookup"><span data-stu-id="19822-122">List of service resources</span></span>

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

### <span data-ttu-id="19822-123">-확인</span><span class="sxs-lookup"><span data-stu-id="19822-123">-Confirm</span></span>
<span data-ttu-id="19822-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="19822-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19822-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19822-125">-WhatIf</span></span>
<span data-ttu-id="19822-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="19822-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19822-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19822-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19822-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19822-128">CommonParameters</span></span>
<span data-ttu-id="19822-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19822-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19822-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19822-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19822-131">입력</span><span class="sxs-lookup"><span data-stu-id="19822-131">INPUTS</span></span>

### <span data-ttu-id="19822-132">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19822-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="19822-133">출력</span><span class="sxs-lookup"><span data-stu-id="19822-133">OUTPUTS</span></span>

### <span data-ttu-id="19822-134">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19822-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="19822-135">상속자</span><span class="sxs-lookup"><span data-stu-id="19822-135">NOTES</span></span>

## <span data-ttu-id="19822-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19822-136">RELATED LINKS</span></span>

[<span data-ttu-id="19822-137">추가-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19822-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="19822-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19822-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="19822-139">새로운 AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19822-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="19822-140">제거-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="19822-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
