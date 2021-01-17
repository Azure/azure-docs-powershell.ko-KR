---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: 4fbc1729debb7f5cf822f152107797e10b1f7ba9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371596"
---
# <span data-ttu-id="a88f8-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a88f8-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="a88f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a88f8-102">SYNOPSIS</span></span>
<span data-ttu-id="a88f8-103">서비스 엔드포인트 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="a88f8-104">구문</span><span class="sxs-lookup"><span data-stu-id="a88f8-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a88f8-105">설명</span><span class="sxs-lookup"><span data-stu-id="a88f8-105">DESCRIPTION</span></span>
<span data-ttu-id="a88f8-106">**New-AzServiceEndpointPolicy** cmdlet은 서비스 엔드포인트 정책을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="a88f8-107">예제</span><span class="sxs-lookup"><span data-stu-id="a88f8-107">EXAMPLES</span></span>

### <span data-ttu-id="a88f8-108">예제 1: 서비스 엔드포인트 정책 생성</span><span class="sxs-lookup"><span data-stu-id="a88f8-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="a88f8-109">이 명령은 개체가 정의한 Policy1이라는 서비스 엔드포인트 정책을 만들고 $serviceEndpointDefinition 정의를 $serviceEndpointPolicy 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="a88f8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a88f8-110">PARAMETERS</span></span>

### <span data-ttu-id="a88f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a88f8-111">-DefaultProfile</span></span>
<span data-ttu-id="a88f8-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a88f8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a88f8-113">-Force</span></span>
<span data-ttu-id="a88f8-114">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a88f8-115">-Location</span><span class="sxs-lookup"><span data-stu-id="a88f8-115">-Location</span></span>
<span data-ttu-id="a88f8-116">위치.</span><span class="sxs-lookup"><span data-stu-id="a88f8-116">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a88f8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a88f8-117">-Name</span></span>
<span data-ttu-id="a88f8-118">서브넷의 이름</span><span class="sxs-lookup"><span data-stu-id="a88f8-118">The name of the subnet</span></span>

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

### <span data-ttu-id="a88f8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a88f8-119">-ResourceGroupName</span></span>
<span data-ttu-id="a88f8-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a88f8-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a88f8-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="a88f8-122">서비스 엔드포인트 정의 목록</span><span class="sxs-lookup"><span data-stu-id="a88f8-122">List of service endpoint definitions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a88f8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a88f8-123">-Confirm</span></span>
<span data-ttu-id="a88f8-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a88f8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a88f8-125">-WhatIf</span></span>
<span data-ttu-id="a88f8-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a88f8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a88f8-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a88f8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a88f8-128">CommonParameters</span></span>
<span data-ttu-id="a88f8-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a88f8-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a88f8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a88f8-131">입력</span><span class="sxs-lookup"><span data-stu-id="a88f8-131">INPUTS</span></span>

### <span data-ttu-id="a88f8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a88f8-132">System.String</span></span>

## <span data-ttu-id="a88f8-133">출력</span><span class="sxs-lookup"><span data-stu-id="a88f8-133">OUTPUTS</span></span>

### <span data-ttu-id="a88f8-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a88f8-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="a88f8-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a88f8-135">NOTES</span></span>

## <span data-ttu-id="a88f8-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a88f8-136">RELATED LINKS</span></span>

[<span data-ttu-id="a88f8-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a88f8-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="a88f8-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a88f8-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="a88f8-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a88f8-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
