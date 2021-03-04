---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: a8326afbeb6d71d54ec861eb3ec65868e7e230bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956992"
---
# <span data-ttu-id="2ec1a-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="2ec1a-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="2ec1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ec1a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec1a-103">ExpressRoutePort 링크 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2ec1a-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="2ec1a-104">구문</span><span class="sxs-lookup"><span data-stu-id="2ec1a-104">SYNTAX</span></span>

### <span data-ttu-id="2ec1a-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2ec1a-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ec1a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ec1a-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ec1a-107">설명</span><span class="sxs-lookup"><span data-stu-id="2ec1a-107">DESCRIPTION</span></span>
<span data-ttu-id="2ec1a-108">**Get-AzExpressRoutePortLinkConfig** cmdlet은 ExpressRoutePort의 링크 구성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec1a-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="2ec1a-109">예제</span><span class="sxs-lookup"><span data-stu-id="2ec1a-109">EXAMPLES</span></span>

### <span data-ttu-id="2ec1a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2ec1a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="2ec1a-111">ExpressRoutePort의 Link1 구성을 $erport</span><span class="sxs-lookup"><span data-stu-id="2ec1a-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="2ec1a-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="2ec1a-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="2ec1a-113">ExpressRoutePort에서 ResourceId $id 링크 구성을 $erport</span><span class="sxs-lookup"><span data-stu-id="2ec1a-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="2ec1a-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2ec1a-114">PARAMETERS</span></span>

### <span data-ttu-id="2ec1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec1a-115">-DefaultProfile</span></span>
<span data-ttu-id="2ec1a-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ec1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ec1a-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2ec1a-117">-ExpressRoutePort</span></span>
<span data-ttu-id="2ec1a-118">ExpressRoutePort 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="2ec1a-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="2ec1a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2ec1a-119">-Name</span></span>
<span data-ttu-id="2ec1a-120">링크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ec1a-120">Name of the link.</span></span>

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

### <span data-ttu-id="2ec1a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ec1a-121">-ResourceId</span></span>
<span data-ttu-id="2ec1a-122">Link의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="2ec1a-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="2ec1a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec1a-123">CommonParameters</span></span>
<span data-ttu-id="2ec1a-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2ec1a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec1a-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ec1a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec1a-126">입력</span><span class="sxs-lookup"><span data-stu-id="2ec1a-126">INPUTS</span></span>

### <span data-ttu-id="2ec1a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="2ec1a-127">System.String</span></span>

### <span data-ttu-id="2ec1a-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2ec1a-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="2ec1a-129">출력</span><span class="sxs-lookup"><span data-stu-id="2ec1a-129">OUTPUTS</span></span>

### <span data-ttu-id="2ec1a-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="2ec1a-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="2ec1a-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2ec1a-131">NOTES</span></span>

## <span data-ttu-id="2ec1a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ec1a-132">RELATED LINKS</span></span>
