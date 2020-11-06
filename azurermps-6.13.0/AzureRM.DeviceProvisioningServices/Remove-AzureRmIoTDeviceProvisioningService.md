---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: ecc91bb19b3d5d40f8c5aa3e4f25812a9999e45b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529587"
---
# <span data-ttu-id="2d807-101">Remove-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="2d807-101">Remove-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="2d807-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d807-102">SYNOPSIS</span></span>
<span data-ttu-id="2d807-103">Azure IoT Hub 디바이스 프로비저닝 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d807-103">Delete an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d807-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d807-104">SYNTAX</span></span>

### <span data-ttu-id="2d807-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2d807-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d807-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2d807-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d807-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2d807-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d807-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2d807-108">DESCRIPTION</span></span>
<span data-ttu-id="2d807-109">Azure IoT Hub Device 프로비저닝 서비스에 대 한 소개는를 참조 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 하세요.</span><span class="sxs-lookup"><span data-stu-id="2d807-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="2d807-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2d807-110">EXAMPLES</span></span>

### <span data-ttu-id="2d807-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2d807-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="2d807-112">Azure IoT Hub 디바이스 프로비저닝 서비스 ' myiotdps '를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d807-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="2d807-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="2d807-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzureRmIotDps
```

<span data-ttu-id="2d807-114">파이프라인을 사용 하 여 Azure IoT Hub 디바이스 프로비저닝 서비스 ' myiotdps '를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d807-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="2d807-115">변수</span><span class="sxs-lookup"><span data-stu-id="2d807-115">PARAMETERS</span></span>

### <span data-ttu-id="2d807-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d807-116">-DefaultProfile</span></span>
<span data-ttu-id="2d807-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d807-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d807-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d807-118">-InputObject</span></span>
<span data-ttu-id="2d807-119">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="2d807-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="2d807-120">-이름</span><span class="sxs-lookup"><span data-stu-id="2d807-120">-Name</span></span>
<span data-ttu-id="2d807-121">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="2d807-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2d807-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d807-122">-PassThru</span></span>
<span data-ttu-id="2d807-123">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="2d807-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2d807-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d807-124">-ResourceGroupName</span></span>
<span data-ttu-id="2d807-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d807-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2d807-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d807-126">-ResourceId</span></span>
<span data-ttu-id="2d807-127">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="2d807-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2d807-128">-확인</span><span class="sxs-lookup"><span data-stu-id="2d807-128">-Confirm</span></span>
<span data-ttu-id="2d807-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d807-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d807-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d807-130">-WhatIf</span></span>
<span data-ttu-id="2d807-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2d807-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d807-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d807-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d807-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d807-133">CommonParameters</span></span>
<span data-ttu-id="2d807-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d807-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d807-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d807-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d807-136">입력</span><span class="sxs-lookup"><span data-stu-id="2d807-136">INPUTS</span></span>

### <span data-ttu-id="2d807-137">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="2d807-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="2d807-138">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2d807-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="2d807-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2d807-139">System.String</span></span>

## <span data-ttu-id="2d807-140">출력</span><span class="sxs-lookup"><span data-stu-id="2d807-140">OUTPUTS</span></span>

### <span data-ttu-id="2d807-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="2d807-141">System.Boolean</span></span>

## <span data-ttu-id="2d807-142">상속자</span><span class="sxs-lookup"><span data-stu-id="2d807-142">NOTES</span></span>

## <span data-ttu-id="2d807-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d807-143">RELATED LINKS</span></span>
