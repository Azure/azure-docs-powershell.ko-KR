---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: a74edbec0051e3a77ab3ac10595f787dd45a2dfc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204516"
---
# <span data-ttu-id="ee6d9-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ee6d9-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="ee6d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee6d9-102">SYNOPSIS</span></span>
<span data-ttu-id="ee6d9-103">서비스 끝점 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="ee6d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee6d9-104">SYNTAX</span></span>

### <span data-ttu-id="ee6d9-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ee6d9-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee6d9-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee6d9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee6d9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ee6d9-107">DESCRIPTION</span></span>
<span data-ttu-id="ee6d9-108">**Get-AzServiceEndpointPolicy** cmdlet은 서비스 끝점 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="ee6d9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ee6d9-109">EXAMPLES</span></span>

### <span data-ttu-id="ee6d9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee6d9-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ee6d9-111">이 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ServiceEndpointPolicy1 이라는 이름의 서비스 끝점 정책을 가져오고이를 $policy 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="ee6d9-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="ee6d9-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ee6d9-113">이 명령은 ResourceGroup01 이라는 리소스 그룹에 있는 모든 서비스 끝점 정책의 목록을 가져와이를 $policyList 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="ee6d9-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="ee6d9-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="ee6d9-115">이 명령은 "ServiceEndpointPolicy"로 시작 하는 모든 서비스 끝점 정책의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="ee6d9-116">변수</span><span class="sxs-lookup"><span data-stu-id="ee6d9-116">PARAMETERS</span></span>

### <span data-ttu-id="ee6d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee6d9-117">-DefaultProfile</span></span>
<span data-ttu-id="ee6d9-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee6d9-119">-이름</span><span class="sxs-lookup"><span data-stu-id="ee6d9-119">-Name</span></span>
<span data-ttu-id="ee6d9-120">서비스 끝점 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-120">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="ee6d9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee6d9-121">-ResourceGroupName</span></span>
<span data-ttu-id="ee6d9-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ee6d9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee6d9-123">-ResourceId</span></span>
<span data-ttu-id="ee6d9-124">서비스 끝점 정책의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-124">The ID of the service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee6d9-125">-확인</span><span class="sxs-lookup"><span data-stu-id="ee6d9-125">-Confirm</span></span>
<span data-ttu-id="ee6d9-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee6d9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee6d9-127">-WhatIf</span></span>
<span data-ttu-id="ee6d9-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee6d9-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee6d9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee6d9-130">CommonParameters</span></span>
<span data-ttu-id="ee6d9-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee6d9-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee6d9-133">입력</span><span class="sxs-lookup"><span data-stu-id="ee6d9-133">INPUTS</span></span>

### <span data-ttu-id="ee6d9-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ee6d9-134">System.String</span></span>

## <span data-ttu-id="ee6d9-135">출력</span><span class="sxs-lookup"><span data-stu-id="ee6d9-135">OUTPUTS</span></span>

### <span data-ttu-id="ee6d9-136">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ee6d9-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="ee6d9-137">상속자</span><span class="sxs-lookup"><span data-stu-id="ee6d9-137">NOTES</span></span>

## <span data-ttu-id="ee6d9-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee6d9-138">RELATED LINKS</span></span>

[<span data-ttu-id="ee6d9-139">새로운 AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ee6d9-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="ee6d9-140">제거-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ee6d9-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="ee6d9-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ee6d9-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
