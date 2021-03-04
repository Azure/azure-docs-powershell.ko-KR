---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: a2b3a4878db022018bd0fae1d8e43e3700dd5e35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958363"
---
# <span data-ttu-id="6b95a-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="6b95a-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="6b95a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b95a-102">SYNOPSIS</span></span>
<span data-ttu-id="6b95a-103">Office 365 트래픽 중단 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6b95a-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="6b95a-104">구문</span><span class="sxs-lookup"><span data-stu-id="6b95a-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b95a-105">설명</span><span class="sxs-lookup"><span data-stu-id="6b95a-105">DESCRIPTION</span></span>
<span data-ttu-id="6b95a-106">New-AzVpnSite cmdlet과 함께 사용할 office 365 Update-AzVpnSite 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b95a-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="6b95a-107">예제</span><span class="sxs-lookup"><span data-stu-id="6b95a-107">EXAMPLES</span></span>

### <span data-ttu-id="6b95a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6b95a-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="6b95a-109">트래픽 범주를 허용하고 최적화할 수 있는 브레이크아웃을 사용하여 Office 365 트래픽 중단 정책을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b95a-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="6b95a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b95a-110">PARAMETERS</span></span>

### <span data-ttu-id="6b95a-111">-허용</span><span class="sxs-lookup"><span data-stu-id="6b95a-111">-Allow</span></span>
<span data-ttu-id="6b95a-112">허용 범주 트래픽을 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="6b95a-112">Breakout the allow category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b95a-113">-Default</span><span class="sxs-lookup"><span data-stu-id="6b95a-113">-Default</span></span>
<span data-ttu-id="6b95a-114">기본 범주 트래픽을 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="6b95a-114">Breakout the default category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b95a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b95a-115">-DefaultProfile</span></span>
<span data-ttu-id="6b95a-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b95a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b95a-117">-최적화</span><span class="sxs-lookup"><span data-stu-id="6b95a-117">-Optimize</span></span>
<span data-ttu-id="6b95a-118">최적화 범주 트래픽을 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="6b95a-118">Breakout the optimize category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b95a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b95a-119">CommonParameters</span></span>
<span data-ttu-id="6b95a-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6b95a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b95a-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b95a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b95a-122">입력</span><span class="sxs-lookup"><span data-stu-id="6b95a-122">INPUTS</span></span>

### <span data-ttu-id="6b95a-123">없음</span><span class="sxs-lookup"><span data-stu-id="6b95a-123">None</span></span>

## <span data-ttu-id="6b95a-124">출력</span><span class="sxs-lookup"><span data-stu-id="6b95a-124">OUTPUTS</span></span>

### <span data-ttu-id="6b95a-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="6b95a-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="6b95a-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6b95a-126">NOTES</span></span>

## <span data-ttu-id="6b95a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b95a-127">RELATED LINKS</span></span>
