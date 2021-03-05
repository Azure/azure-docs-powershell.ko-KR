---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: f9ce00bb5efbe5182143a08f9f205101b9f85611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979584"
---
# <span data-ttu-id="3d2a2-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3d2a2-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="3d2a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d2a2-102">SYNOPSIS</span></span>
<span data-ttu-id="3d2a2-103">Azure ExpressRoutePort 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3d2a2-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="3d2a2-104">구문</span><span class="sxs-lookup"><span data-stu-id="3d2a2-104">SYNTAX</span></span>

### <span data-ttu-id="3d2a2-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3d2a2-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d2a2-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d2a2-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d2a2-107">설명</span><span class="sxs-lookup"><span data-stu-id="3d2a2-107">DESCRIPTION</span></span>
<span data-ttu-id="3d2a2-108">**Get-AzExpressRoutePort** cmdlet은 구독에서 ExpressRoutePort 개체를 검색하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d2a2-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="3d2a2-109">반환된 expressrouteport 개체는 ExpressRoutePort에서 작동하는 다른 cmdlet에 대한 입력으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d2a2-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="3d2a2-110">예제</span><span class="sxs-lookup"><span data-stu-id="3d2a2-110">EXAMPLES</span></span>

### <span data-ttu-id="3d2a2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3d2a2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="3d2a2-112">구독의 리소스 그룹에서 이름 $PortName ExpressRoutePort 개체를 $rg 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d2a2-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="3d2a2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="3d2a2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="3d2a2-114">이름이 "test"로 시작하는 모든 ExpressRoutePort 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3d2a2-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="3d2a2-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="3d2a2-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="3d2a2-116">ResourceId를 통해 ExpressRoutePort 개체를 $id.</span><span class="sxs-lookup"><span data-stu-id="3d2a2-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="3d2a2-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3d2a2-117">PARAMETERS</span></span>

### <span data-ttu-id="3d2a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d2a2-118">-DefaultProfile</span></span>
<span data-ttu-id="3d2a2-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d2a2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d2a2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3d2a2-120">-Name</span></span>
<span data-ttu-id="3d2a2-121">ExpressRoutePort의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d2a2-121">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="3d2a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d2a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="3d2a2-123">ExpressRoutePort의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d2a2-123">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="3d2a2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d2a2-124">-ResourceId</span></span>
<span data-ttu-id="3d2a2-125">Express 경로 포트의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="3d2a2-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="3d2a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d2a2-126">CommonParameters</span></span>
<span data-ttu-id="3d2a2-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3d2a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d2a2-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d2a2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d2a2-129">입력</span><span class="sxs-lookup"><span data-stu-id="3d2a2-129">INPUTS</span></span>

### <span data-ttu-id="3d2a2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3d2a2-130">System.String</span></span>

## <span data-ttu-id="3d2a2-131">출력</span><span class="sxs-lookup"><span data-stu-id="3d2a2-131">OUTPUTS</span></span>

### <span data-ttu-id="3d2a2-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3d2a2-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="3d2a2-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3d2a2-133">NOTES</span></span>

## <span data-ttu-id="3d2a2-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d2a2-134">RELATED LINKS</span></span>

[<span data-ttu-id="3d2a2-135">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3d2a2-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="3d2a2-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3d2a2-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="3d2a2-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3d2a2-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
