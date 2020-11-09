---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 197d18f5d7585f6ae7e865b1c2b0449d032b4238
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310868"
---
# <span data-ttu-id="714ba-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="714ba-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="714ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="714ba-102">SYNOPSIS</span></span>
<span data-ttu-id="714ba-103">ExpressRoutePort 링크 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="714ba-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="714ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="714ba-104">SYNTAX</span></span>

### <span data-ttu-id="714ba-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="714ba-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="714ba-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="714ba-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="714ba-107">설명은</span><span class="sxs-lookup"><span data-stu-id="714ba-107">DESCRIPTION</span></span>
<span data-ttu-id="714ba-108">**AzExpressRoutePortLinkConfig** Cmdlet은 ExpressRoutePort의 링크 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="714ba-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="714ba-109">예제의</span><span class="sxs-lookup"><span data-stu-id="714ba-109">EXAMPLES</span></span>

### <span data-ttu-id="714ba-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="714ba-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="714ba-111">ExpressRoutePort $erport의 Link1 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="714ba-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="714ba-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="714ba-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="714ba-113">ExpressRoutePort의 ResourceId $id를 사용 하 여 링크의 구성을 가져옵니다 $erport</span><span class="sxs-lookup"><span data-stu-id="714ba-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="714ba-114">변수</span><span class="sxs-lookup"><span data-stu-id="714ba-114">PARAMETERS</span></span>

### <span data-ttu-id="714ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="714ba-115">-DefaultProfile</span></span>
<span data-ttu-id="714ba-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="714ba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="714ba-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="714ba-117">-ExpressRoutePort</span></span>
<span data-ttu-id="714ba-118">ExpressRoutePort 리소스에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="714ba-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="714ba-119">-이름</span><span class="sxs-lookup"><span data-stu-id="714ba-119">-Name</span></span>
<span data-ttu-id="714ba-120">링크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="714ba-120">Name of the link.</span></span>

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

### <span data-ttu-id="714ba-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="714ba-121">-ResourceId</span></span>
<span data-ttu-id="714ba-122">링크의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="714ba-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="714ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="714ba-123">CommonParameters</span></span>
<span data-ttu-id="714ba-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="714ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="714ba-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="714ba-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="714ba-126">입력</span><span class="sxs-lookup"><span data-stu-id="714ba-126">INPUTS</span></span>

### <span data-ttu-id="714ba-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="714ba-127">System.String</span></span>

### <span data-ttu-id="714ba-128">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="714ba-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="714ba-129">출력</span><span class="sxs-lookup"><span data-stu-id="714ba-129">OUTPUTS</span></span>

### <span data-ttu-id="714ba-130">PSExpressRouteLink에 대 한.</span><span class="sxs-lookup"><span data-stu-id="714ba-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="714ba-131">상속자</span><span class="sxs-lookup"><span data-stu-id="714ba-131">NOTES</span></span>

## <span data-ttu-id="714ba-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="714ba-132">RELATED LINKS</span></span>
