---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservicecountry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceCountry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceCountry.md
ms.openlocfilehash: 4f13c0be9681fb2eda6fa509e321c2fa161049ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989487"
---
# <span data-ttu-id="882fa-101">Get-AzPeeringServiceCountry</span><span class="sxs-lookup"><span data-stu-id="882fa-101">Get-AzPeeringServiceCountry</span></span>

## <span data-ttu-id="882fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="882fa-102">SYNOPSIS</span></span>
<span data-ttu-id="882fa-103">피어링 서비스에 사용할 수 있는 국가를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="882fa-103">Lists the countries available for peering service.</span></span>

## <span data-ttu-id="882fa-104">구문</span><span class="sxs-lookup"><span data-stu-id="882fa-104">SYNTAX</span></span>

```
Get-AzPeeringServiceCountry [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="882fa-105">설명</span><span class="sxs-lookup"><span data-stu-id="882fa-105">DESCRIPTION</span></span>
<span data-ttu-id="882fa-106">피어링 서비스에 사용할 수 있는 국가를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="882fa-106">Lists the countries available for peering service.</span></span>

## <span data-ttu-id="882fa-107">예제</span><span class="sxs-lookup"><span data-stu-id="882fa-107">EXAMPLES</span></span>

### <span data-ttu-id="882fa-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="882fa-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceCountry
```

<span data-ttu-id="882fa-109">피어링 서비스에 사용할 수 있는 국가 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="882fa-109">List of countries available for peering service.</span></span>

## <span data-ttu-id="882fa-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="882fa-110">PARAMETERS</span></span>

### <span data-ttu-id="882fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="882fa-111">-DefaultProfile</span></span>
<span data-ttu-id="882fa-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="882fa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="882fa-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="882fa-113">CommonParameters</span></span>
<span data-ttu-id="882fa-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="882fa-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="882fa-115">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="882fa-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="882fa-116">입력</span><span class="sxs-lookup"><span data-stu-id="882fa-116">INPUTS</span></span>

### <span data-ttu-id="882fa-117">없음</span><span class="sxs-lookup"><span data-stu-id="882fa-117">None</span></span>

## <span data-ttu-id="882fa-118">출력</span><span class="sxs-lookup"><span data-stu-id="882fa-118">OUTPUTS</span></span>

### <span data-ttu-id="882fa-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="882fa-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="882fa-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="882fa-120">NOTES</span></span>

## <span data-ttu-id="882fa-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="882fa-121">RELATED LINKS</span></span>
