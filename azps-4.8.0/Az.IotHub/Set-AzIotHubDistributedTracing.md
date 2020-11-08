---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: 364b54f9e0b7a9112c2ce46f33363a4510c7bb68
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056329"
---
# <span data-ttu-id="c65ae-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="c65ae-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="c65ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c65ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c65ae-103">장치에 대 한 분산 추적 옵션을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c65ae-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="c65ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c65ae-104">SYNTAX</span></span>

### <span data-ttu-id="c65ae-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c65ae-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c65ae-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c65ae-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c65ae-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c65ae-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c65ae-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c65ae-108">DESCRIPTION</span></span>
<span data-ttu-id="c65ae-109">장치에 대 한 분산 추적 옵션을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c65ae-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="c65ae-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c65ae-110">EXAMPLES</span></span>

### <span data-ttu-id="c65ae-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c65ae-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="c65ae-112">장치에 대 한 분산 추적 옵션을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c65ae-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="c65ae-113">변수</span><span class="sxs-lookup"><span data-stu-id="c65ae-113">PARAMETERS</span></span>

### <span data-ttu-id="c65ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c65ae-114">-DefaultProfile</span></span>
<span data-ttu-id="c65ae-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c65ae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c65ae-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="c65ae-116">-DeviceId</span></span>
<span data-ttu-id="c65ae-117">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c65ae-117">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c65ae-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c65ae-118">-InputObject</span></span>
<span data-ttu-id="c65ae-119">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="c65ae-119">IotHub object</span></span>

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

### <span data-ttu-id="c65ae-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c65ae-120">-IotHubName</span></span>
<span data-ttu-id="c65ae-121">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="c65ae-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c65ae-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c65ae-122">-ResourceGroupName</span></span>
<span data-ttu-id="c65ae-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c65ae-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c65ae-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c65ae-124">-ResourceId</span></span>
<span data-ttu-id="c65ae-125">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="c65ae-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c65ae-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="c65ae-126">-SamplingMode</span></span>
<span data-ttu-id="c65ae-127">분산 추적을 사용 하도록 설정 하 고 샘플링을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c65ae-127">Turns sampling for distributed tracing enable and disable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDistributedTracingSamplingMode
Parameter Sets: (All)
Aliases: Mode
Accepted values: Disabled, Enabled

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c65ae-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="c65ae-128">-SamplingRate</span></span>
<span data-ttu-id="c65ae-129">추적 컨텍스트를 추가 하기 위해 샘플링 되는 메시지의 양을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="c65ae-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="c65ae-130">이 값은 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="c65ae-130">This value is a percentage.</span></span>
<span data-ttu-id="c65ae-131">0에서 100 (포함) 까지의 값만 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c65ae-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Rate

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c65ae-132">-확인</span><span class="sxs-lookup"><span data-stu-id="c65ae-132">-Confirm</span></span>
<span data-ttu-id="c65ae-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c65ae-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c65ae-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c65ae-134">-WhatIf</span></span>
<span data-ttu-id="c65ae-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c65ae-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c65ae-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c65ae-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c65ae-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c65ae-137">CommonParameters</span></span>
<span data-ttu-id="c65ae-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c65ae-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c65ae-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c65ae-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c65ae-140">입력</span><span class="sxs-lookup"><span data-stu-id="c65ae-140">INPUTS</span></span>

### <span data-ttu-id="c65ae-141">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="c65ae-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c65ae-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c65ae-142">System.String</span></span>

## <span data-ttu-id="c65ae-143">출력</span><span class="sxs-lookup"><span data-stu-id="c65ae-143">OUTPUTS</span></span>

### <span data-ttu-id="c65ae-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="c65ae-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="c65ae-145">상속자</span><span class="sxs-lookup"><span data-stu-id="c65ae-145">NOTES</span></span>

## <span data-ttu-id="c65ae-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c65ae-146">RELATED LINKS</span></span>
