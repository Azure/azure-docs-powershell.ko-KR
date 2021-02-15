---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187076"
---
# <span data-ttu-id="82b13-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="82b13-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="82b13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82b13-102">SYNOPSIS</span></span>
<span data-ttu-id="82b13-103">Express 경로 포트에 대한 권한 부여 문서의 편지를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="82b13-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="82b13-104">구문</span><span class="sxs-lookup"><span data-stu-id="82b13-104">SYNTAX</span></span>

### <span data-ttu-id="82b13-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="82b13-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82b13-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82b13-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82b13-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82b13-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82b13-108">설명</span><span class="sxs-lookup"><span data-stu-id="82b13-108">DESCRIPTION</span></span>
<span data-ttu-id="82b13-109">New-AzExpressRoutePortLOA cmdlet은 EXPRESS 경로 포트에 대한 PDF 형식으로 권한 부여 문서를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="82b13-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="82b13-110">예제</span><span class="sxs-lookup"><span data-stu-id="82b13-110">EXAMPLES</span></span>

### <span data-ttu-id="82b13-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="82b13-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="82b13-112">Express 경로 포트 'myPort'에 대한 권한 부여 문서를 다운로드하고 'loa.pdf' 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="82b13-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="82b13-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82b13-113">PARAMETERS</span></span>

### <span data-ttu-id="82b13-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82b13-114">-AsJob</span></span>
<span data-ttu-id="82b13-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="82b13-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82b13-116">-CustomerName</span><span class="sxs-lookup"><span data-stu-id="82b13-116">-CustomerName</span></span>
<span data-ttu-id="82b13-117">이 Express 경로 포트가 할당된 고객 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82b13-117">The customer name to whom this Express Route Port is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b13-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b13-118">-DefaultProfile</span></span>
<span data-ttu-id="82b13-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82b13-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82b13-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="82b13-120">-Destination</span></span>
<span data-ttu-id="82b13-121">권한 부여 편지를 저장할 출력 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="82b13-121">The output filepath to store the Letter of Authorization to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b13-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="82b13-122">-ExpressRoutePort</span></span>
<span data-ttu-id="82b13-123">Express 경로 포트 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="82b13-123">The express route port resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b13-124">-Id</span><span class="sxs-lookup"><span data-stu-id="82b13-124">-Id</span></span>
<span data-ttu-id="82b13-125">Express 경로 포트의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="82b13-125">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b13-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82b13-126">-PassThru</span></span>
<span data-ttu-id="82b13-127">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="82b13-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="82b13-128">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82b13-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="82b13-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="82b13-129">-PortName</span></span>
<span data-ttu-id="82b13-130">Express 경로 포트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82b13-130">The express route port name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b13-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82b13-131">-ResourceGroupName</span></span>
<span data-ttu-id="82b13-132">Express 경로 포트의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82b13-132">The resource group name of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b13-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b13-133">CommonParameters</span></span>
<span data-ttu-id="82b13-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82b13-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b13-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82b13-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b13-136">입력</span><span class="sxs-lookup"><span data-stu-id="82b13-136">INPUTS</span></span>

### <span data-ttu-id="82b13-137">System.String</span><span class="sxs-lookup"><span data-stu-id="82b13-137">System.String</span></span>

## <span data-ttu-id="82b13-138">출력</span><span class="sxs-lookup"><span data-stu-id="82b13-138">OUTPUTS</span></span>

### <span data-ttu-id="82b13-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="82b13-139">System.Boolean</span></span>

## <span data-ttu-id="82b13-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82b13-140">NOTES</span></span>

## <span data-ttu-id="82b13-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82b13-141">RELATED LINKS</span></span>
