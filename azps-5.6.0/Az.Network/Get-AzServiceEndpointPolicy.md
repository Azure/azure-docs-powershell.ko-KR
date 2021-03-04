---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: eac0d67e2c9ffc77d9387eeb599ad624ac01fbbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006283"
---
# <span data-ttu-id="a147a-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a147a-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="a147a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a147a-102">SYNOPSIS</span></span>
<span data-ttu-id="a147a-103">서비스 엔드포인트 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a147a-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="a147a-104">구문</span><span class="sxs-lookup"><span data-stu-id="a147a-104">SYNTAX</span></span>

### <span data-ttu-id="a147a-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a147a-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a147a-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a147a-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a147a-107">설명</span><span class="sxs-lookup"><span data-stu-id="a147a-107">DESCRIPTION</span></span>
<span data-ttu-id="a147a-108">**Get-AzServiceEndpointPolicy** cmdlet은 서비스 엔드포인트 정책을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a147a-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="a147a-109">예제</span><span class="sxs-lookup"><span data-stu-id="a147a-109">EXAMPLES</span></span>

### <span data-ttu-id="a147a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a147a-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a147a-111">이 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ServiceEndpointPolicy1이라는 서비스 엔드포인트 정책을 얻게 $policy 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a147a-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="a147a-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="a147a-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a147a-113">이 명령은 ResourceGroup01이라는 리소스 그룹의 모든 서비스 엔드포인트 정책 목록을 얻게 $policyList 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a147a-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="a147a-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="a147a-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="a147a-115">이 명령은 "ServiceEndpointPolicy"로 시작하는 모든 서비스 엔드포인트 정책 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a147a-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="a147a-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a147a-116">PARAMETERS</span></span>

### <span data-ttu-id="a147a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a147a-117">-DefaultProfile</span></span>
<span data-ttu-id="a147a-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a147a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a147a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a147a-119">-Name</span></span>
<span data-ttu-id="a147a-120">서비스 엔드포인트 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="a147a-120">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="a147a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a147a-121">-ResourceGroupName</span></span>
<span data-ttu-id="a147a-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a147a-122">The resource group name.</span></span>

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

### <span data-ttu-id="a147a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a147a-123">-ResourceId</span></span>
<span data-ttu-id="a147a-124">서비스 엔드포인트 정책의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a147a-124">The ID of the service endpoint policy.</span></span>

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

### <span data-ttu-id="a147a-125">-확인</span><span class="sxs-lookup"><span data-stu-id="a147a-125">-Confirm</span></span>
<span data-ttu-id="a147a-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a147a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a147a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a147a-127">-WhatIf</span></span>
<span data-ttu-id="a147a-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a147a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a147a-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a147a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a147a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a147a-130">CommonParameters</span></span>
<span data-ttu-id="a147a-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a147a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a147a-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a147a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a147a-133">입력</span><span class="sxs-lookup"><span data-stu-id="a147a-133">INPUTS</span></span>

### <span data-ttu-id="a147a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a147a-134">System.String</span></span>

## <span data-ttu-id="a147a-135">출력</span><span class="sxs-lookup"><span data-stu-id="a147a-135">OUTPUTS</span></span>

### <span data-ttu-id="a147a-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a147a-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="a147a-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a147a-137">NOTES</span></span>

## <span data-ttu-id="a147a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a147a-138">RELATED LINKS</span></span>

[<span data-ttu-id="a147a-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a147a-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="a147a-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a147a-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="a147a-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a147a-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
