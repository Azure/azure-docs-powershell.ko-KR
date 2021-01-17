---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8b16d95d582e29be6f49cac9eaeb00bcda67de0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340953"
---
# <span data-ttu-id="cb87a-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="cb87a-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="cb87a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb87a-102">SYNOPSIS</span></span>
<span data-ttu-id="cb87a-103">디바이스 등록 레코드를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="cb87a-103">Delete a device enrollment record.</span></span>

## <span data-ttu-id="cb87a-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb87a-104">SYNTAX</span></span>

### <span data-ttu-id="cb87a-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="cb87a-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb87a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cb87a-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb87a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cb87a-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb87a-108">설명</span><span class="sxs-lookup"><span data-stu-id="cb87a-108">DESCRIPTION</span></span>
<span data-ttu-id="cb87a-109">Azure IoT Hub Device Provisioning Service에서 디바이스 등록을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="cb87a-109">Delete a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="cb87a-110">예제</span><span class="sxs-lookup"><span data-stu-id="cb87a-110">EXAMPLES</span></span>

### <span data-ttu-id="cb87a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cb87a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="cb87a-112">지정된 등록 레코드를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="cb87a-112">Delete a specified enrollment record.</span></span>

### <span data-ttu-id="cb87a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="cb87a-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="cb87a-114">모든 등록 레코드를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="cb87a-114">Delete all enrollment records.</span></span>

## <span data-ttu-id="cb87a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb87a-115">PARAMETERS</span></span>

### <span data-ttu-id="cb87a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb87a-116">-DefaultProfile</span></span>
<span data-ttu-id="cb87a-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb87a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb87a-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="cb87a-118">-DpsName</span></span>
<span data-ttu-id="cb87a-119">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="cb87a-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="cb87a-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="cb87a-120">-DpsObject</span></span>
<span data-ttu-id="cb87a-121">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="cb87a-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="cb87a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb87a-122">-PassThru</span></span>
<span data-ttu-id="cb87a-123">부울 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb87a-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="cb87a-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb87a-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cb87a-125">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="cb87a-125">-RegistrationId</span></span>
<span data-ttu-id="cb87a-126">개별 등록 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cb87a-126">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="cb87a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb87a-127">-ResourceGroupName</span></span>
<span data-ttu-id="cb87a-128">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="cb87a-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cb87a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb87a-129">-ResourceId</span></span>
<span data-ttu-id="cb87a-130">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="cb87a-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="cb87a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb87a-131">-Confirm</span></span>
<span data-ttu-id="cb87a-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb87a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb87a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb87a-133">-WhatIf</span></span>
<span data-ttu-id="cb87a-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cb87a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb87a-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb87a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb87a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb87a-136">CommonParameters</span></span>
<span data-ttu-id="cb87a-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb87a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb87a-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb87a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb87a-139">입력</span><span class="sxs-lookup"><span data-stu-id="cb87a-139">INPUTS</span></span>

### <span data-ttu-id="cb87a-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="cb87a-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="cb87a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="cb87a-141">System.String</span></span>

## <span data-ttu-id="cb87a-142">출력</span><span class="sxs-lookup"><span data-stu-id="cb87a-142">OUTPUTS</span></span>

### <span data-ttu-id="cb87a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb87a-143">System.Boolean</span></span>

## <span data-ttu-id="cb87a-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb87a-144">NOTES</span></span>

## <span data-ttu-id="cb87a-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb87a-145">RELATED LINKS</span></span>
