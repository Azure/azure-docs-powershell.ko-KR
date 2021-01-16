---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 85fc0f0687ed3b32492f42f753f67ba1e85a4656
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349010"
---
# <span data-ttu-id="af7be-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="af7be-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="af7be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af7be-102">SYNOPSIS</span></span>
<span data-ttu-id="af7be-103">CDN 엔드포인트를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="af7be-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="af7be-104">구문</span><span class="sxs-lookup"><span data-stu-id="af7be-104">SYNTAX</span></span>

### <span data-ttu-id="af7be-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="af7be-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af7be-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af7be-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af7be-107">설명</span><span class="sxs-lookup"><span data-stu-id="af7be-107">DESCRIPTION</span></span>
<span data-ttu-id="af7be-108">**Start-AzCdnEndpoint** cmdlet은 Azure CDN(Content Delivery Network) 엔드포인트를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="af7be-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="af7be-109">예제</span><span class="sxs-lookup"><span data-stu-id="af7be-109">EXAMPLES</span></span>

## <span data-ttu-id="af7be-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af7be-110">PARAMETERS</span></span>

### <span data-ttu-id="af7be-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="af7be-111">-CdnEndpoint</span></span>
<span data-ttu-id="af7be-112">이 cmdlet이 시작하는 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af7be-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="af7be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af7be-113">-DefaultProfile</span></span>
<span data-ttu-id="af7be-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="af7be-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af7be-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="af7be-115">-EndpointName</span></span>
<span data-ttu-id="af7be-116">이 cmdlet이 시작하는 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af7be-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="af7be-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af7be-117">-PassThru</span></span>
<span data-ttu-id="af7be-118">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="af7be-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="af7be-119">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af7be-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="af7be-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="af7be-120">-ProfileName</span></span>
<span data-ttu-id="af7be-121">엔드포인트가 속한 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af7be-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="af7be-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af7be-122">-ResourceGroupName</span></span>
<span data-ttu-id="af7be-123">엔드포인트가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af7be-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="af7be-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af7be-124">-Confirm</span></span>
<span data-ttu-id="af7be-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="af7be-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af7be-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af7be-126">-WhatIf</span></span>
<span data-ttu-id="af7be-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="af7be-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af7be-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af7be-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af7be-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7be-129">CommonParameters</span></span>
<span data-ttu-id="af7be-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="af7be-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7be-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="af7be-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7be-132">입력</span><span class="sxs-lookup"><span data-stu-id="af7be-132">INPUTS</span></span>

### <span data-ttu-id="af7be-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="af7be-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="af7be-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="af7be-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="af7be-135">출력</span><span class="sxs-lookup"><span data-stu-id="af7be-135">OUTPUTS</span></span>

### <span data-ttu-id="af7be-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="af7be-136">System.Boolean</span></span>

## <span data-ttu-id="af7be-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="af7be-137">NOTES</span></span>

## <span data-ttu-id="af7be-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af7be-138">RELATED LINKS</span></span>

[<span data-ttu-id="af7be-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="af7be-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="af7be-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="af7be-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="af7be-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="af7be-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="af7be-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="af7be-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="af7be-143">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="af7be-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


