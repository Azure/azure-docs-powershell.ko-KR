---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: b4800b77441a82fc0e9966be16f91c9d81a2214a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702171"
---
# <span data-ttu-id="0d4a7-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="0d4a7-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="0d4a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d4a7-102">SYNOPSIS</span></span>
<span data-ttu-id="0d4a7-103">CDN 원본 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d4a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d4a7-104">SYNTAX</span></span>

### <span data-ttu-id="0d4a7-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0d4a7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d4a7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d4a7-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d4a7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0d4a7-107">DESCRIPTION</span></span>
<span data-ttu-id="0d4a7-108">**AzureRmCdnOrigin** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 원본 서버와 해당 구성 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="0d4a7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0d4a7-109">EXAMPLES</span></span>

## <span data-ttu-id="0d4a7-110">변수</span><span class="sxs-lookup"><span data-stu-id="0d4a7-110">PARAMETERS</span></span>

### <span data-ttu-id="0d4a7-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d4a7-111">-CdnEndpoint</span></span>
<span data-ttu-id="0d4a7-112">원점이 속한 CDN 끝점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="0d4a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d4a7-113">-DefaultProfile</span></span>
<span data-ttu-id="0d4a7-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0d4a7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d4a7-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0d4a7-115">-EndpointName</span></span>
<span data-ttu-id="0d4a7-116">원본 서버가 속한 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="0d4a7-117">-OriginName</span><span class="sxs-lookup"><span data-stu-id="0d4a7-117">-OriginName</span></span>
<span data-ttu-id="0d4a7-118">원본 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-118">Specifies the name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4a7-119">-/Profile</span><span class="sxs-lookup"><span data-stu-id="0d4a7-119">-ProfileName</span></span>
<span data-ttu-id="0d4a7-120">원본 서버가 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="0d4a7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d4a7-121">-ResourceGroupName</span></span>
<span data-ttu-id="0d4a7-122">원본 서버가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="0d4a7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d4a7-123">CommonParameters</span></span>
<span data-ttu-id="0d4a7-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d4a7-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d4a7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d4a7-126">입력</span><span class="sxs-lookup"><span data-stu-id="0d4a7-126">INPUTS</span></span>

### <span data-ttu-id="0d4a7-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d4a7-127">PSEndpoint</span></span>
<span data-ttu-id="0d4a7-128">' CdnEndpoint ' 매개 변수는 파이프라인에서 ' PSEndpoint ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="0d4a7-129">출력</span><span class="sxs-lookup"><span data-stu-id="0d4a7-129">OUTPUTS</span></span>

###  
<span data-ttu-id="0d4a7-130">이 cmdlet은 원본 서버 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d4a7-130">This cmdlet returns an origin server object.</span></span>

## <span data-ttu-id="0d4a7-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0d4a7-131">NOTES</span></span>

## <span data-ttu-id="0d4a7-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d4a7-132">RELATED LINKS</span></span>

[<span data-ttu-id="0d4a7-133">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="0d4a7-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


