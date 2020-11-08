---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: ce1fe3b50d8198dd9ee1965a3a3ab7a2409e1145
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213614"
---
# <span data-ttu-id="49387-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="49387-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="49387-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49387-102">SYNOPSIS</span></span>
<span data-ttu-id="49387-103">장치 등록 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="49387-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="49387-104">구문과</span><span class="sxs-lookup"><span data-stu-id="49387-104">SYNTAX</span></span>

### <span data-ttu-id="49387-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="49387-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49387-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="49387-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49387-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="49387-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49387-108">설명은</span><span class="sxs-lookup"><span data-stu-id="49387-108">DESCRIPTION</span></span>
<span data-ttu-id="49387-109">Azure IoT Hub 디바이스 프로비저닝 서비스에서 등록 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="49387-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="49387-110">예제의</span><span class="sxs-lookup"><span data-stu-id="49387-110">EXAMPLES</span></span>

### <span data-ttu-id="49387-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="49387-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="49387-112">지정 된 등록 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="49387-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="49387-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="49387-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="49387-114">모든 등록 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="49387-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="49387-115">변수</span><span class="sxs-lookup"><span data-stu-id="49387-115">PARAMETERS</span></span>

### <span data-ttu-id="49387-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49387-116">-DefaultProfile</span></span>
<span data-ttu-id="49387-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49387-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49387-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="49387-118">-DpsName</span></span>
<span data-ttu-id="49387-119">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="49387-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="49387-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="49387-120">-DpsObject</span></span>
<span data-ttu-id="49387-121">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="49387-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="49387-122">-이름</span><span class="sxs-lookup"><span data-stu-id="49387-122">-Name</span></span>
<span data-ttu-id="49387-123">등록 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49387-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="49387-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49387-124">-PassThru</span></span>
<span data-ttu-id="49387-125">Boolean 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49387-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="49387-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49387-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="49387-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49387-127">-ResourceGroupName</span></span>
<span data-ttu-id="49387-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49387-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="49387-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49387-129">-ResourceId</span></span>
<span data-ttu-id="49387-130">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="49387-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="49387-131">-확인</span><span class="sxs-lookup"><span data-stu-id="49387-131">-Confirm</span></span>
<span data-ttu-id="49387-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="49387-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49387-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49387-133">-WhatIf</span></span>
<span data-ttu-id="49387-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="49387-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49387-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49387-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49387-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49387-136">CommonParameters</span></span>
<span data-ttu-id="49387-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="49387-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49387-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49387-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49387-139">입력</span><span class="sxs-lookup"><span data-stu-id="49387-139">INPUTS</span></span>

### <span data-ttu-id="49387-140">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="49387-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="49387-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="49387-141">System.String</span></span>

## <span data-ttu-id="49387-142">출력</span><span class="sxs-lookup"><span data-stu-id="49387-142">OUTPUTS</span></span>

### <span data-ttu-id="49387-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="49387-143">System.Boolean</span></span>

## <span data-ttu-id="49387-144">상속자</span><span class="sxs-lookup"><span data-stu-id="49387-144">NOTES</span></span>

## <span data-ttu-id="49387-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49387-145">RELATED LINKS</span></span>
