---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: 2aeb26447c5684b57d966c403a256fe3d1361a41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309562"
---
# <span data-ttu-id="36d78-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="36d78-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="36d78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36d78-102">SYNOPSIS</span></span>
<span data-ttu-id="36d78-103">Office 365 트래픽 브레이크 아웃 정책 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="36d78-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="36d78-104">구문과</span><span class="sxs-lookup"><span data-stu-id="36d78-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36d78-105">설명은</span><span class="sxs-lookup"><span data-stu-id="36d78-105">DESCRIPTION</span></span>
<span data-ttu-id="36d78-106">New-AzVpnSite 및 Update-AzVpnSite cmdlet에 사용할 office 365 아웃 브레이크 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="36d78-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="36d78-107">예제의</span><span class="sxs-lookup"><span data-stu-id="36d78-107">EXAMPLES</span></span>

### <span data-ttu-id="36d78-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="36d78-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="36d78-109">트래픽 허용 및 최적화 범주에 대 한 브레이크 아웃을 허용 하는 office 365 트래픽 브레이크 아웃 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="36d78-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="36d78-110">변수</span><span class="sxs-lookup"><span data-stu-id="36d78-110">PARAMETERS</span></span>

### <span data-ttu-id="36d78-111">-허용</span><span class="sxs-lookup"><span data-stu-id="36d78-111">-Allow</span></span>
<span data-ttu-id="36d78-112">범주 트래픽 허용을 브레이크 아웃 합니다.</span><span class="sxs-lookup"><span data-stu-id="36d78-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="36d78-113">-기본</span><span class="sxs-lookup"><span data-stu-id="36d78-113">-Default</span></span>
<span data-ttu-id="36d78-114">기본 범주 소통량을 브레이크 아웃 합니다.</span><span class="sxs-lookup"><span data-stu-id="36d78-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="36d78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d78-115">-DefaultProfile</span></span>
<span data-ttu-id="36d78-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36d78-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36d78-117">-최적화</span><span class="sxs-lookup"><span data-stu-id="36d78-117">-Optimize</span></span>
<span data-ttu-id="36d78-118">범주 소통량 최적화를 브레이크 합니다.</span><span class="sxs-lookup"><span data-stu-id="36d78-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="36d78-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d78-119">CommonParameters</span></span>
<span data-ttu-id="36d78-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36d78-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d78-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="36d78-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d78-122">입력</span><span class="sxs-lookup"><span data-stu-id="36d78-122">INPUTS</span></span>

### <span data-ttu-id="36d78-123">않아야</span><span class="sxs-lookup"><span data-stu-id="36d78-123">None</span></span>

## <span data-ttu-id="36d78-124">출력</span><span class="sxs-lookup"><span data-stu-id="36d78-124">OUTPUTS</span></span>

### <span data-ttu-id="36d78-125">PSO365PolicyProperties에 대 한.</span><span class="sxs-lookup"><span data-stu-id="36d78-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="36d78-126">상속자</span><span class="sxs-lookup"><span data-stu-id="36d78-126">NOTES</span></span>

## <span data-ttu-id="36d78-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36d78-127">RELATED LINKS</span></span>
