---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/stop-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
ms.openlocfilehash: e1afa87d1ab21222987a4eeecf68a3786934ef57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195148"
---
# <span data-ttu-id="0184d-101">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0184d-101">Stop-AzCdnEndpoint</span></span>

## <span data-ttu-id="0184d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0184d-102">SYNOPSIS</span></span>
<span data-ttu-id="0184d-103">CDN 엔드포인트를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="0184d-103">Stops the CDN endpoint.</span></span>

## <span data-ttu-id="0184d-104">구문</span><span class="sxs-lookup"><span data-stu-id="0184d-104">SYNTAX</span></span>

### <span data-ttu-id="0184d-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0184d-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0184d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0184d-106">ByObjectParameterSet</span></span>
```
Stop-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0184d-107">설명</span><span class="sxs-lookup"><span data-stu-id="0184d-107">DESCRIPTION</span></span>
<span data-ttu-id="0184d-108">**Stop-AzCdnEndpoint** cmdlet은 Azure CDN(Content Delivery Network) 엔드포인트를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="0184d-108">The **Stop-AzCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="0184d-109">예제</span><span class="sxs-lookup"><span data-stu-id="0184d-109">EXAMPLES</span></span>

## <span data-ttu-id="0184d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0184d-110">PARAMETERS</span></span>

### <span data-ttu-id="0184d-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0184d-111">-CdnEndpoint</span></span>
<span data-ttu-id="0184d-112">이 cmdlet이 중지하는 엔드포인트 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0184d-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="0184d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0184d-113">-DefaultProfile</span></span>
<span data-ttu-id="0184d-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0184d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0184d-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0184d-115">-EndpointName</span></span>
<span data-ttu-id="0184d-116">이 cmdlet이 중지하는 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0184d-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="0184d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0184d-117">-PassThru</span></span>
<span data-ttu-id="0184d-118">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0184d-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0184d-119">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0184d-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0184d-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0184d-120">-ProfileName</span></span>
<span data-ttu-id="0184d-121">엔드포인트가 속한 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0184d-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="0184d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0184d-122">-ResourceGroupName</span></span>
<span data-ttu-id="0184d-123">엔드포인트가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0184d-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="0184d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0184d-124">-Confirm</span></span>
<span data-ttu-id="0184d-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0184d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0184d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0184d-126">-WhatIf</span></span>
<span data-ttu-id="0184d-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0184d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0184d-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0184d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0184d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0184d-129">CommonParameters</span></span>
<span data-ttu-id="0184d-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0184d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0184d-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0184d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0184d-132">입력</span><span class="sxs-lookup"><span data-stu-id="0184d-132">INPUTS</span></span>

### <span data-ttu-id="0184d-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="0184d-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="0184d-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0184d-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0184d-135">출력</span><span class="sxs-lookup"><span data-stu-id="0184d-135">OUTPUTS</span></span>

### <span data-ttu-id="0184d-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0184d-136">System.Boolean</span></span>

## <span data-ttu-id="0184d-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0184d-137">NOTES</span></span>

## <span data-ttu-id="0184d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0184d-138">RELATED LINKS</span></span>

[<span data-ttu-id="0184d-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0184d-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="0184d-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0184d-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="0184d-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0184d-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="0184d-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0184d-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="0184d-143">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0184d-143">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)


