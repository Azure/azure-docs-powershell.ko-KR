---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/stop-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
ms.openlocfilehash: a606bbcb630ab4868e64221b9bcaa8f471327977
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869201"
---
# <span data-ttu-id="d3877-101">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3877-101">Stop-AzCdnEndpoint</span></span>

## <span data-ttu-id="d3877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3877-102">SYNOPSIS</span></span>
<span data-ttu-id="d3877-103">CDN 끝점을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3877-103">Stops the CDN endpoint.</span></span>

## <span data-ttu-id="d3877-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3877-104">SYNTAX</span></span>

### <span data-ttu-id="d3877-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d3877-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3877-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3877-106">ByObjectParameterSet</span></span>
```
Stop-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3877-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d3877-107">DESCRIPTION</span></span>
<span data-ttu-id="d3877-108">**AzCdnEndpoint** Cmdlet은 Azure CDN (Content Delivery Network) 끝점을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3877-108">The **Stop-AzCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="d3877-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d3877-109">EXAMPLES</span></span>

## <span data-ttu-id="d3877-110">변수</span><span class="sxs-lookup"><span data-stu-id="d3877-110">PARAMETERS</span></span>

### <span data-ttu-id="d3877-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3877-111">-CdnEndpoint</span></span>
<span data-ttu-id="d3877-112">이 cmdlet이 중지 하는 끝점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3877-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d3877-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3877-113">-DefaultProfile</span></span>
<span data-ttu-id="d3877-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d3877-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3877-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d3877-115">-EndpointName</span></span>
<span data-ttu-id="d3877-116">이 cmdlet이 중지 하는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3877-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d3877-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3877-117">-PassThru</span></span>
<span data-ttu-id="d3877-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3877-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d3877-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3877-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d3877-120">-/Profile</span><span class="sxs-lookup"><span data-stu-id="d3877-120">-ProfileName</span></span>
<span data-ttu-id="d3877-121">종점이 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3877-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="d3877-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3877-122">-ResourceGroupName</span></span>
<span data-ttu-id="d3877-123">끝점이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3877-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="d3877-124">-확인</span><span class="sxs-lookup"><span data-stu-id="d3877-124">-Confirm</span></span>
<span data-ttu-id="d3877-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3877-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3877-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3877-126">-WhatIf</span></span>
<span data-ttu-id="d3877-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3877-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3877-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3877-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3877-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3877-129">CommonParameters</span></span>
<span data-ttu-id="d3877-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3877-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3877-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3877-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3877-132">입력</span><span class="sxs-lookup"><span data-stu-id="d3877-132">INPUTS</span></span>

### <span data-ttu-id="d3877-133">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3877-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="d3877-134">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d3877-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d3877-135">출력</span><span class="sxs-lookup"><span data-stu-id="d3877-135">OUTPUTS</span></span>

### <span data-ttu-id="d3877-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d3877-136">System.Boolean</span></span>

## <span data-ttu-id="d3877-137">상속자</span><span class="sxs-lookup"><span data-stu-id="d3877-137">NOTES</span></span>

## <span data-ttu-id="d3877-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3877-138">RELATED LINKS</span></span>

[<span data-ttu-id="d3877-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3877-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="d3877-140">새로운 AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3877-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="d3877-141">제거-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3877-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="d3877-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3877-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="d3877-143">시작-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3877-143">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)


