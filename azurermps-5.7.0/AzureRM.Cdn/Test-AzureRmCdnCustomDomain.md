---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/test-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 93f2013612a872288f95fba2cbf577002c7a9ace
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531120"
---
# <span data-ttu-id="9b777-101">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="9b777-101">Test-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="9b777-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b777-102">SYNOPSIS</span></span>
<span data-ttu-id="9b777-103">사용자 지정 도메인을 끝점에 추가할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b777-103">Checks whether a custom domain can be added to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b777-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b777-104">SYNTAX</span></span>

### <span data-ttu-id="9b777-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9b777-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzureRmCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b777-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b777-106">ByObjectParameterSet</span></span>
```
Test-AzureRmCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b777-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9b777-107">DESCRIPTION</span></span>
<span data-ttu-id="9b777-108">**테스트 AzureRmCdnCustomDomain** Cmdlet은 CName 매핑의 유효성을 검사 하 여 사용자 지정 도메인을 끝점에 추가할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b777-108">The **Test-AzureRmCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="9b777-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9b777-109">EXAMPLES</span></span>

## <span data-ttu-id="9b777-110">변수</span><span class="sxs-lookup"><span data-stu-id="9b777-110">PARAMETERS</span></span>

### <span data-ttu-id="9b777-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9b777-111">-CdnEndpoint</span></span>
<span data-ttu-id="9b777-112">사용자 지정 도메인을 추가 하려는 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b777-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="9b777-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="9b777-113">-CustomDomainHostName</span></span>
<span data-ttu-id="9b777-114">사용자 지정 도메인의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b777-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="9b777-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b777-115">-DefaultProfile</span></span>
<span data-ttu-id="9b777-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9b777-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b777-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9b777-117">-EndpointName</span></span>
<span data-ttu-id="9b777-118">사용자 지정 도메인을 추가 하려는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b777-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="9b777-119">-/Profile</span><span class="sxs-lookup"><span data-stu-id="9b777-119">-ProfileName</span></span>
<span data-ttu-id="9b777-120">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b777-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="9b777-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b777-121">-ResourceGroupName</span></span>
<span data-ttu-id="9b777-122">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b777-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9b777-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b777-123">CommonParameters</span></span>
<span data-ttu-id="9b777-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b777-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b777-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b777-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b777-126">입력</span><span class="sxs-lookup"><span data-stu-id="9b777-126">INPUTS</span></span>

### <span data-ttu-id="9b777-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="9b777-127">PSEndpoint</span></span>
<span data-ttu-id="9b777-128">' CdnEndpoint ' 매개 변수는 파이프라인에서 ' PSEndpoint ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b777-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="9b777-129">출력</span><span class="sxs-lookup"><span data-stu-id="9b777-129">OUTPUTS</span></span>

### <span data-ttu-id="9b777-130">PSValidateCustomDomainOutput를 통해 끝점을 보세요.</span><span class="sxs-lookup"><span data-stu-id="9b777-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="9b777-131">상속자</span><span class="sxs-lookup"><span data-stu-id="9b777-131">NOTES</span></span>

## <span data-ttu-id="9b777-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b777-132">RELATED LINKS</span></span>

[<span data-ttu-id="9b777-133">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="9b777-133">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="9b777-134">새로운 AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="9b777-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="9b777-135">제거-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="9b777-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


