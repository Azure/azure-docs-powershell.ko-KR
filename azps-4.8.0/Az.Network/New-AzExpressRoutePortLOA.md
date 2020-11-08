---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214860"
---
# <span data-ttu-id="cdfca-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="cdfca-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="cdfca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdfca-102">SYNOPSIS</span></span>
<span data-ttu-id="cdfca-103">Express 경로 포트에 대 한 권한 부여 문서의 다운로드 편지입니다.</span><span class="sxs-lookup"><span data-stu-id="cdfca-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="cdfca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cdfca-104">SYNTAX</span></span>

### <span data-ttu-id="cdfca-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cdfca-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdfca-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdfca-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdfca-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdfca-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdfca-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cdfca-108">DESCRIPTION</span></span>
<span data-ttu-id="cdfca-109">New-AzExpressRoutePortLOA cmdlet은 express 경로 포트에 대 한 인증 문서의 문자를 PDF 형식으로 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdfca-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="cdfca-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cdfca-110">EXAMPLES</span></span>

### <span data-ttu-id="cdfca-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cdfca-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="cdfca-112">Express 경로 포트 ' myPort '에 대 한 권한 부여 문서의 문자를 다운로드 하 여 ' loa.pdf ' 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdfca-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="cdfca-113">변수</span><span class="sxs-lookup"><span data-stu-id="cdfca-113">PARAMETERS</span></span>

### <span data-ttu-id="cdfca-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cdfca-114">-AsJob</span></span>
<span data-ttu-id="cdfca-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cdfca-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cdfca-116">-CustomerName</span><span class="sxs-lookup"><span data-stu-id="cdfca-116">-CustomerName</span></span>
<span data-ttu-id="cdfca-117">이 Express 경로 포트가 할당 된 고객 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdfca-117">The customer name to whom this Express Route Port is assigned to.</span></span>

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

### <span data-ttu-id="cdfca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdfca-118">-DefaultProfile</span></span>
<span data-ttu-id="cdfca-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cdfca-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdfca-120">-대상</span><span class="sxs-lookup"><span data-stu-id="cdfca-120">-Destination</span></span>
<span data-ttu-id="cdfca-121">권한 부여의 문자를 저장할 출력 filepath입니다.</span><span class="sxs-lookup"><span data-stu-id="cdfca-121">The output filepath to store the Letter of Authorization to.</span></span>

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

### <span data-ttu-id="cdfca-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cdfca-122">-ExpressRoutePort</span></span>
<span data-ttu-id="cdfca-123">Express 경로 포트 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="cdfca-123">The express route port resource.</span></span>

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

### <span data-ttu-id="cdfca-124">-Id</span><span class="sxs-lookup"><span data-stu-id="cdfca-124">-Id</span></span>
<span data-ttu-id="cdfca-125">Express 경로 포트의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="cdfca-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="cdfca-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdfca-126">-PassThru</span></span>
<span data-ttu-id="cdfca-127">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdfca-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="cdfca-128">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cdfca-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cdfca-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="cdfca-129">-PortName</span></span>
<span data-ttu-id="cdfca-130">Express 경로 포트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdfca-130">The express route port name.</span></span>

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

### <span data-ttu-id="cdfca-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdfca-131">-ResourceGroupName</span></span>
<span data-ttu-id="cdfca-132">Express 경로 포트의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdfca-132">The resource group name of the express route port.</span></span>

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

### <span data-ttu-id="cdfca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdfca-133">CommonParameters</span></span>
<span data-ttu-id="cdfca-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdfca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdfca-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cdfca-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdfca-136">입력</span><span class="sxs-lookup"><span data-stu-id="cdfca-136">INPUTS</span></span>

### <span data-ttu-id="cdfca-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cdfca-137">System.String</span></span>

## <span data-ttu-id="cdfca-138">출력</span><span class="sxs-lookup"><span data-stu-id="cdfca-138">OUTPUTS</span></span>

### <span data-ttu-id="cdfca-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="cdfca-139">System.Boolean</span></span>

## <span data-ttu-id="cdfca-140">상속자</span><span class="sxs-lookup"><span data-stu-id="cdfca-140">NOTES</span></span>

## <span data-ttu-id="cdfca-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cdfca-141">RELATED LINKS</span></span>
