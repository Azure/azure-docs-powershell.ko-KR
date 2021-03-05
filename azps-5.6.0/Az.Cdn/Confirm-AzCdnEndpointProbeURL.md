---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: afc2400feb8694e74dd46731969429d6d7784369
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007264"
---
# <span data-ttu-id="91145-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="91145-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="91145-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91145-102">SYNOPSIS</span></span>
<span data-ttu-id="91145-103">프로브 URL의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="91145-103">Validates a probe URL.</span></span>

## <span data-ttu-id="91145-104">구문</span><span class="sxs-lookup"><span data-stu-id="91145-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91145-105">설명</span><span class="sxs-lookup"><span data-stu-id="91145-105">DESCRIPTION</span></span>
<span data-ttu-id="91145-106">**Confirm-AzCdnEndpointProbeURL** cmdlet은 제공된 프로브 URL을 동적 사이트 가속에 사용할 수 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="91145-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="91145-107">예제</span><span class="sxs-lookup"><span data-stu-id="91145-107">EXAMPLES</span></span>

### <span data-ttu-id="91145-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="91145-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="91145-109">프로브 URL의 유효성을 http://www.bing.com/images 검사합니다. "</span><span class="sxs-lookup"><span data-stu-id="91145-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="91145-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="91145-110">PARAMETERS</span></span>

### <span data-ttu-id="91145-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91145-111">-DefaultProfile</span></span>
<span data-ttu-id="91145-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91145-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91145-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="91145-113">-ProbeUrl</span></span>
<span data-ttu-id="91145-114">유효성을 검사하는 제안된 프로브 URL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91145-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="91145-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91145-115">CommonParameters</span></span>
<span data-ttu-id="91145-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="91145-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91145-117">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91145-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91145-118">입력</span><span class="sxs-lookup"><span data-stu-id="91145-118">INPUTS</span></span>

### <span data-ttu-id="91145-119">없음</span><span class="sxs-lookup"><span data-stu-id="91145-119">None</span></span>

## <span data-ttu-id="91145-120">출력</span><span class="sxs-lookup"><span data-stu-id="91145-120">OUTPUTS</span></span>

### <span data-ttu-id="91145-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="91145-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="91145-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="91145-122">NOTES</span></span>

## <span data-ttu-id="91145-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91145-123">RELATED LINKS</span></span>
