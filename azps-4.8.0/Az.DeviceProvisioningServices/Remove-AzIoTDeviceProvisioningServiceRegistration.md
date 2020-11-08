---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: b0fa84887a54eb1f4e9c689c49fb08a1300cd62b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213610"
---
# <span data-ttu-id="c3de6-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="c3de6-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="c3de6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3de6-102">SYNOPSIS</span></span>
<span data-ttu-id="c3de6-103">디바이스 등록을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3de6-103">Deletes the device registration.</span></span>

## <span data-ttu-id="c3de6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c3de6-104">SYNTAX</span></span>

### <span data-ttu-id="c3de6-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c3de6-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3de6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c3de6-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3de6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c3de6-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> -RegistrationId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3de6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c3de6-108">DESCRIPTION</span></span>
<span data-ttu-id="c3de6-109">Azure IoT Hub 디바이스 프로비저닝 서비스에서 디바이스 등록을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3de6-109">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="c3de6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c3de6-110">EXAMPLES</span></span>

### <span data-ttu-id="c3de6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c3de6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="c3de6-112">Azure IoT Hub 디바이스 프로비저닝 서비스에서 디바이스 등록을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3de6-112">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="c3de6-113">변수</span><span class="sxs-lookup"><span data-stu-id="c3de6-113">PARAMETERS</span></span>

### <span data-ttu-id="c3de6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3de6-114">-DefaultProfile</span></span>
<span data-ttu-id="c3de6-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3de6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3de6-116">-DpsName</span><span class="sxs-lookup"><span data-stu-id="c3de6-116">-DpsName</span></span>
<span data-ttu-id="c3de6-117">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="c3de6-117">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c3de6-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="c3de6-118">-DpsObject</span></span>
<span data-ttu-id="c3de6-119">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="c3de6-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c3de6-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3de6-120">-PassThru</span></span>
<span data-ttu-id="c3de6-121">Boolean 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3de6-121">Allows to return the boolean object.</span></span>
<span data-ttu-id="c3de6-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3de6-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c3de6-123">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="c3de6-123">-RegistrationId</span></span>
<span data-ttu-id="c3de6-124">디바이스 등록의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c3de6-124">ID of device registration.</span></span>

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

### <span data-ttu-id="c3de6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3de6-125">-ResourceGroupName</span></span>
<span data-ttu-id="c3de6-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3de6-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c3de6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3de6-127">-ResourceId</span></span>
<span data-ttu-id="c3de6-128">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="c3de6-128">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c3de6-129">-확인</span><span class="sxs-lookup"><span data-stu-id="c3de6-129">-Confirm</span></span>
<span data-ttu-id="c3de6-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3de6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3de6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3de6-131">-WhatIf</span></span>
<span data-ttu-id="c3de6-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c3de6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3de6-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3de6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3de6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3de6-134">CommonParameters</span></span>
<span data-ttu-id="c3de6-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3de6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3de6-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3de6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3de6-137">입력</span><span class="sxs-lookup"><span data-stu-id="c3de6-137">INPUTS</span></span>

### <span data-ttu-id="c3de6-138">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="c3de6-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="c3de6-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c3de6-139">System.String</span></span>

## <span data-ttu-id="c3de6-140">출력</span><span class="sxs-lookup"><span data-stu-id="c3de6-140">OUTPUTS</span></span>

### <span data-ttu-id="c3de6-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c3de6-141">System.Boolean</span></span>

## <span data-ttu-id="c3de6-142">상속자</span><span class="sxs-lookup"><span data-stu-id="c3de6-142">NOTES</span></span>

## <span data-ttu-id="c3de6-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3de6-143">RELATED LINKS</span></span>
