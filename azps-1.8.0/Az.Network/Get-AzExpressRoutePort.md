---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 69a03bc9772e9d74fdc1863221c99b46620ae700
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700577"
---
# <span data-ttu-id="88ded-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="88ded-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="88ded-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88ded-102">SYNOPSIS</span></span>
<span data-ttu-id="88ded-103">Azure ExpressRoutePort 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88ded-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="88ded-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88ded-104">SYNTAX</span></span>

### <span data-ttu-id="88ded-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="88ded-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88ded-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ded-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88ded-107">설명은</span><span class="sxs-lookup"><span data-stu-id="88ded-107">DESCRIPTION</span></span>
<span data-ttu-id="88ded-108">**AzExpressRoutePort** cmdlet은 구독에서 ExpressRoutePort 개체를 검색 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="88ded-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="88ded-109">ExpressRoutePort에서 작동 하는 다른 cmdlet에 대 한 입력으로 반환 되는 expressrouteport 개체를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88ded-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="88ded-110">예제의</span><span class="sxs-lookup"><span data-stu-id="88ded-110">EXAMPLES</span></span>

### <span data-ttu-id="88ded-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="88ded-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="88ded-112">구독에 있는 리소스 그룹 $rg에서 이름이 $PortName 인 ExpressRoutePort 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88ded-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="88ded-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="88ded-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="88ded-114">이름이 "test"로 시작 하는 모든 ExpressRoutePort 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88ded-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="88ded-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="88ded-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="88ded-116">ResourceId $id를 사용 하 여 ExpressRoutePort 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88ded-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="88ded-117">변수</span><span class="sxs-lookup"><span data-stu-id="88ded-117">PARAMETERS</span></span>

### <span data-ttu-id="88ded-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ded-118">-DefaultProfile</span></span>
<span data-ttu-id="88ded-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88ded-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88ded-120">-이름</span><span class="sxs-lookup"><span data-stu-id="88ded-120">-Name</span></span>
<span data-ttu-id="88ded-121">ExpressRoutePort의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88ded-121">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="88ded-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88ded-122">-ResourceGroupName</span></span>
<span data-ttu-id="88ded-123">ExpressRoutePort의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88ded-123">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="88ded-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88ded-124">-ResourceId</span></span>
<span data-ttu-id="88ded-125">Express 경로 포트의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="88ded-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="88ded-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ded-126">CommonParameters</span></span>
<span data-ttu-id="88ded-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88ded-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ded-128">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="88ded-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ded-129">입력</span><span class="sxs-lookup"><span data-stu-id="88ded-129">INPUTS</span></span>

### <span data-ttu-id="88ded-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="88ded-130">System.String</span></span>

## <span data-ttu-id="88ded-131">출력</span><span class="sxs-lookup"><span data-stu-id="88ded-131">OUTPUTS</span></span>

### <span data-ttu-id="88ded-132">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="88ded-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="88ded-133">상속자</span><span class="sxs-lookup"><span data-stu-id="88ded-133">NOTES</span></span>

## <span data-ttu-id="88ded-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88ded-134">RELATED LINKS</span></span>

[<span data-ttu-id="88ded-135">새로운 AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="88ded-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="88ded-136">제거-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="88ded-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="88ded-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="88ded-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)