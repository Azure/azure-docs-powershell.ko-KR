---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: e7025a48fd1d83a0018ac18de01673b0deeed742
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700277"
---
# <span data-ttu-id="5e73c-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5e73c-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="5e73c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e73c-102">SYNOPSIS</span></span>
<span data-ttu-id="5e73c-103">서비스 끝점 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e73c-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="5e73c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5e73c-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e73c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5e73c-105">DESCRIPTION</span></span>
<span data-ttu-id="5e73c-106">**새 AzServiceEndpointPolicy** cmdlet은 서비스 끝점 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e73c-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="5e73c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5e73c-107">EXAMPLES</span></span>

### <span data-ttu-id="5e73c-108">예제 1: 서비스 끝점 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="5e73c-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="5e73c-109">이 명령은 개체 $serviceEndpointDefinition 정의 하는 정의를 사용 하 여 Policy1 라는 서비스 끝점 정책을 만들고이를 $serviceEndpointPolicy 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e73c-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="5e73c-110">변수</span><span class="sxs-lookup"><span data-stu-id="5e73c-110">PARAMETERS</span></span>

### <span data-ttu-id="5e73c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e73c-111">-DefaultProfile</span></span>
<span data-ttu-id="5e73c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5e73c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e73c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5e73c-113">-Force</span></span>
<span data-ttu-id="5e73c-114">리소스를 overrite 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="5e73c-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="5e73c-115">-위치</span><span class="sxs-lookup"><span data-stu-id="5e73c-115">-Location</span></span>
<span data-ttu-id="5e73c-116">location.</span><span class="sxs-lookup"><span data-stu-id="5e73c-116">location.</span></span>

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

### <span data-ttu-id="5e73c-117">-이름</span><span class="sxs-lookup"><span data-stu-id="5e73c-117">-Name</span></span>
<span data-ttu-id="5e73c-118">서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e73c-118">The name of the subnet</span></span>

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

### <span data-ttu-id="5e73c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e73c-119">-ResourceGroupName</span></span>
<span data-ttu-id="5e73c-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e73c-120">The resource group name.</span></span>

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

### <span data-ttu-id="5e73c-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5e73c-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="5e73c-122">서비스 끝점 정의 목록</span><span class="sxs-lookup"><span data-stu-id="5e73c-122">List of service endpoint definitions</span></span>

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

### <span data-ttu-id="5e73c-123">-확인</span><span class="sxs-lookup"><span data-stu-id="5e73c-123">-Confirm</span></span>
<span data-ttu-id="5e73c-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e73c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e73c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e73c-125">-WhatIf</span></span>
<span data-ttu-id="5e73c-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5e73c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e73c-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e73c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e73c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e73c-128">CommonParameters</span></span>
<span data-ttu-id="5e73c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e73c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e73c-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e73c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e73c-131">입력</span><span class="sxs-lookup"><span data-stu-id="5e73c-131">INPUTS</span></span>

### <span data-ttu-id="5e73c-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5e73c-132">System.String</span></span>

## <span data-ttu-id="5e73c-133">출력</span><span class="sxs-lookup"><span data-stu-id="5e73c-133">OUTPUTS</span></span>

### <span data-ttu-id="5e73c-134">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5e73c-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="5e73c-135">상속자</span><span class="sxs-lookup"><span data-stu-id="5e73c-135">NOTES</span></span>

## <span data-ttu-id="5e73c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e73c-136">RELATED LINKS</span></span>

[<span data-ttu-id="5e73c-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5e73c-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="5e73c-138">제거-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5e73c-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="5e73c-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5e73c-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
