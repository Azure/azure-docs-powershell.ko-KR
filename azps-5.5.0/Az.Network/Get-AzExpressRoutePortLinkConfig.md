---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 197d18f5d7585f6ae7e865b1c2b0449d032b4238
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203086"
---
# <span data-ttu-id="542a8-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="542a8-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="542a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="542a8-102">SYNOPSIS</span></span>
<span data-ttu-id="542a8-103">ExpressRoutePort 링크 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="542a8-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="542a8-104">구문</span><span class="sxs-lookup"><span data-stu-id="542a8-104">SYNTAX</span></span>

### <span data-ttu-id="542a8-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="542a8-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="542a8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="542a8-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="542a8-107">설명</span><span class="sxs-lookup"><span data-stu-id="542a8-107">DESCRIPTION</span></span>
<span data-ttu-id="542a8-108">**Get-AzExpressRoutePortLinkConfig** cmdlet은 ExpressRoutePort의 링크 구성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="542a8-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="542a8-109">예제</span><span class="sxs-lookup"><span data-stu-id="542a8-109">EXAMPLES</span></span>

### <span data-ttu-id="542a8-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="542a8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="542a8-111">ExpressRoutePort의 Link1 구성을 $erport</span><span class="sxs-lookup"><span data-stu-id="542a8-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="542a8-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="542a8-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="542a8-113">ExpressRoutePort 계정에서 ResourceId $id 구성을 $erport</span><span class="sxs-lookup"><span data-stu-id="542a8-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="542a8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="542a8-114">PARAMETERS</span></span>

### <span data-ttu-id="542a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="542a8-115">-DefaultProfile</span></span>
<span data-ttu-id="542a8-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="542a8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="542a8-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="542a8-117">-ExpressRoutePort</span></span>
<span data-ttu-id="542a8-118">ExpressRoutePort 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="542a8-118">The reference of the ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="542a8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="542a8-119">-Name</span></span>
<span data-ttu-id="542a8-120">링크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="542a8-120">Name of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="542a8-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="542a8-121">-ResourceId</span></span>
<span data-ttu-id="542a8-122">링크의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="542a8-122">ResourceId of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="542a8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="542a8-123">CommonParameters</span></span>
<span data-ttu-id="542a8-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="542a8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="542a8-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="542a8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="542a8-126">입력</span><span class="sxs-lookup"><span data-stu-id="542a8-126">INPUTS</span></span>

### <span data-ttu-id="542a8-127">System.String</span><span class="sxs-lookup"><span data-stu-id="542a8-127">System.String</span></span>

### <span data-ttu-id="542a8-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="542a8-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="542a8-129">출력</span><span class="sxs-lookup"><span data-stu-id="542a8-129">OUTPUTS</span></span>

### <span data-ttu-id="542a8-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="542a8-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="542a8-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="542a8-131">NOTES</span></span>

## <span data-ttu-id="542a8-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="542a8-132">RELATED LINKS</span></span>
