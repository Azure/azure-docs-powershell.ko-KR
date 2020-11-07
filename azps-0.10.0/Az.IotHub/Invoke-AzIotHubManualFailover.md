---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: 5055960ae541ef93d57eee53078413143fad7839
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876740"
---
# <span data-ttu-id="30e30-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="30e30-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="30e30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30e30-102">SYNOPSIS</span></span>
<span data-ttu-id="30e30-103">IoT Hub에 대 한 장애 조치 프로세스를 geo 페어링 재해 복구 지역으로 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e30-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="30e30-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30e30-104">SYNTAX</span></span>

### <span data-ttu-id="30e30-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="30e30-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30e30-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="30e30-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30e30-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="30e30-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30e30-108">설명은</span><span class="sxs-lookup"><span data-stu-id="30e30-108">DESCRIPTION</span></span>
<span data-ttu-id="30e30-109">이는 IoT hub의 장애 조치를 보조 위치로 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="30e30-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="30e30-110">이 작업을 수행 하면 솔루션에 시간 및 원격 분석 손실이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e30-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="30e30-111">이 작업은 장기 실행 이며 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30e30-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="30e30-112">사용 하는 경우 주의 해 주십시오.</span><span class="sxs-lookup"><span data-stu-id="30e30-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="30e30-113">예제의</span><span class="sxs-lookup"><span data-stu-id="30e30-113">EXAMPLES</span></span>

### <span data-ttu-id="30e30-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="30e30-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="30e30-115">"Myiothub" IoT Hub의 장애 조치 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e30-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="30e30-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="30e30-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="30e30-117">백그라운드에서 "myiothub" IoT Hub의 장애 조치 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e30-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="30e30-118">변수</span><span class="sxs-lookup"><span data-stu-id="30e30-118">PARAMETERS</span></span>

### <span data-ttu-id="30e30-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30e30-119">-AsJob</span></span>
<span data-ttu-id="30e30-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="30e30-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30e30-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30e30-121">-DefaultProfile</span></span>
<span data-ttu-id="30e30-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30e30-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30e30-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30e30-123">-InputObject</span></span>
<span data-ttu-id="30e30-124">Iot Hub 개체</span><span class="sxs-lookup"><span data-stu-id="30e30-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="30e30-125">-이름</span><span class="sxs-lookup"><span data-stu-id="30e30-125">-Name</span></span>
<span data-ttu-id="30e30-126">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="30e30-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="30e30-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30e30-127">-PassThru</span></span>
<span data-ttu-id="30e30-128">Boolean 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30e30-128">Allows to return the boolean object.</span></span> <span data-ttu-id="30e30-129">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30e30-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="30e30-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30e30-130">-ResourceGroupName</span></span>
<span data-ttu-id="30e30-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30e30-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="30e30-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30e30-132">-ResourceId</span></span>
<span data-ttu-id="30e30-133">Iot Hub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="30e30-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="30e30-134">-확인</span><span class="sxs-lookup"><span data-stu-id="30e30-134">-Confirm</span></span>
<span data-ttu-id="30e30-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e30-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30e30-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30e30-136">-WhatIf</span></span>
<span data-ttu-id="30e30-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="30e30-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30e30-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30e30-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30e30-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e30-139">CommonParameters</span></span>
<span data-ttu-id="30e30-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e30-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e30-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30e30-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e30-142">입력</span><span class="sxs-lookup"><span data-stu-id="30e30-142">INPUTS</span></span>

### <span data-ttu-id="30e30-143">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="30e30-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="30e30-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="30e30-144">System.String</span></span>

## <span data-ttu-id="30e30-145">출력</span><span class="sxs-lookup"><span data-stu-id="30e30-145">OUTPUTS</span></span>

### <span data-ttu-id="30e30-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="30e30-146">System.Boolean</span></span>

## <span data-ttu-id="30e30-147">상속자</span><span class="sxs-lookup"><span data-stu-id="30e30-147">NOTES</span></span>

## <span data-ttu-id="30e30-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30e30-148">RELATED LINKS</span></span>
