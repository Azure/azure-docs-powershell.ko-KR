---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: d32cad2dc435c468ca785da4f81416c7c5330bd8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495448"
---
# <span data-ttu-id="df338-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="df338-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="df338-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df338-102">SYNOPSIS</span></span>
<span data-ttu-id="df338-103">IoT Hub에 대한 장애 조치 프로세스를 지역 쌍 재해 복구 지역에 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="df338-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="df338-104">구문</span><span class="sxs-lookup"><span data-stu-id="df338-104">SYNTAX</span></span>

### <span data-ttu-id="df338-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="df338-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df338-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="df338-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df338-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="df338-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df338-108">설명</span><span class="sxs-lookup"><span data-stu-id="df338-108">DESCRIPTION</span></span>
<span data-ttu-id="df338-109">IoT Hub를 보조 위치로 장애 조치(failover)를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="df338-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="df338-110">이 작업을 수행하면 솔루션에 대한 다운 시간 및 원격 분석 손실이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df338-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="df338-111">이 작업은 장기 실행 작업으로 완료하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df338-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="df338-112">사용할 때는 주의를 기울이는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="df338-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="df338-113">예제</span><span class="sxs-lookup"><span data-stu-id="df338-113">EXAMPLES</span></span>

### <span data-ttu-id="df338-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="df338-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="df338-115">"myiothub" IoT Hub의 장애 조치(failover) 프로세스 시작</span><span class="sxs-lookup"><span data-stu-id="df338-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="df338-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="df338-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="df338-117">백그라운드에서 "myiothub" IoT Hub의 장애 조치(failover) 프로세스 시작</span><span class="sxs-lookup"><span data-stu-id="df338-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="df338-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df338-118">PARAMETERS</span></span>

### <span data-ttu-id="df338-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df338-119">-AsJob</span></span>
<span data-ttu-id="df338-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="df338-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df338-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df338-121">-DefaultProfile</span></span>
<span data-ttu-id="df338-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df338-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df338-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df338-123">-InputObject</span></span>
<span data-ttu-id="df338-124">Iot Hub 개체</span><span class="sxs-lookup"><span data-stu-id="df338-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="df338-125">-Name</span><span class="sxs-lookup"><span data-stu-id="df338-125">-Name</span></span>
<span data-ttu-id="df338-126">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="df338-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="df338-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df338-127">-PassThru</span></span>
<span data-ttu-id="df338-128">부울 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df338-128">Allows to return the boolean object.</span></span> <span data-ttu-id="df338-129">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df338-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="df338-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df338-130">-ResourceGroupName</span></span>
<span data-ttu-id="df338-131">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="df338-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="df338-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df338-132">-ResourceId</span></span>
<span data-ttu-id="df338-133">Iot Hub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="df338-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="df338-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df338-134">-Confirm</span></span>
<span data-ttu-id="df338-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="df338-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df338-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df338-136">-WhatIf</span></span>
<span data-ttu-id="df338-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="df338-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df338-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df338-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df338-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df338-139">CommonParameters</span></span>
<span data-ttu-id="df338-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df338-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df338-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="df338-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df338-142">입력</span><span class="sxs-lookup"><span data-stu-id="df338-142">INPUTS</span></span>

### <span data-ttu-id="df338-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="df338-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="df338-144">System.String</span><span class="sxs-lookup"><span data-stu-id="df338-144">System.String</span></span>

## <span data-ttu-id="df338-145">출력</span><span class="sxs-lookup"><span data-stu-id="df338-145">OUTPUTS</span></span>

### <span data-ttu-id="df338-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="df338-146">System.Boolean</span></span>

## <span data-ttu-id="df338-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="df338-147">NOTES</span></span>

## <span data-ttu-id="df338-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df338-148">RELATED LINKS</span></span>
