---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 341d46e5dd4ceefaf8baa76a71de462559115a5d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042828"
---
# <span data-ttu-id="f8502-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f8502-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="f8502-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8502-102">SYNOPSIS</span></span>
<span data-ttu-id="f8502-103">CDN 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8502-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="f8502-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f8502-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8502-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f8502-105">DESCRIPTION</span></span>
<span data-ttu-id="f8502-106">**AzCdnProfile** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8502-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="f8502-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f8502-107">EXAMPLES</span></span>

## <span data-ttu-id="f8502-108">변수</span><span class="sxs-lookup"><span data-stu-id="f8502-108">PARAMETERS</span></span>

### <span data-ttu-id="f8502-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="f8502-109">-CdnProfile</span></span>
<span data-ttu-id="f8502-110">이 cmdlet이 업데이트 하는 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8502-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="f8502-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8502-111">-DefaultProfile</span></span>
<span data-ttu-id="f8502-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f8502-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8502-113">-확인</span><span class="sxs-lookup"><span data-stu-id="f8502-113">-Confirm</span></span>
<span data-ttu-id="f8502-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8502-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8502-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8502-115">-WhatIf</span></span>
<span data-ttu-id="f8502-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f8502-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8502-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8502-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8502-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8502-118">CommonParameters</span></span>
<span data-ttu-id="f8502-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8502-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8502-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f8502-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8502-121">입력</span><span class="sxs-lookup"><span data-stu-id="f8502-121">INPUTS</span></span>

### <span data-ttu-id="f8502-122">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="f8502-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="f8502-123">출력</span><span class="sxs-lookup"><span data-stu-id="f8502-123">OUTPUTS</span></span>

### <span data-ttu-id="f8502-124">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="f8502-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="f8502-125">상속자</span><span class="sxs-lookup"><span data-stu-id="f8502-125">NOTES</span></span>

## <span data-ttu-id="f8502-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8502-126">RELATED LINKS</span></span>

[<span data-ttu-id="f8502-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f8502-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="f8502-128">새로운 AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f8502-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="f8502-129">제거-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f8502-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


