---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/stop-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 20206ebf99d597a2961804bf3062cd4c049f8017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703471"
---
# <span data-ttu-id="bf5e6-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf5e6-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="bf5e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf5e6-102">SYNOPSIS</span></span>
<span data-ttu-id="bf5e6-103">CDN 끝점을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf5e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf5e6-104">SYNTAX</span></span>

### <span data-ttu-id="bf5e6-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bf5e6-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf5e6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf5e6-106">ByObjectParameterSet</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf5e6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bf5e6-107">DESCRIPTION</span></span>
<span data-ttu-id="bf5e6-108">**AzureRmCdnEndpoint** Cmdlet은 Azure CDN (Content Delivery Network) 끝점을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="bf5e6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bf5e6-109">EXAMPLES</span></span>

## <span data-ttu-id="bf5e6-110">변수</span><span class="sxs-lookup"><span data-stu-id="bf5e6-110">PARAMETERS</span></span>

### <span data-ttu-id="bf5e6-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf5e6-111">-CdnEndpoint</span></span>
<span data-ttu-id="bf5e6-112">이 cmdlet이 중지 하는 끝점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="bf5e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf5e6-113">-DefaultProfile</span></span>
<span data-ttu-id="bf5e6-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bf5e6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf5e6-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bf5e6-115">-EndpointName</span></span>
<span data-ttu-id="bf5e6-116">이 cmdlet이 중지 하는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="bf5e6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf5e6-117">-PassThru</span></span>
<span data-ttu-id="bf5e6-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bf5e6-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bf5e6-120">-/Profile</span><span class="sxs-lookup"><span data-stu-id="bf5e6-120">-ProfileName</span></span>
<span data-ttu-id="bf5e6-121">종점이 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="bf5e6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf5e6-122">-ResourceGroupName</span></span>
<span data-ttu-id="bf5e6-123">끝점이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="bf5e6-124">-확인</span><span class="sxs-lookup"><span data-stu-id="bf5e6-124">-Confirm</span></span>
<span data-ttu-id="bf5e6-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf5e6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf5e6-126">-WhatIf</span></span>
<span data-ttu-id="bf5e6-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf5e6-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf5e6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf5e6-129">CommonParameters</span></span>
<span data-ttu-id="bf5e6-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf5e6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf5e6-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf5e6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf5e6-132">입력</span><span class="sxs-lookup"><span data-stu-id="bf5e6-132">INPUTS</span></span>

### <span data-ttu-id="bf5e6-133">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf5e6-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="bf5e6-134">매개 변수: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bf5e6-134">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="bf5e6-135">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="bf5e6-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bf5e6-136">출력</span><span class="sxs-lookup"><span data-stu-id="bf5e6-136">OUTPUTS</span></span>

### <span data-ttu-id="bf5e6-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="bf5e6-137">System.Boolean</span></span>

## <span data-ttu-id="bf5e6-138">상속자</span><span class="sxs-lookup"><span data-stu-id="bf5e6-138">NOTES</span></span>

## <span data-ttu-id="bf5e6-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf5e6-139">RELATED LINKS</span></span>

[<span data-ttu-id="bf5e6-140">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf5e6-140">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="bf5e6-141">새로운 AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf5e6-141">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="bf5e6-142">제거-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf5e6-142">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="bf5e6-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf5e6-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="bf5e6-144">시작-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf5e6-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


