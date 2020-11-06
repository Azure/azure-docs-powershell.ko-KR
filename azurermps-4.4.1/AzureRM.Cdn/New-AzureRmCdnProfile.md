---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: 0e69e48d29c96163acbb82ffe691de6affe8d131
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533144"
---
# <span data-ttu-id="ade17-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ade17-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="ade17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ade17-102">SYNOPSIS</span></span>
<span data-ttu-id="ade17-103">CDN 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ade17-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ade17-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ade17-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ade17-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ade17-105">DESCRIPTION</span></span>
<span data-ttu-id="ade17-106">**AzureRmCdnProfile** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ade17-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="ade17-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ade17-107">EXAMPLES</span></span>

## <span data-ttu-id="ade17-108">변수</span><span class="sxs-lookup"><span data-stu-id="ade17-108">PARAMETERS</span></span>

### <span data-ttu-id="ade17-109">-위치</span><span class="sxs-lookup"><span data-stu-id="ade17-109">-Location</span></span>
<span data-ttu-id="ade17-110">프로필의 리소스 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade17-110">Specifies the resource location of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade17-111">-/Profile</span><span class="sxs-lookup"><span data-stu-id="ade17-111">-ProfileName</span></span>
<span data-ttu-id="ade17-112">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade17-112">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade17-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade17-113">-ResourceGroupName</span></span>
<span data-ttu-id="ade17-114">프로필이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade17-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade17-115">-Sku</span><span class="sxs-lookup"><span data-stu-id="ade17-115">-Sku</span></span>
<span data-ttu-id="ade17-116">프로필의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade17-116">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade17-117">태그</span><span class="sxs-lookup"><span data-stu-id="ade17-117">-Tags</span></span>
<span data-ttu-id="ade17-118">이 프로필에 연결 된 태그의 해시 테이블을 Sepcifies 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade17-118">Sepcifies a hash table of tags that are associated with this profile.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade17-119">-확인</span><span class="sxs-lookup"><span data-stu-id="ade17-119">-Confirm</span></span>
<span data-ttu-id="ade17-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade17-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ade17-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ade17-121">-WhatIf</span></span>
<span data-ttu-id="ade17-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ade17-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ade17-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ade17-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ade17-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade17-124">-DefaultProfile</span></span>
<span data-ttu-id="ade17-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ade17-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ade17-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade17-126">CommonParameters</span></span>
<span data-ttu-id="ade17-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ade17-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade17-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ade17-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade17-129">입력</span><span class="sxs-lookup"><span data-stu-id="ade17-129">INPUTS</span></span>

## <span data-ttu-id="ade17-130">출력</span><span class="sxs-lookup"><span data-stu-id="ade17-130">OUTPUTS</span></span>

### <span data-ttu-id="ade17-131">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="ade17-131">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="ade17-132">상속자</span><span class="sxs-lookup"><span data-stu-id="ade17-132">NOTES</span></span>

## <span data-ttu-id="ade17-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ade17-133">RELATED LINKS</span></span>

[<span data-ttu-id="ade17-134">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ade17-134">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="ade17-135">제거-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ade17-135">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="ade17-136">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ade17-136">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


