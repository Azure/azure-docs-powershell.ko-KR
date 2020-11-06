---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
ms.openlocfilehash: c758131685787ec8627f6e0cd3760e2ee42107c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536591"
---
# <span data-ttu-id="e252f-101">Get-AzureRmExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="e252f-101">Get-AzureRmExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="e252f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e252f-102">SYNOPSIS</span></span>
<span data-ttu-id="e252f-103">ExpressRoutePort 링크 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e252f-103">Gets an ExpressRoutePort link configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e252f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e252f-104">SYNTAX</span></span>

### <span data-ttu-id="e252f-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e252f-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e252f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e252f-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> -ResourceId <String> 
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e252f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e252f-107">DESCRIPTION</span></span>
<span data-ttu-id="e252f-108">**AzureRmExpressRoutePortLinkConfig** Cmdlet은 ExpressRoutePort의 링크 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="e252f-108">The **Get-AzureRmExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="e252f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e252f-109">EXAMPLES</span></span>

### <span data-ttu-id="e252f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e252f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="e252f-111">ExpressRoutePort $erport의 Link1 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e252f-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="e252f-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="e252f-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="e252f-113">ExpressRoutePort의 ResourceId $id를 사용 하 여 링크의 구성을 가져옵니다 $erport</span><span class="sxs-lookup"><span data-stu-id="e252f-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="e252f-114">변수</span><span class="sxs-lookup"><span data-stu-id="e252f-114">PARAMETERS</span></span>

### <span data-ttu-id="e252f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e252f-115">-DefaultProfile</span></span>
<span data-ttu-id="e252f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e252f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e252f-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e252f-117">-ExpressRoutePort</span></span>
<span data-ttu-id="e252f-118">ExpressRoutePort 리소스에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="e252f-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="e252f-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e252f-119">-Name</span></span>
<span data-ttu-id="e252f-120">링크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e252f-120">Name of the link.</span></span>

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

### <span data-ttu-id="e252f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e252f-121">-ResourceId</span></span>
<span data-ttu-id="e252f-122">링크의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="e252f-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="e252f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e252f-123">CommonParameters</span></span>
<span data-ttu-id="e252f-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e252f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e252f-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e252f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e252f-126">입력</span><span class="sxs-lookup"><span data-stu-id="e252f-126">INPUTS</span></span>

### <span data-ttu-id="e252f-127">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e252f-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="e252f-128">출력</span><span class="sxs-lookup"><span data-stu-id="e252f-128">OUTPUTS</span></span>

### <span data-ttu-id="e252f-129">PSExpressRouteLink에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e252f-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="e252f-130">상속자</span><span class="sxs-lookup"><span data-stu-id="e252f-130">NOTES</span></span>

## <span data-ttu-id="e252f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e252f-131">RELATED LINKS</span></span>
