---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
ms.openlocfilehash: 742fe2795f16ed0a626e071520977ead66a491f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531169"
---
# <span data-ttu-id="42c83-101">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="42c83-101">Start-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="42c83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42c83-102">SYNOPSIS</span></span>
<span data-ttu-id="42c83-103">CDN 끝점을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c83-103">Starts a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42c83-104">구문과</span><span class="sxs-lookup"><span data-stu-id="42c83-104">SYNTAX</span></span>

### <span data-ttu-id="42c83-105">필드 매개 변수에 대해 설정 되는 매개 변수 (기본값)</span><span class="sxs-lookup"><span data-stu-id="42c83-105">Parameter Set for fields parameters (Default)</span></span>
```
Start-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42c83-106">개체 매개 변수에 대해 설정 되는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="42c83-106">Parameter Set for object parameters</span></span>
```
Start-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42c83-107">설명은</span><span class="sxs-lookup"><span data-stu-id="42c83-107">DESCRIPTION</span></span>
<span data-ttu-id="42c83-108">**AzureRmCdnEndpoint** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 끝점을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c83-108">The **Start-AzureRmCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="42c83-109">예제의</span><span class="sxs-lookup"><span data-stu-id="42c83-109">EXAMPLES</span></span>

## <span data-ttu-id="42c83-110">변수</span><span class="sxs-lookup"><span data-stu-id="42c83-110">PARAMETERS</span></span>

### <span data-ttu-id="42c83-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="42c83-111">-CdnEndpoint</span></span>
<span data-ttu-id="42c83-112">이 cmdlet이 시작 되는 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c83-112">Specifies the endpoint that this cmdlet starts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42c83-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="42c83-113">-EndpointName</span></span>
<span data-ttu-id="42c83-114">이 cmdlet이 시작 되는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c83-114">Specifies the name of the endpoint that this cmdlet starts.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c83-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42c83-115">-PassThru</span></span>
<span data-ttu-id="42c83-116">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c83-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="42c83-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42c83-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="42c83-118">-/Profile</span><span class="sxs-lookup"><span data-stu-id="42c83-118">-ProfileName</span></span>
<span data-ttu-id="42c83-119">종점이 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c83-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c83-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42c83-120">-ResourceGroupName</span></span>
<span data-ttu-id="42c83-121">끝점이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c83-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c83-122">-확인</span><span class="sxs-lookup"><span data-stu-id="42c83-122">-Confirm</span></span>
<span data-ttu-id="42c83-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c83-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42c83-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42c83-124">-WhatIf</span></span>
<span data-ttu-id="42c83-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="42c83-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42c83-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42c83-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42c83-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c83-127">-DefaultProfile</span></span>
<span data-ttu-id="42c83-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42c83-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42c83-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c83-129">CommonParameters</span></span>
<span data-ttu-id="42c83-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c83-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c83-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42c83-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c83-132">입력</span><span class="sxs-lookup"><span data-stu-id="42c83-132">INPUTS</span></span>

### <span data-ttu-id="42c83-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="42c83-133">PSEndpoint</span></span>
<span data-ttu-id="42c83-134">' CdnEndpoint ' 매개 변수는 파이프라인에서 ' PSEndpoint ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c83-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="42c83-135">출력</span><span class="sxs-lookup"><span data-stu-id="42c83-135">OUTPUTS</span></span>

### <span data-ttu-id="42c83-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="42c83-136">System.Boolean</span></span>

## <span data-ttu-id="42c83-137">상속자</span><span class="sxs-lookup"><span data-stu-id="42c83-137">NOTES</span></span>

## <span data-ttu-id="42c83-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42c83-138">RELATED LINKS</span></span>

[<span data-ttu-id="42c83-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="42c83-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="42c83-140">새로운 AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="42c83-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="42c83-141">제거-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="42c83-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="42c83-142">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="42c83-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="42c83-143">중지-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="42c83-143">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


