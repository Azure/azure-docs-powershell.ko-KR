---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: c64f84c9f41dba29e54b14a69235bccd764ea750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703470"
---
# <span data-ttu-id="33583-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="33583-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="33583-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33583-102">SYNOPSIS</span></span>
<span data-ttu-id="33583-103">CDN 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="33583-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33583-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33583-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33583-105">설명은</span><span class="sxs-lookup"><span data-stu-id="33583-105">DESCRIPTION</span></span>
<span data-ttu-id="33583-106">**AzureRmCdnProfile** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="33583-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="33583-107">예제의</span><span class="sxs-lookup"><span data-stu-id="33583-107">EXAMPLES</span></span>

## <span data-ttu-id="33583-108">변수</span><span class="sxs-lookup"><span data-stu-id="33583-108">PARAMETERS</span></span>

### <span data-ttu-id="33583-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33583-109">-DefaultProfile</span></span>
<span data-ttu-id="33583-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="33583-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33583-111">-위치</span><span class="sxs-lookup"><span data-stu-id="33583-111">-Location</span></span>
<span data-ttu-id="33583-112">프로필의 리소스 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33583-112">Specifies the resource location of the profile.</span></span>

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

### <span data-ttu-id="33583-113">-/Profile</span><span class="sxs-lookup"><span data-stu-id="33583-113">-ProfileName</span></span>
<span data-ttu-id="33583-114">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33583-114">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="33583-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33583-115">-ResourceGroupName</span></span>
<span data-ttu-id="33583-116">프로필이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33583-116">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="33583-117">-Sku</span><span class="sxs-lookup"><span data-stu-id="33583-117">-Sku</span></span>
<span data-ttu-id="33583-118">프로필의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33583-118">Specifies the SKU of the profile.</span></span>

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

### <span data-ttu-id="33583-119">태그</span><span class="sxs-lookup"><span data-stu-id="33583-119">-Tag</span></span>
<span data-ttu-id="33583-120">Azure CDN 프로필에 연결할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="33583-120">The tags to associate with the Azure CDN profile.</span></span>

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

### <span data-ttu-id="33583-121">-확인</span><span class="sxs-lookup"><span data-stu-id="33583-121">-Confirm</span></span>
<span data-ttu-id="33583-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="33583-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33583-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33583-123">-WhatIf</span></span>
<span data-ttu-id="33583-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="33583-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33583-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33583-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33583-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33583-126">CommonParameters</span></span>
<span data-ttu-id="33583-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33583-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33583-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33583-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33583-129">입력</span><span class="sxs-lookup"><span data-stu-id="33583-129">INPUTS</span></span>

### <span data-ttu-id="33583-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="33583-130">System.String</span></span>

## <span data-ttu-id="33583-131">출력</span><span class="sxs-lookup"><span data-stu-id="33583-131">OUTPUTS</span></span>

### <span data-ttu-id="33583-132">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="33583-132">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="33583-133">상속자</span><span class="sxs-lookup"><span data-stu-id="33583-133">NOTES</span></span>

## <span data-ttu-id="33583-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33583-134">RELATED LINKS</span></span>

[<span data-ttu-id="33583-135">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="33583-135">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="33583-136">제거-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="33583-136">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="33583-137">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="33583-137">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


