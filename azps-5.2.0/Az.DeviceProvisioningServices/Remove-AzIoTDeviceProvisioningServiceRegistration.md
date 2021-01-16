---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: b0fa84887a54eb1f4e9c689c49fb08a1300cd62b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338289"
---
# <span data-ttu-id="57b85-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="57b85-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="57b85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57b85-102">SYNOPSIS</span></span>
<span data-ttu-id="57b85-103">디바이스 등록을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="57b85-103">Deletes the device registration.</span></span>

## <span data-ttu-id="57b85-104">구문</span><span class="sxs-lookup"><span data-stu-id="57b85-104">SYNTAX</span></span>

### <span data-ttu-id="57b85-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="57b85-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57b85-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="57b85-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57b85-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="57b85-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> -RegistrationId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57b85-108">설명</span><span class="sxs-lookup"><span data-stu-id="57b85-108">DESCRIPTION</span></span>
<span data-ttu-id="57b85-109">Azure IoT Hub Device Provisioning Service에서 디바이스 등록을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="57b85-109">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="57b85-110">예제</span><span class="sxs-lookup"><span data-stu-id="57b85-110">EXAMPLES</span></span>

### <span data-ttu-id="57b85-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="57b85-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="57b85-112">Azure IoT Hub Device Provisioning Service에서 디바이스 등록을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="57b85-112">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="57b85-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57b85-113">PARAMETERS</span></span>

### <span data-ttu-id="57b85-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57b85-114">-DefaultProfile</span></span>
<span data-ttu-id="57b85-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57b85-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57b85-116">-DpsName</span><span class="sxs-lookup"><span data-stu-id="57b85-116">-DpsName</span></span>
<span data-ttu-id="57b85-117">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="57b85-117">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="57b85-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="57b85-118">-DpsObject</span></span>
<span data-ttu-id="57b85-119">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="57b85-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="57b85-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57b85-120">-PassThru</span></span>
<span data-ttu-id="57b85-121">부울 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57b85-121">Allows to return the boolean object.</span></span>
<span data-ttu-id="57b85-122">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57b85-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="57b85-123">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="57b85-123">-RegistrationId</span></span>
<span data-ttu-id="57b85-124">디바이스 등록의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="57b85-124">ID of device registration.</span></span>

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

### <span data-ttu-id="57b85-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57b85-125">-ResourceGroupName</span></span>
<span data-ttu-id="57b85-126">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="57b85-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="57b85-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57b85-127">-ResourceId</span></span>
<span data-ttu-id="57b85-128">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="57b85-128">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="57b85-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57b85-129">-Confirm</span></span>
<span data-ttu-id="57b85-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="57b85-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57b85-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57b85-131">-WhatIf</span></span>
<span data-ttu-id="57b85-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="57b85-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57b85-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57b85-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57b85-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b85-134">CommonParameters</span></span>
<span data-ttu-id="57b85-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57b85-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b85-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="57b85-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b85-137">입력</span><span class="sxs-lookup"><span data-stu-id="57b85-137">INPUTS</span></span>

### <span data-ttu-id="57b85-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="57b85-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="57b85-139">System.String</span><span class="sxs-lookup"><span data-stu-id="57b85-139">System.String</span></span>

## <span data-ttu-id="57b85-140">출력</span><span class="sxs-lookup"><span data-stu-id="57b85-140">OUTPUTS</span></span>

### <span data-ttu-id="57b85-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57b85-141">System.Boolean</span></span>

## <span data-ttu-id="57b85-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="57b85-142">NOTES</span></span>

## <span data-ttu-id="57b85-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57b85-143">RELATED LINKS</span></span>