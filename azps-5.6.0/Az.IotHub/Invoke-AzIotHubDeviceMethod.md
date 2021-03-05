---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 4c3782496041be7328ede29fad5ab3818791a0be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962944"
---
# <span data-ttu-id="7d8d3-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="7d8d3-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="7d8d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d8d3-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8d3-103">디바이스에서 직접 메서드를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="7d8d3-104">구문</span><span class="sxs-lookup"><span data-stu-id="7d8d3-104">SYNTAX</span></span>

### <span data-ttu-id="7d8d3-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7d8d3-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d8d3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7d8d3-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d8d3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7d8d3-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d8d3-108">설명</span><span class="sxs-lookup"><span data-stu-id="7d8d3-108">DESCRIPTION</span></span>
<span data-ttu-id="7d8d3-109">디바이스에서 직접 메서드를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="7d8d3-110">자세한 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods 내용은 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="7d8d3-111">예제</span><span class="sxs-lookup"><span data-stu-id="7d8d3-111">EXAMPLES</span></span>

### <span data-ttu-id="7d8d3-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d8d3-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="7d8d3-113">디바이스 메서드를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-113">Invoke a device method.</span></span>

## <span data-ttu-id="7d8d3-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7d8d3-114">PARAMETERS</span></span>

### <span data-ttu-id="7d8d3-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="7d8d3-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="7d8d3-116">연결이 성공적으로 완료될 때까지 기다리는 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="7d8d3-117">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-117">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8d3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8d3-118">-DefaultProfile</span></span>
<span data-ttu-id="7d8d3-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d8d3-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7d8d3-120">-DeviceId</span></span>
<span data-ttu-id="7d8d3-121">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-121">Target Device Id.</span></span>

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

### <span data-ttu-id="7d8d3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d8d3-122">-InputObject</span></span>
<span data-ttu-id="7d8d3-123">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="7d8d3-123">IotHub object</span></span>

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

### <span data-ttu-id="7d8d3-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7d8d3-124">-IotHubName</span></span>
<span data-ttu-id="7d8d3-125">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="7d8d3-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7d8d3-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7d8d3-126">-Name</span></span>
<span data-ttu-id="7d8d3-127">이 디바이스에서 호출할 메서드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-127">The name of the method to invoke on this device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8d3-128">-페이로드</span><span class="sxs-lookup"><span data-stu-id="7d8d3-128">-Payload</span></span>
<span data-ttu-id="7d8d3-129">이 디바이스에서 호출할 메서드에 대한 페이로드입니다.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="7d8d3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d8d3-130">-ResourceGroupName</span></span>
<span data-ttu-id="7d8d3-131">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="7d8d3-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7d8d3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d8d3-132">-ResourceId</span></span>
<span data-ttu-id="7d8d3-133">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="7d8d3-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7d8d3-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="7d8d3-134">-ResponseTimeOut</span></span>
<span data-ttu-id="7d8d3-135">결과가 직접 메서드에서 수신될 때까지 기다리는 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="7d8d3-136">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-136">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8d3-137">-확인</span><span class="sxs-lookup"><span data-stu-id="7d8d3-137">-Confirm</span></span>
<span data-ttu-id="7d8d3-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d8d3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d8d3-139">-WhatIf</span></span>
<span data-ttu-id="7d8d3-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d8d3-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d8d3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8d3-142">CommonParameters</span></span>
<span data-ttu-id="7d8d3-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8d3-144">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7d8d3-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8d3-145">입력</span><span class="sxs-lookup"><span data-stu-id="7d8d3-145">INPUTS</span></span>

### <span data-ttu-id="7d8d3-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7d8d3-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7d8d3-147">System.String</span><span class="sxs-lookup"><span data-stu-id="7d8d3-147">System.String</span></span>

## <span data-ttu-id="7d8d3-148">출력</span><span class="sxs-lookup"><span data-stu-id="7d8d3-148">OUTPUTS</span></span>

### <span data-ttu-id="7d8d3-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="7d8d3-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="7d8d3-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7d8d3-150">NOTES</span></span>

## <span data-ttu-id="7d8d3-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d8d3-151">RELATED LINKS</span></span>
