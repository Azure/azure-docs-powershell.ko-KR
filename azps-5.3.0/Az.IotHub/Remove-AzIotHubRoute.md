---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: b729aa9bab91f5a977d827de6bd83828166ba103
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386646"
---
# <span data-ttu-id="b0781-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="b0781-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="b0781-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0781-102">SYNOPSIS</span></span>
<span data-ttu-id="b0781-103">IoT Hub에서 경로 삭제</span><span class="sxs-lookup"><span data-stu-id="b0781-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="b0781-104">구문</span><span class="sxs-lookup"><span data-stu-id="b0781-104">SYNTAX</span></span>

### <span data-ttu-id="b0781-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b0781-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0781-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b0781-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0781-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b0781-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0781-108">설명</span><span class="sxs-lookup"><span data-stu-id="b0781-108">DESCRIPTION</span></span>
<span data-ttu-id="b0781-109">엔드포인트에 대한 경로 삭제</span><span class="sxs-lookup"><span data-stu-id="b0781-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="b0781-110">예제</span><span class="sxs-lookup"><span data-stu-id="b0781-110">EXAMPLES</span></span>

### <span data-ttu-id="b0781-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b0781-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="b0781-112">"myiothub" IoT Hub에서 경로 "R1"을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b0781-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="b0781-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0781-113">PARAMETERS</span></span>

### <span data-ttu-id="b0781-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0781-114">-DefaultProfile</span></span>
<span data-ttu-id="b0781-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0781-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0781-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0781-116">-InputObject</span></span>
<span data-ttu-id="b0781-117">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="b0781-117">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0781-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b0781-118">-Name</span></span>
<span data-ttu-id="b0781-119">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="b0781-119">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0781-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0781-120">-PassThru</span></span>
<span data-ttu-id="b0781-121">부울 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0781-121">Allows to return the boolean object.</span></span> <span data-ttu-id="b0781-122">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0781-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b0781-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0781-123">-ResourceGroupName</span></span>
<span data-ttu-id="b0781-124">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="b0781-124">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0781-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0781-125">-ResourceId</span></span>
<span data-ttu-id="b0781-126">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b0781-126">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0781-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="b0781-127">-RouteName</span></span>
<span data-ttu-id="b0781-128">경로의 이름</span><span class="sxs-lookup"><span data-stu-id="b0781-128">Name of the Route</span></span>

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

### <span data-ttu-id="b0781-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0781-129">-Confirm</span></span>
<span data-ttu-id="b0781-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0781-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0781-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0781-131">-WhatIf</span></span>
<span data-ttu-id="b0781-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b0781-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0781-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0781-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0781-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0781-134">CommonParameters</span></span>
<span data-ttu-id="b0781-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b0781-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0781-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b0781-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0781-137">입력</span><span class="sxs-lookup"><span data-stu-id="b0781-137">INPUTS</span></span>

### <span data-ttu-id="b0781-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b0781-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b0781-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b0781-139">System.String</span></span>

## <span data-ttu-id="b0781-140">출력</span><span class="sxs-lookup"><span data-stu-id="b0781-140">OUTPUTS</span></span>

### <span data-ttu-id="b0781-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b0781-141">System.Boolean</span></span>

## <span data-ttu-id="b0781-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b0781-142">NOTES</span></span>

## <span data-ttu-id="b0781-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0781-143">RELATED LINKS</span></span>
