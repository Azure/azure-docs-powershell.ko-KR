---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 341d46e5dd4ceefaf8baa76a71de462559115a5d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352910"
---
# <span data-ttu-id="cb60a-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="cb60a-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="cb60a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb60a-102">SYNOPSIS</span></span>
<span data-ttu-id="cb60a-103">CDN 프로필을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cb60a-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="cb60a-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb60a-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb60a-105">설명</span><span class="sxs-lookup"><span data-stu-id="cb60a-105">DESCRIPTION</span></span>
<span data-ttu-id="cb60a-106">**Set-AzCdnProfile** cmdlet은 Azure CDN(Content Delivery Network) 프로필을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cb60a-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="cb60a-107">예제</span><span class="sxs-lookup"><span data-stu-id="cb60a-107">EXAMPLES</span></span>

## <span data-ttu-id="cb60a-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb60a-108">PARAMETERS</span></span>

### <span data-ttu-id="cb60a-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="cb60a-109">-CdnProfile</span></span>
<span data-ttu-id="cb60a-110">이 cmdlet이 업데이트하는 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb60a-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="cb60a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb60a-111">-DefaultProfile</span></span>
<span data-ttu-id="cb60a-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cb60a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb60a-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb60a-113">-Confirm</span></span>
<span data-ttu-id="cb60a-114">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb60a-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb60a-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb60a-115">-WhatIf</span></span>
<span data-ttu-id="cb60a-116">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cb60a-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb60a-117">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb60a-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb60a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb60a-118">CommonParameters</span></span>
<span data-ttu-id="cb60a-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb60a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb60a-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cb60a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb60a-121">입력</span><span class="sxs-lookup"><span data-stu-id="cb60a-121">INPUTS</span></span>

### <span data-ttu-id="cb60a-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="cb60a-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="cb60a-123">출력</span><span class="sxs-lookup"><span data-stu-id="cb60a-123">OUTPUTS</span></span>

### <span data-ttu-id="cb60a-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="cb60a-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="cb60a-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb60a-125">NOTES</span></span>

## <span data-ttu-id="cb60a-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb60a-126">RELATED LINKS</span></span>

[<span data-ttu-id="cb60a-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="cb60a-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="cb60a-128">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="cb60a-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="cb60a-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="cb60a-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


