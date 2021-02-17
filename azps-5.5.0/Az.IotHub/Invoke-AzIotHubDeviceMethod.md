---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 78247b26d2f8e6618d3999389efa509e3f8854b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192420"
---
# <span data-ttu-id="1209d-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="1209d-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="1209d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1209d-102">SYNOPSIS</span></span>
<span data-ttu-id="1209d-103">디바이스에서 직접 메서드를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="1209d-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="1209d-104">구문</span><span class="sxs-lookup"><span data-stu-id="1209d-104">SYNTAX</span></span>

### <span data-ttu-id="1209d-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1209d-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1209d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1209d-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1209d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1209d-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1209d-108">설명</span><span class="sxs-lookup"><span data-stu-id="1209d-108">DESCRIPTION</span></span>
<span data-ttu-id="1209d-109">디바이스에서 직접 메서드를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="1209d-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="1209d-110">자세한 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods 내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1209d-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="1209d-111">예제</span><span class="sxs-lookup"><span data-stu-id="1209d-111">EXAMPLES</span></span>

### <span data-ttu-id="1209d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="1209d-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="1209d-113">디바이스 메서드를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="1209d-113">Invoke a device method.</span></span>

## <span data-ttu-id="1209d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1209d-114">PARAMETERS</span></span>

### <span data-ttu-id="1209d-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="1209d-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="1209d-116">연결이 성공적으로 완료될 때까지 대기하는 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="1209d-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="1209d-117">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="1209d-117">Default is 10.</span></span>

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

### <span data-ttu-id="1209d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1209d-118">-DefaultProfile</span></span>
<span data-ttu-id="1209d-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1209d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1209d-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="1209d-120">-DeviceId</span></span>
<span data-ttu-id="1209d-121">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1209d-121">Target Device Id.</span></span>

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

### <span data-ttu-id="1209d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1209d-122">-InputObject</span></span>
<span data-ttu-id="1209d-123">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="1209d-123">IotHub object</span></span>

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

### <span data-ttu-id="1209d-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1209d-124">-IotHubName</span></span>
<span data-ttu-id="1209d-125">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="1209d-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1209d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1209d-126">-Name</span></span>
<span data-ttu-id="1209d-127">이 디바이스에서 호출할 메서드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1209d-127">The name of the method to invoke on this device.</span></span>

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

### <span data-ttu-id="1209d-128">-Payload</span><span class="sxs-lookup"><span data-stu-id="1209d-128">-Payload</span></span>
<span data-ttu-id="1209d-129">이 디바이스에서 호출할 메서드에 대한 페이로드입니다.</span><span class="sxs-lookup"><span data-stu-id="1209d-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="1209d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1209d-130">-ResourceGroupName</span></span>
<span data-ttu-id="1209d-131">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="1209d-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1209d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1209d-132">-ResourceId</span></span>
<span data-ttu-id="1209d-133">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="1209d-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1209d-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="1209d-134">-ResponseTimeOut</span></span>
<span data-ttu-id="1209d-135">직접 메서드에서 결과가 수신될 때까지 대기하는 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="1209d-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="1209d-136">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="1209d-136">Default is 10.</span></span>

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

### <span data-ttu-id="1209d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1209d-137">-Confirm</span></span>
<span data-ttu-id="1209d-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1209d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1209d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1209d-139">-WhatIf</span></span>
<span data-ttu-id="1209d-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1209d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1209d-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1209d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1209d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1209d-142">CommonParameters</span></span>
<span data-ttu-id="1209d-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1209d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1209d-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1209d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1209d-145">입력</span><span class="sxs-lookup"><span data-stu-id="1209d-145">INPUTS</span></span>

### <span data-ttu-id="1209d-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1209d-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1209d-147">System.String</span><span class="sxs-lookup"><span data-stu-id="1209d-147">System.String</span></span>

## <span data-ttu-id="1209d-148">출력</span><span class="sxs-lookup"><span data-stu-id="1209d-148">OUTPUTS</span></span>

### <span data-ttu-id="1209d-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="1209d-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="1209d-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1209d-150">NOTES</span></span>

## <span data-ttu-id="1209d-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1209d-151">RELATED LINKS</span></span>
