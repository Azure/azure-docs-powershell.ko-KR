---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azinterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
ms.openlocfilehash: 55133225b380e16112301620a52f857fca50dc0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700563"
---
# <span data-ttu-id="68f12-101">Get-AzInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="68f12-101">Get-AzInterfaceEndpoint</span></span>

## <span data-ttu-id="68f12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68f12-102">SYNOPSIS</span></span>
<span data-ttu-id="68f12-103">Get-AzInterfaceEndpoint cmdlet은 인터페이스 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68f12-103">The Get-AzInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="68f12-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68f12-104">SYNTAX</span></span>

### <span data-ttu-id="68f12-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="68f12-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzInterfaceEndpoint [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f12-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68f12-106">GetByResourceIdParameterSet</span></span>
```
Get-AzInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68f12-107">설명은</span><span class="sxs-lookup"><span data-stu-id="68f12-107">DESCRIPTION</span></span>
<span data-ttu-id="68f12-108">**Get-AzInterfaceEndpoint** Cmdlet은 인터페이스 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68f12-108">The **Get-AzInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="68f12-109">예제의</span><span class="sxs-lookup"><span data-stu-id="68f12-109">EXAMPLES</span></span>

### <span data-ttu-id="68f12-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="68f12-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="68f12-111">이 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 InterfaceEndpoint1 이라는 인터페이스 끝점을 가져와이를 $interfaceendpoint 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="68f12-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="68f12-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="68f12-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"
```

<span data-ttu-id="68f12-113">이 명령은 resourceId/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 인 인터페이스 끝점을 가져와이를 $interfaceendpoint 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="68f12-113">This command gets the interface endpoint with resourceId /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="68f12-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="68f12-114">Example 3</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name InterfaceEndpoint*
```

<span data-ttu-id="68f12-115">이 명령은 "Arendpoint"로 시작 하는 인터페이스 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68f12-115">This command gets the interface endpoints that start with "InterfaceEndpoint"</span></span>

## <span data-ttu-id="68f12-116">변수</span><span class="sxs-lookup"><span data-stu-id="68f12-116">PARAMETERS</span></span>

### <span data-ttu-id="68f12-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f12-117">-DefaultProfile</span></span>
<span data-ttu-id="68f12-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68f12-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68f12-119">-이름</span><span class="sxs-lookup"><span data-stu-id="68f12-119">-Name</span></span>
<span data-ttu-id="68f12-120">인터페이스 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68f12-120">The name of the interface endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="68f12-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68f12-121">-ResourceGroupName</span></span>
<span data-ttu-id="68f12-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68f12-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="68f12-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68f12-123">-ResourceId</span></span>
<span data-ttu-id="68f12-124">인터페이스 끝점의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="68f12-124">The ID of the interface endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68f12-125">-확인</span><span class="sxs-lookup"><span data-stu-id="68f12-125">-Confirm</span></span>
<span data-ttu-id="68f12-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68f12-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f12-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68f12-127">-WhatIf</span></span>
<span data-ttu-id="68f12-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="68f12-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68f12-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68f12-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f12-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f12-130">CommonParameters</span></span>
<span data-ttu-id="68f12-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68f12-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f12-132">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68f12-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f12-133">입력</span><span class="sxs-lookup"><span data-stu-id="68f12-133">INPUTS</span></span>

### <span data-ttu-id="68f12-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="68f12-134">System.String</span></span>

## <span data-ttu-id="68f12-135">출력</span><span class="sxs-lookup"><span data-stu-id="68f12-135">OUTPUTS</span></span>

### <span data-ttu-id="68f12-136">Microsoft. 네트워크 모델. Ps인터페이스 끝점</span><span class="sxs-lookup"><span data-stu-id="68f12-136">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>

## <span data-ttu-id="68f12-137">상속자</span><span class="sxs-lookup"><span data-stu-id="68f12-137">NOTES</span></span>

## <span data-ttu-id="68f12-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68f12-138">RELATED LINKS</span></span>
