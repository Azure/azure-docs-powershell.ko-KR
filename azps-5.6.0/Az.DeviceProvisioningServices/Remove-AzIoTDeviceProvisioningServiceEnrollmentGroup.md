---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 9b27875e19837d7e3b69770234bdcd19648c3130
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985161"
---
# <span data-ttu-id="dbe20-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="dbe20-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="dbe20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbe20-102">SYNOPSIS</span></span>
<span data-ttu-id="dbe20-103">디바이스 등록 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe20-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="dbe20-104">구문</span><span class="sxs-lookup"><span data-stu-id="dbe20-104">SYNTAX</span></span>

### <span data-ttu-id="dbe20-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="dbe20-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbe20-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dbe20-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbe20-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dbe20-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbe20-108">설명</span><span class="sxs-lookup"><span data-stu-id="dbe20-108">DESCRIPTION</span></span>
<span data-ttu-id="dbe20-109">Azure IoT Hub 디바이스 프로비전 서비스에서 등록 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe20-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="dbe20-110">예제</span><span class="sxs-lookup"><span data-stu-id="dbe20-110">EXAMPLES</span></span>

### <span data-ttu-id="dbe20-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="dbe20-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="dbe20-112">지정된 등록 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe20-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="dbe20-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="dbe20-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="dbe20-114">모든 등록 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe20-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="dbe20-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="dbe20-115">PARAMETERS</span></span>

### <span data-ttu-id="dbe20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbe20-116">-DefaultProfile</span></span>
<span data-ttu-id="dbe20-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dbe20-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbe20-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="dbe20-118">-DpsName</span></span>
<span data-ttu-id="dbe20-119">IoT 디바이스 프로비전 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="dbe20-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="dbe20-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="dbe20-120">-DpsObject</span></span>
<span data-ttu-id="dbe20-121">IoT 디바이스 프로비전 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="dbe20-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="dbe20-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dbe20-122">-Name</span></span>
<span data-ttu-id="dbe20-123">등록 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dbe20-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="dbe20-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbe20-124">-PassThru</span></span>
<span data-ttu-id="dbe20-125">부울 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dbe20-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="dbe20-126">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dbe20-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dbe20-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbe20-127">-ResourceGroupName</span></span>
<span data-ttu-id="dbe20-128">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="dbe20-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dbe20-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbe20-129">-ResourceId</span></span>
<span data-ttu-id="dbe20-130">IoT 디바이스 프로비전 서비스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="dbe20-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="dbe20-131">-확인</span><span class="sxs-lookup"><span data-stu-id="dbe20-131">-Confirm</span></span>
<span data-ttu-id="dbe20-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dbe20-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbe20-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbe20-133">-WhatIf</span></span>
<span data-ttu-id="dbe20-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="dbe20-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbe20-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dbe20-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbe20-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbe20-136">CommonParameters</span></span>
<span data-ttu-id="dbe20-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe20-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbe20-138">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dbe20-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbe20-139">입력</span><span class="sxs-lookup"><span data-stu-id="dbe20-139">INPUTS</span></span>

### <span data-ttu-id="dbe20-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="dbe20-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="dbe20-141">System.String</span><span class="sxs-lookup"><span data-stu-id="dbe20-141">System.String</span></span>

## <span data-ttu-id="dbe20-142">출력</span><span class="sxs-lookup"><span data-stu-id="dbe20-142">OUTPUTS</span></span>

### <span data-ttu-id="dbe20-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dbe20-143">System.Boolean</span></span>

## <span data-ttu-id="dbe20-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dbe20-144">NOTES</span></span>

## <span data-ttu-id="dbe20-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbe20-145">RELATED LINKS</span></span>
