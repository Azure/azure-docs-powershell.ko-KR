---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: aba554d2c81e4fce438e9bd6e10a8dfec63da465
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537875"
---
# <span data-ttu-id="b97ba-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b97ba-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="b97ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b97ba-102">SYNOPSIS</span></span>
<span data-ttu-id="b97ba-103">CDN 원본 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b97ba-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b97ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b97ba-104">SYNTAX</span></span>

### <span data-ttu-id="b97ba-105">필드 매개 변수에 대해 설정 되는 매개 변수 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b97ba-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b97ba-106">개체 매개 변수에 대해 설정 되는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b97ba-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b97ba-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b97ba-107">DESCRIPTION</span></span>
<span data-ttu-id="b97ba-108">**AzureRmCdnOrigin** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 원본 서버와 해당 구성 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b97ba-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="b97ba-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b97ba-109">EXAMPLES</span></span>

## <span data-ttu-id="b97ba-110">변수</span><span class="sxs-lookup"><span data-stu-id="b97ba-110">PARAMETERS</span></span>

### <span data-ttu-id="b97ba-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b97ba-111">-CdnEndpoint</span></span>
<span data-ttu-id="b97ba-112">원점이 속한 CDN 끝점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b97ba-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="b97ba-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b97ba-113">-EndpointName</span></span>
<span data-ttu-id="b97ba-114">원본 서버가 속한 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b97ba-114">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="b97ba-115">-OriginName</span><span class="sxs-lookup"><span data-stu-id="b97ba-115">-OriginName</span></span>
<span data-ttu-id="b97ba-116">원본 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b97ba-116">Specifies the name of the origin server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b97ba-117">-/Profile</span><span class="sxs-lookup"><span data-stu-id="b97ba-117">-ProfileName</span></span>
<span data-ttu-id="b97ba-118">원본 서버가 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b97ba-118">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="b97ba-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b97ba-119">-ResourceGroupName</span></span>
<span data-ttu-id="b97ba-120">원본 서버가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b97ba-120">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="b97ba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b97ba-121">-DefaultProfile</span></span>
<span data-ttu-id="b97ba-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b97ba-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b97ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b97ba-123">CommonParameters</span></span>
<span data-ttu-id="b97ba-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b97ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b97ba-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b97ba-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b97ba-126">입력</span><span class="sxs-lookup"><span data-stu-id="b97ba-126">INPUTS</span></span>

### <span data-ttu-id="b97ba-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b97ba-127">PSEndpoint</span></span>
<span data-ttu-id="b97ba-128">' CdnEndpoint ' 매개 변수는 파이프라인에서 ' PSEndpoint ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b97ba-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="b97ba-129">출력</span><span class="sxs-lookup"><span data-stu-id="b97ba-129">OUTPUTS</span></span>

###  
<span data-ttu-id="b97ba-130">이 cmdlet은 원본 서버 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b97ba-130">This cmdlet returns an origin server object.</span></span>

## <span data-ttu-id="b97ba-131">상속자</span><span class="sxs-lookup"><span data-stu-id="b97ba-131">NOTES</span></span>

## <span data-ttu-id="b97ba-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b97ba-132">RELATED LINKS</span></span>

[<span data-ttu-id="b97ba-133">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b97ba-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


