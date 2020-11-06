---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
ms.openlocfilehash: e80b82f567dd1c0935dd56d8e3996a63bcce72e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531421"
---
# <span data-ttu-id="3b7c1-101">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="3b7c1-101">Set-AzureRmCdnProfile</span></span>

## <span data-ttu-id="3b7c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b7c1-102">SYNOPSIS</span></span>
<span data-ttu-id="3b7c1-103">CDN 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7c1-103">Updates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b7c1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3b7c1-104">SYNTAX</span></span>

```
Set-AzureRmCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b7c1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3b7c1-105">DESCRIPTION</span></span>
<span data-ttu-id="3b7c1-106">**AzureRmCdnProfile** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7c1-106">The **Set-AzureRmCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="3b7c1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3b7c1-107">EXAMPLES</span></span>

## <span data-ttu-id="3b7c1-108">변수</span><span class="sxs-lookup"><span data-stu-id="3b7c1-108">PARAMETERS</span></span>

### <span data-ttu-id="3b7c1-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="3b7c1-109">-CdnProfile</span></span>
<span data-ttu-id="3b7c1-110">이 cmdlet이 업데이트 하는 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7c1-110">Specifies the profile that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b7c1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b7c1-111">-DefaultProfile</span></span>
<span data-ttu-id="3b7c1-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3b7c1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b7c1-113">-확인</span><span class="sxs-lookup"><span data-stu-id="3b7c1-113">-Confirm</span></span>
<span data-ttu-id="3b7c1-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7c1-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b7c1-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b7c1-115">-WhatIf</span></span>
<span data-ttu-id="3b7c1-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3b7c1-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b7c1-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b7c1-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b7c1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b7c1-118">CommonParameters</span></span>
<span data-ttu-id="3b7c1-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b7c1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b7c1-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b7c1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b7c1-121">입력</span><span class="sxs-lookup"><span data-stu-id="3b7c1-121">INPUTS</span></span>

### <span data-ttu-id="3b7c1-122">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="3b7c1-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="3b7c1-123">매개 변수: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3b7c1-123">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="3b7c1-124">출력</span><span class="sxs-lookup"><span data-stu-id="3b7c1-124">OUTPUTS</span></span>

### <span data-ttu-id="3b7c1-125">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="3b7c1-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="3b7c1-126">상속자</span><span class="sxs-lookup"><span data-stu-id="3b7c1-126">NOTES</span></span>

## <span data-ttu-id="3b7c1-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b7c1-127">RELATED LINKS</span></span>

[<span data-ttu-id="3b7c1-128">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="3b7c1-128">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="3b7c1-129">새로운 AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="3b7c1-129">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="3b7c1-130">제거-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="3b7c1-130">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)


