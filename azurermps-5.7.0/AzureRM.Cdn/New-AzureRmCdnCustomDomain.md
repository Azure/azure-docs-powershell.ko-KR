---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 2788c135f7c93d0ca2f3a8dbb17228e4118625c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527015"
---
# <span data-ttu-id="022af-101">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="022af-101">New-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="022af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="022af-102">SYNOPSIS</span></span>
<span data-ttu-id="022af-103">CDN 끝점에 대 한 사용자 지정 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="022af-103">Creates a custom domain for a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="022af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="022af-104">SYNTAX</span></span>

### <span data-ttu-id="022af-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="022af-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="022af-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="022af-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="022af-107">설명은</span><span class="sxs-lookup"><span data-stu-id="022af-107">DESCRIPTION</span></span>
<span data-ttu-id="022af-108">**AzureRmCdnCustomDomain** CMDLET은 CDN (Content Delivery Network) 끝점에 대 한 사용자 지정 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="022af-108">The **New-AzureRmCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="022af-109">예제의</span><span class="sxs-lookup"><span data-stu-id="022af-109">EXAMPLES</span></span>

## <span data-ttu-id="022af-110">변수</span><span class="sxs-lookup"><span data-stu-id="022af-110">PARAMETERS</span></span>

### <span data-ttu-id="022af-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="022af-111">-CdnEndpoint</span></span>
<span data-ttu-id="022af-112">사용자 지정 도메인이 추가 되는 CDN 끝점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="022af-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="022af-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="022af-113">-CustomDomainName</span></span>
<span data-ttu-id="022af-114">사용자 지정 도메인의 리소스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="022af-114">Specifies the resource name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="022af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="022af-115">-DefaultProfile</span></span>
<span data-ttu-id="022af-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="022af-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="022af-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="022af-117">-EndpointName</span></span>
<span data-ttu-id="022af-118">끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="022af-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="022af-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="022af-119">-HostName</span></span>
<span data-ttu-id="022af-120">사용자 지정 도메인의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="022af-120">Specifies the host name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="022af-121">-/Profile</span><span class="sxs-lookup"><span data-stu-id="022af-121">-ProfileName</span></span>
<span data-ttu-id="022af-122">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="022af-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="022af-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="022af-123">-ResourceGroupName</span></span>
<span data-ttu-id="022af-124">사용자 지정 도메인이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="022af-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="022af-125">-확인</span><span class="sxs-lookup"><span data-stu-id="022af-125">-Confirm</span></span>
<span data-ttu-id="022af-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="022af-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="022af-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="022af-127">-WhatIf</span></span>
<span data-ttu-id="022af-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="022af-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="022af-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="022af-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="022af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="022af-130">CommonParameters</span></span>
<span data-ttu-id="022af-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="022af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="022af-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="022af-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="022af-133">입력</span><span class="sxs-lookup"><span data-stu-id="022af-133">INPUTS</span></span>

### <span data-ttu-id="022af-134">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="022af-134">PSEndpoint</span></span>
<span data-ttu-id="022af-135">' CdnEndpoint ' 매개 변수는 파이프라인에서 ' PSEndpoint ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="022af-135">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="022af-136">출력</span><span class="sxs-lookup"><span data-stu-id="022af-136">OUTPUTS</span></span>

### <span data-ttu-id="022af-137">PSCustomDomain (.). c.</span><span class="sxs-lookup"><span data-stu-id="022af-137">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="022af-138">상속자</span><span class="sxs-lookup"><span data-stu-id="022af-138">NOTES</span></span>

## <span data-ttu-id="022af-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="022af-139">RELATED LINKS</span></span>

[<span data-ttu-id="022af-140">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="022af-140">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="022af-141">제거-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="022af-141">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="022af-142">테스트-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="022af-142">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


