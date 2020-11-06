---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/stop-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 508465250489f2bcd0b031627258f11370fccfa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526996"
---
# <span data-ttu-id="6f57d-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f57d-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="6f57d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f57d-102">SYNOPSIS</span></span>
<span data-ttu-id="6f57d-103">CDN 끝점을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f57d-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f57d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f57d-104">SYNTAX</span></span>

### <span data-ttu-id="6f57d-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6f57d-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f57d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f57d-106">ByObjectParameterSet</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f57d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6f57d-107">DESCRIPTION</span></span>
<span data-ttu-id="6f57d-108">**AzureRmCdnEndpoint** Cmdlet은 Azure CDN (Content Delivery Network) 끝점을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f57d-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="6f57d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6f57d-109">EXAMPLES</span></span>

## <span data-ttu-id="6f57d-110">변수</span><span class="sxs-lookup"><span data-stu-id="6f57d-110">PARAMETERS</span></span>

### <span data-ttu-id="6f57d-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f57d-111">-CdnEndpoint</span></span>
<span data-ttu-id="6f57d-112">이 cmdlet이 중지 하는 끝점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f57d-112">Specifies the endpoint object that this cmdlet stops.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f57d-113">-DefaultProfile</span></span>
<span data-ttu-id="6f57d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6f57d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6f57d-115">-EndpointName</span></span>
<span data-ttu-id="6f57d-116">이 cmdlet이 중지 하는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f57d-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f57d-117">-PassThru</span></span>
<span data-ttu-id="6f57d-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f57d-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6f57d-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f57d-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-120">-/Profile</span><span class="sxs-lookup"><span data-stu-id="6f57d-120">-ProfileName</span></span>
<span data-ttu-id="6f57d-121">종점이 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f57d-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f57d-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f57d-123">끝점이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f57d-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-124">-확인</span><span class="sxs-lookup"><span data-stu-id="6f57d-124">-Confirm</span></span>
<span data-ttu-id="6f57d-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f57d-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f57d-126">-WhatIf</span></span>
<span data-ttu-id="6f57d-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f57d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f57d-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f57d-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f57d-129">CommonParameters</span></span>
<span data-ttu-id="6f57d-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f57d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f57d-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f57d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f57d-132">입력</span><span class="sxs-lookup"><span data-stu-id="6f57d-132">INPUTS</span></span>

### <span data-ttu-id="6f57d-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f57d-133">PSEndpoint</span></span>
<span data-ttu-id="6f57d-134">' CdnEndpoint ' 매개 변수는 파이프라인에서 ' PSEndpoint ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f57d-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="6f57d-135">출력</span><span class="sxs-lookup"><span data-stu-id="6f57d-135">OUTPUTS</span></span>

### <span data-ttu-id="6f57d-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6f57d-136">System.Boolean</span></span>

## <span data-ttu-id="6f57d-137">상속자</span><span class="sxs-lookup"><span data-stu-id="6f57d-137">NOTES</span></span>

## <span data-ttu-id="6f57d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f57d-138">RELATED LINKS</span></span>

[<span data-ttu-id="6f57d-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f57d-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="6f57d-140">새로운 AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f57d-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="6f57d-141">제거-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f57d-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="6f57d-142">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f57d-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="6f57d-143">시작-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f57d-143">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


