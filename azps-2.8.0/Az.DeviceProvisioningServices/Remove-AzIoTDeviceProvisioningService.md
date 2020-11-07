---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: a2700c1872e53234d97e82c41a93ef6e9e328391
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696580"
---
# <span data-ttu-id="b4ddf-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="b4ddf-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="b4ddf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4ddf-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ddf-103">Azure IoT Hub 디바이스 프로비저닝 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddf-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="b4ddf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4ddf-104">SYNTAX</span></span>

### <span data-ttu-id="b4ddf-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b4ddf-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4ddf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b4ddf-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4ddf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b4ddf-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4ddf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b4ddf-108">DESCRIPTION</span></span>
<span data-ttu-id="b4ddf-109">Azure IoT Hub Device 프로비저닝 서비스에 대 한 소개는를 참조 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4ddf-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="b4ddf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b4ddf-110">EXAMPLES</span></span>

### <span data-ttu-id="b4ddf-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b4ddf-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="b4ddf-112">Azure IoT Hub 디바이스 프로비저닝 서비스 ' myiotdps '를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddf-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="b4ddf-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="b4ddf-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="b4ddf-114">파이프라인을 사용 하 여 Azure IoT Hub 디바이스 프로비저닝 서비스 ' myiotdps '를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddf-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="b4ddf-115">변수</span><span class="sxs-lookup"><span data-stu-id="b4ddf-115">PARAMETERS</span></span>

### <span data-ttu-id="b4ddf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ddf-116">-DefaultProfile</span></span>
<span data-ttu-id="b4ddf-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4ddf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4ddf-118">-InputObject</span></span>
<span data-ttu-id="b4ddf-119">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="b4ddf-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4ddf-120">-이름</span><span class="sxs-lookup"><span data-stu-id="b4ddf-120">-Name</span></span>
<span data-ttu-id="b4ddf-121">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="b4ddf-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="b4ddf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4ddf-122">-PassThru</span></span>
<span data-ttu-id="b4ddf-123">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="b4ddf-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b4ddf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4ddf-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4ddf-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddf-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b4ddf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4ddf-126">-ResourceId</span></span>
<span data-ttu-id="b4ddf-127">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="b4ddf-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="b4ddf-128">-확인</span><span class="sxs-lookup"><span data-stu-id="b4ddf-128">-Confirm</span></span>
<span data-ttu-id="b4ddf-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4ddf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4ddf-130">-WhatIf</span></span>
<span data-ttu-id="b4ddf-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4ddf-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4ddf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ddf-133">CommonParameters</span></span>
<span data-ttu-id="b4ddf-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ddf-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4ddf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ddf-136">입력</span><span class="sxs-lookup"><span data-stu-id="b4ddf-136">INPUTS</span></span>

### <span data-ttu-id="b4ddf-137">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="b4ddf-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="b4ddf-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b4ddf-138">System.String</span></span>

## <span data-ttu-id="b4ddf-139">출력</span><span class="sxs-lookup"><span data-stu-id="b4ddf-139">OUTPUTS</span></span>

### <span data-ttu-id="b4ddf-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b4ddf-140">System.Boolean</span></span>

## <span data-ttu-id="b4ddf-141">상속자</span><span class="sxs-lookup"><span data-stu-id="b4ddf-141">NOTES</span></span>

## <span data-ttu-id="b4ddf-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4ddf-142">RELATED LINKS</span></span>
