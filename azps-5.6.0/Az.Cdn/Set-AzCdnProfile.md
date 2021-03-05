---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 88e10d5f887d290139ee465217756c598bef0a3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975499"
---
# <span data-ttu-id="80262-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="80262-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="80262-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80262-102">SYNOPSIS</span></span>
<span data-ttu-id="80262-103">CDN 프로필을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="80262-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="80262-104">구문</span><span class="sxs-lookup"><span data-stu-id="80262-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80262-105">설명</span><span class="sxs-lookup"><span data-stu-id="80262-105">DESCRIPTION</span></span>
<span data-ttu-id="80262-106">**Set-AzCdnProfile** cmdlet은 AZURE CDN(콘텐츠 배달 네트워크) 프로필을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="80262-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="80262-107">예제</span><span class="sxs-lookup"><span data-stu-id="80262-107">EXAMPLES</span></span>

## <span data-ttu-id="80262-108">매개 변수</span><span class="sxs-lookup"><span data-stu-id="80262-108">PARAMETERS</span></span>

### <span data-ttu-id="80262-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="80262-109">-CdnProfile</span></span>
<span data-ttu-id="80262-110">이 cmdlet이 업데이트하는 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="80262-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="80262-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80262-111">-DefaultProfile</span></span>
<span data-ttu-id="80262-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="80262-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80262-113">-확인</span><span class="sxs-lookup"><span data-stu-id="80262-113">-Confirm</span></span>
<span data-ttu-id="80262-114">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="80262-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80262-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80262-115">-WhatIf</span></span>
<span data-ttu-id="80262-116">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="80262-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80262-117">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80262-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80262-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80262-118">CommonParameters</span></span>
<span data-ttu-id="80262-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="80262-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80262-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80262-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80262-121">입력</span><span class="sxs-lookup"><span data-stu-id="80262-121">INPUTS</span></span>

### <span data-ttu-id="80262-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="80262-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="80262-123">출력</span><span class="sxs-lookup"><span data-stu-id="80262-123">OUTPUTS</span></span>

### <span data-ttu-id="80262-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="80262-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="80262-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="80262-125">NOTES</span></span>

## <span data-ttu-id="80262-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80262-126">RELATED LINKS</span></span>

[<span data-ttu-id="80262-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="80262-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="80262-128">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="80262-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="80262-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="80262-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


