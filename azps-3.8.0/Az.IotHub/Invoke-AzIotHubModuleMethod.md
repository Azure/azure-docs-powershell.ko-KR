---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: 818e973d4d7be9fb03e23a23d7264745920f843f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043819"
---
# <span data-ttu-id="ba33f-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="ba33f-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="ba33f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba33f-102">SYNOPSIS</span></span>
<span data-ttu-id="ba33f-103">Edge 모듈 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="ba33f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba33f-104">SYNTAX</span></span>

### <span data-ttu-id="ba33f-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ba33f-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba33f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ba33f-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba33f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ba33f-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba33f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ba33f-108">DESCRIPTION</span></span>
<span data-ttu-id="ba33f-109">Edge 모듈 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-109">Invoke an Edge module method.</span></span> <span data-ttu-id="ba33f-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba33f-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="ba33f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ba33f-111">EXAMPLES</span></span>

### <span data-ttu-id="ba33f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ba33f-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="ba33f-113">Edge 모듈 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="ba33f-114">변수</span><span class="sxs-lookup"><span data-stu-id="ba33f-114">PARAMETERS</span></span>

### <span data-ttu-id="ba33f-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="ba33f-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="ba33f-116">연결을 설정할 때까지 대기 하는 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="ba33f-117">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-117">Default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba33f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba33f-118">-DefaultProfile</span></span>
<span data-ttu-id="ba33f-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba33f-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="ba33f-120">-DeviceId</span></span>
<span data-ttu-id="ba33f-121">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-121">Target Device Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba33f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba33f-122">-InputObject</span></span>
<span data-ttu-id="ba33f-123">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="ba33f-123">IotHub object</span></span>

```yaml
Type: PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba33f-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ba33f-124">-IotHubName</span></span>
<span data-ttu-id="ba33f-125">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="ba33f-125">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba33f-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="ba33f-126">-ModuleId</span></span>
<span data-ttu-id="ba33f-127">대상 디바이스의 모듈 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-127">Target device's module id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba33f-128">-이름</span><span class="sxs-lookup"><span data-stu-id="ba33f-128">-Name</span></span>
<span data-ttu-id="ba33f-129">이 장치 모듈에서 호출할 메서드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-129">The name of the method to invoke on this device module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba33f-130">-페이로드</span><span class="sxs-lookup"><span data-stu-id="ba33f-130">-Payload</span></span>
<span data-ttu-id="ba33f-131">이 장치 모듈에서 호출할 메서드의 페이로드입니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-131">The payload for the method to invoke on this device module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba33f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba33f-132">-ResourceGroupName</span></span>
<span data-ttu-id="ba33f-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-133">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba33f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba33f-134">-ResourceId</span></span>
<span data-ttu-id="ba33f-135">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="ba33f-135">IotHub Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba33f-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="ba33f-136">-ResponseTimeOut</span></span>
<span data-ttu-id="ba33f-137">Direct 메서드에서 결과를 받을 때까지 대기 하는 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="ba33f-138">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-138">Default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba33f-139">-확인</span><span class="sxs-lookup"><span data-stu-id="ba33f-139">-Confirm</span></span>
<span data-ttu-id="ba33f-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba33f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba33f-141">-WhatIf</span></span>
<span data-ttu-id="ba33f-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba33f-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba33f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba33f-144">CommonParameters</span></span>
<span data-ttu-id="ba33f-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba33f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ba33f-146">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba33f-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba33f-147">입력</span><span class="sxs-lookup"><span data-stu-id="ba33f-147">INPUTS</span></span>

### <span data-ttu-id="ba33f-148">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="ba33f-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ba33f-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ba33f-149">System.String</span></span>

## <span data-ttu-id="ba33f-150">출력</span><span class="sxs-lookup"><span data-stu-id="ba33f-150">OUTPUTS</span></span>

### <span data-ttu-id="ba33f-151">IotHub. PSCloudToDeviceMethodResult/. \*</span><span class="sxs-lookup"><span data-stu-id="ba33f-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="ba33f-152">상속자</span><span class="sxs-lookup"><span data-stu-id="ba33f-152">NOTES</span></span>

## <span data-ttu-id="ba33f-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba33f-153">RELATED LINKS</span></span>
