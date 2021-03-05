---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: f9372a246e16e719db60f52922a8a416f3de10c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970811"
---
# <span data-ttu-id="ceb42-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="ceb42-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="ceb42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceb42-102">SYNOPSIS</span></span>
<span data-ttu-id="ceb42-103">IoT Hub에 대한 장애 조치(failover) 프로세스를 지역 페어링된 재해 복구 지역에 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="ceb42-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="ceb42-104">구문</span><span class="sxs-lookup"><span data-stu-id="ceb42-104">SYNTAX</span></span>

### <span data-ttu-id="ceb42-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ceb42-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceb42-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ceb42-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceb42-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ceb42-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceb42-108">설명</span><span class="sxs-lookup"><span data-stu-id="ceb42-108">DESCRIPTION</span></span>
<span data-ttu-id="ceb42-109">IoT Hub를 보조 위치로 장애 조치(failover)를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="ceb42-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="ceb42-110">이 작업은 솔루션에 대한 다운 시간 및 원격 분석 손실을 유발합니다.</span><span class="sxs-lookup"><span data-stu-id="ceb42-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="ceb42-111">이 작업은 장기 실행 작업으로 완료하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceb42-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="ceb42-112">사용 시 주의하세요.</span><span class="sxs-lookup"><span data-stu-id="ceb42-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="ceb42-113">예제</span><span class="sxs-lookup"><span data-stu-id="ceb42-113">EXAMPLES</span></span>

### <span data-ttu-id="ceb42-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="ceb42-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ceb42-115">"myiothub" IoT Hub의 장애 조치(failover) 프로세스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="ceb42-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="ceb42-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="ceb42-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="ceb42-117">백그라운드에서 "myiothub" IoT Hub의 장애 조치(failover) 프로세스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="ceb42-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="ceb42-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ceb42-118">PARAMETERS</span></span>

### <span data-ttu-id="ceb42-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ceb42-119">-AsJob</span></span>
<span data-ttu-id="ceb42-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ceb42-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ceb42-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceb42-121">-DefaultProfile</span></span>
<span data-ttu-id="ceb42-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ceb42-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ceb42-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ceb42-123">-InputObject</span></span>
<span data-ttu-id="ceb42-124">Iot Hub 개체</span><span class="sxs-lookup"><span data-stu-id="ceb42-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="ceb42-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ceb42-125">-Name</span></span>
<span data-ttu-id="ceb42-126">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="ceb42-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ceb42-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ceb42-127">-PassThru</span></span>
<span data-ttu-id="ceb42-128">부울 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceb42-128">Allows to return the boolean object.</span></span> <span data-ttu-id="ceb42-129">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ceb42-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ceb42-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceb42-130">-ResourceGroupName</span></span>
<span data-ttu-id="ceb42-131">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="ceb42-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ceb42-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ceb42-132">-ResourceId</span></span>
<span data-ttu-id="ceb42-133">Iot Hub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ceb42-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="ceb42-134">-확인</span><span class="sxs-lookup"><span data-stu-id="ceb42-134">-Confirm</span></span>
<span data-ttu-id="ceb42-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ceb42-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceb42-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceb42-136">-WhatIf</span></span>
<span data-ttu-id="ceb42-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ceb42-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ceb42-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ceb42-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceb42-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceb42-139">CommonParameters</span></span>
<span data-ttu-id="ceb42-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ceb42-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceb42-141">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ceb42-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceb42-142">입력</span><span class="sxs-lookup"><span data-stu-id="ceb42-142">INPUTS</span></span>

### <span data-ttu-id="ceb42-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ceb42-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ceb42-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ceb42-144">System.String</span></span>

## <span data-ttu-id="ceb42-145">출력</span><span class="sxs-lookup"><span data-stu-id="ceb42-145">OUTPUTS</span></span>

### <span data-ttu-id="ceb42-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ceb42-146">System.Boolean</span></span>

## <span data-ttu-id="ceb42-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ceb42-147">NOTES</span></span>

## <span data-ttu-id="ceb42-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ceb42-148">RELATED LINKS</span></span>
