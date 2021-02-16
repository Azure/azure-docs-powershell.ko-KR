---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 85fc0f0687ed3b32492f42f753f67ba1e85a4656
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177860"
---
# <span data-ttu-id="df7f4-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="df7f4-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="df7f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df7f4-102">SYNOPSIS</span></span>
<span data-ttu-id="df7f4-103">CDN 엔드포인트를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f4-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="df7f4-104">구문</span><span class="sxs-lookup"><span data-stu-id="df7f4-104">SYNTAX</span></span>

### <span data-ttu-id="df7f4-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="df7f4-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df7f4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df7f4-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df7f4-107">설명</span><span class="sxs-lookup"><span data-stu-id="df7f4-107">DESCRIPTION</span></span>
<span data-ttu-id="df7f4-108">**Start-AzCdnEndpoint** cmdlet은 Azure CDN(Content Delivery Network) 엔드포인트를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f4-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="df7f4-109">예제</span><span class="sxs-lookup"><span data-stu-id="df7f4-109">EXAMPLES</span></span>

## <span data-ttu-id="df7f4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df7f4-110">PARAMETERS</span></span>

### <span data-ttu-id="df7f4-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="df7f4-111">-CdnEndpoint</span></span>
<span data-ttu-id="df7f4-112">이 cmdlet이 시작하는 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f4-112">Specifies the endpoint that this cmdlet starts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df7f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df7f4-113">-DefaultProfile</span></span>
<span data-ttu-id="df7f4-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="df7f4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df7f4-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="df7f4-115">-EndpointName</span></span>
<span data-ttu-id="df7f4-116">이 cmdlet이 시작하는 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f4-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df7f4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df7f4-117">-PassThru</span></span>
<span data-ttu-id="df7f4-118">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f4-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="df7f4-119">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df7f4-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df7f4-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="df7f4-120">-ProfileName</span></span>
<span data-ttu-id="df7f4-121">엔드포인트가 속한 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f4-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df7f4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df7f4-122">-ResourceGroupName</span></span>
<span data-ttu-id="df7f4-123">엔드포인트가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f4-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df7f4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df7f4-124">-Confirm</span></span>
<span data-ttu-id="df7f4-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="df7f4-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df7f4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df7f4-126">-WhatIf</span></span>
<span data-ttu-id="df7f4-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="df7f4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df7f4-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df7f4-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df7f4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7f4-129">CommonParameters</span></span>
<span data-ttu-id="df7f4-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df7f4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7f4-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="df7f4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7f4-132">입력</span><span class="sxs-lookup"><span data-stu-id="df7f4-132">INPUTS</span></span>

### <span data-ttu-id="df7f4-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="df7f4-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="df7f4-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="df7f4-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="df7f4-135">출력</span><span class="sxs-lookup"><span data-stu-id="df7f4-135">OUTPUTS</span></span>

### <span data-ttu-id="df7f4-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="df7f4-136">System.Boolean</span></span>

## <span data-ttu-id="df7f4-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="df7f4-137">NOTES</span></span>

## <span data-ttu-id="df7f4-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df7f4-138">RELATED LINKS</span></span>

[<span data-ttu-id="df7f4-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="df7f4-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="df7f4-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="df7f4-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="df7f4-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="df7f4-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="df7f4-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="df7f4-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="df7f4-143">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="df7f4-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


