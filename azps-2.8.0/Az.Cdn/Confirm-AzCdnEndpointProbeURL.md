---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: 517fb30fd95bfc435fcc847a7f9f0765befc21c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697621"
---
# <span data-ttu-id="e2bb4-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="e2bb4-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="e2bb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="e2bb4-103">프로브 URL의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2bb4-103">Validates a probe URL.</span></span>

## <span data-ttu-id="e2bb4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2bb4-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2bb4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e2bb4-105">DESCRIPTION</span></span>
<span data-ttu-id="e2bb4-106">AzCdnEndpointProbeURL cmdlet은 제공 된 프로브 URL을 동적 사이트 가속에 사용할 수 있는지 **확인** 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2bb4-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="e2bb4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e2bb4-107">EXAMPLES</span></span>

### <span data-ttu-id="e2bb4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e2bb4-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="e2bb4-109">검색 url ""의 유효성을 검사 합니다. http://www.bing.com/images</span><span class="sxs-lookup"><span data-stu-id="e2bb4-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="e2bb4-110">변수</span><span class="sxs-lookup"><span data-stu-id="e2bb4-110">PARAMETERS</span></span>

### <span data-ttu-id="e2bb4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2bb4-111">-DefaultProfile</span></span>
<span data-ttu-id="e2bb4-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2bb4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2bb4-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="e2bb4-113">-ProbeUrl</span></span>
<span data-ttu-id="e2bb4-114">유효성을 검사할 제안 된 프로브 URL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2bb4-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="e2bb4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2bb4-115">CommonParameters</span></span>
<span data-ttu-id="e2bb4-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2bb4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2bb4-117">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e2bb4-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2bb4-118">입력</span><span class="sxs-lookup"><span data-stu-id="e2bb4-118">INPUTS</span></span>

### <span data-ttu-id="e2bb4-119">않아야</span><span class="sxs-lookup"><span data-stu-id="e2bb4-119">None</span></span>

## <span data-ttu-id="e2bb4-120">출력</span><span class="sxs-lookup"><span data-stu-id="e2bb4-120">OUTPUTS</span></span>

### <span data-ttu-id="e2bb4-121">PSValidateProbeOutput를 통해 끝점을 보세요.</span><span class="sxs-lookup"><span data-stu-id="e2bb4-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="e2bb4-122">상속자</span><span class="sxs-lookup"><span data-stu-id="e2bb4-122">NOTES</span></span>

## <span data-ttu-id="e2bb4-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2bb4-123">RELATED LINKS</span></span>
