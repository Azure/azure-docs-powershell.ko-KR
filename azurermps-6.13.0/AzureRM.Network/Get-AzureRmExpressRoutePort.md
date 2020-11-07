---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
ms.openlocfilehash: 36c15c9a0bfae9bbf3a14f59877d23c1c8778163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711342"
---
# <span data-ttu-id="f3218-101">Get-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f3218-101">Get-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="f3218-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3218-102">SYNOPSIS</span></span>
<span data-ttu-id="f3218-103">Azure ExpressRoutePort 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f3218-103">Gets an Azure ExpressRoutePort resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3218-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3218-104">SYNTAX</span></span>

### <span data-ttu-id="f3218-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f3218-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3218-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3218-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3218-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f3218-107">DESCRIPTION</span></span>
<span data-ttu-id="f3218-108">**AzureRmExpressRoutePort** cmdlet은 구독에서 ExpressRoutePort 개체를 검색 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3218-108">The **Get-AzureRmExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="f3218-109">ExpressRoutePort에서 작동 하는 다른 cmdlet에 대 한 입력으로 반환 되는 expressrouteport 개체를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3218-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="f3218-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f3218-110">EXAMPLES</span></span>

### <span data-ttu-id="f3218-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f3218-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="f3218-112">구독에 있는 리소스 그룹 $rg에서 이름이 $PortName 인 ExpressRoutePort 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f3218-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="f3218-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f3218-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -ResourceId $id
```

<span data-ttu-id="f3218-114">ResourceId $id를 사용 하 여 ExpressRoutePort 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f3218-114">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="f3218-115">변수</span><span class="sxs-lookup"><span data-stu-id="f3218-115">PARAMETERS</span></span>

### <span data-ttu-id="f3218-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3218-116">-DefaultProfile</span></span>
<span data-ttu-id="f3218-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3218-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3218-118">-이름</span><span class="sxs-lookup"><span data-stu-id="f3218-118">-Name</span></span>
<span data-ttu-id="f3218-119">ExpressRoutePort의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3218-119">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3218-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3218-120">-ResourceGroupName</span></span>
<span data-ttu-id="f3218-121">ExpressRoutePort의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3218-121">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3218-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3218-122">-ResourceId</span></span>
<span data-ttu-id="f3218-123">Express 경로 포트의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="f3218-123">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="f3218-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3218-124">CommonParameters</span></span>
<span data-ttu-id="f3218-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3218-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3218-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3218-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3218-127">입력</span><span class="sxs-lookup"><span data-stu-id="f3218-127">INPUTS</span></span>

### <span data-ttu-id="f3218-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f3218-128">System.String</span></span>

## <span data-ttu-id="f3218-129">출력</span><span class="sxs-lookup"><span data-stu-id="f3218-129">OUTPUTS</span></span>

### <span data-ttu-id="f3218-130">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f3218-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="f3218-131">상속자</span><span class="sxs-lookup"><span data-stu-id="f3218-131">NOTES</span></span>

## <span data-ttu-id="f3218-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3218-132">RELATED LINKS</span></span>
