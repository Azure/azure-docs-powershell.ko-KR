---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 78247b26d2f8e6618d3999389efa509e3f8854b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226983"
---
# <span data-ttu-id="7cd47-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="7cd47-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="7cd47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cd47-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd47-103">장치에서 직접 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd47-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="7cd47-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7cd47-104">SYNTAX</span></span>

### <span data-ttu-id="7cd47-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7cd47-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd47-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7cd47-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd47-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7cd47-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cd47-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7cd47-108">DESCRIPTION</span></span>
<span data-ttu-id="7cd47-109">장치에서 직접 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd47-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="7cd47-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7cd47-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="7cd47-111">예제의</span><span class="sxs-lookup"><span data-stu-id="7cd47-111">EXAMPLES</span></span>

### <span data-ttu-id="7cd47-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7cd47-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="7cd47-113">장치 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd47-113">Invoke a device method.</span></span>

## <span data-ttu-id="7cd47-114">변수</span><span class="sxs-lookup"><span data-stu-id="7cd47-114">PARAMETERS</span></span>

### <span data-ttu-id="7cd47-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="7cd47-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="7cd47-116">연결을 설정할 때까지 대기 하는 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="7cd47-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="7cd47-117">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="7cd47-117">Default is 10.</span></span>

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

### <span data-ttu-id="7cd47-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd47-118">-DefaultProfile</span></span>
<span data-ttu-id="7cd47-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7cd47-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cd47-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7cd47-120">-DeviceId</span></span>
<span data-ttu-id="7cd47-121">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="7cd47-121">Target Device Id.</span></span>

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

### <span data-ttu-id="7cd47-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cd47-122">-InputObject</span></span>
<span data-ttu-id="7cd47-123">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="7cd47-123">IotHub object</span></span>

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

### <span data-ttu-id="7cd47-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7cd47-124">-IotHubName</span></span>
<span data-ttu-id="7cd47-125">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="7cd47-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7cd47-126">-이름</span><span class="sxs-lookup"><span data-stu-id="7cd47-126">-Name</span></span>
<span data-ttu-id="7cd47-127">이 장치에서 호출할 메서드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7cd47-127">The name of the method to invoke on this device.</span></span>

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

### <span data-ttu-id="7cd47-128">-페이로드</span><span class="sxs-lookup"><span data-stu-id="7cd47-128">-Payload</span></span>
<span data-ttu-id="7cd47-129">이 장치에서 호출할 메서드의 페이로드입니다.</span><span class="sxs-lookup"><span data-stu-id="7cd47-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="7cd47-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cd47-130">-ResourceGroupName</span></span>
<span data-ttu-id="7cd47-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7cd47-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7cd47-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd47-132">-ResourceId</span></span>
<span data-ttu-id="7cd47-133">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="7cd47-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7cd47-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="7cd47-134">-ResponseTimeOut</span></span>
<span data-ttu-id="7cd47-135">Direct 메서드에서 결과를 받을 때까지 대기 하는 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="7cd47-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="7cd47-136">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="7cd47-136">Default is 10.</span></span>

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

### <span data-ttu-id="7cd47-137">-확인</span><span class="sxs-lookup"><span data-stu-id="7cd47-137">-Confirm</span></span>
<span data-ttu-id="7cd47-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd47-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cd47-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cd47-139">-WhatIf</span></span>
<span data-ttu-id="7cd47-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7cd47-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cd47-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7cd47-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cd47-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd47-142">CommonParameters</span></span>
<span data-ttu-id="7cd47-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cd47-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd47-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cd47-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd47-145">입력</span><span class="sxs-lookup"><span data-stu-id="7cd47-145">INPUTS</span></span>

### <span data-ttu-id="7cd47-146">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="7cd47-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7cd47-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7cd47-147">System.String</span></span>

## <span data-ttu-id="7cd47-148">출력</span><span class="sxs-lookup"><span data-stu-id="7cd47-148">OUTPUTS</span></span>

### <span data-ttu-id="7cd47-149">IotHub. PSCloudToDeviceMethodResult/. \*</span><span class="sxs-lookup"><span data-stu-id="7cd47-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="7cd47-150">상속자</span><span class="sxs-lookup"><span data-stu-id="7cd47-150">NOTES</span></span>

## <span data-ttu-id="7cd47-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7cd47-151">RELATED LINKS</span></span>
