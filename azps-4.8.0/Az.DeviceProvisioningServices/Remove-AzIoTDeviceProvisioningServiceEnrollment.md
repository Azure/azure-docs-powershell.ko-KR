---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8b16d95d582e29be6f49cac9eaeb00bcda67de0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213609"
---
# <span data-ttu-id="57059-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="57059-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="57059-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57059-102">SYNOPSIS</span></span>
<span data-ttu-id="57059-103">장치 등록 레코드를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="57059-103">Delete a device enrollment record.</span></span>

## <span data-ttu-id="57059-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57059-104">SYNTAX</span></span>

### <span data-ttu-id="57059-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="57059-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57059-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="57059-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57059-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="57059-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57059-108">설명은</span><span class="sxs-lookup"><span data-stu-id="57059-108">DESCRIPTION</span></span>
<span data-ttu-id="57059-109">Azure IoT Hub 디바이스 프로비저닝 서비스에서 디바이스 등록을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="57059-109">Delete a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="57059-110">예제의</span><span class="sxs-lookup"><span data-stu-id="57059-110">EXAMPLES</span></span>

### <span data-ttu-id="57059-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="57059-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="57059-112">지정 된 등록 레코드를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="57059-112">Delete a specified enrollment record.</span></span>

### <span data-ttu-id="57059-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="57059-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="57059-114">모든 등록 레코드를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="57059-114">Delete all enrollment records.</span></span>

## <span data-ttu-id="57059-115">변수</span><span class="sxs-lookup"><span data-stu-id="57059-115">PARAMETERS</span></span>

### <span data-ttu-id="57059-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57059-116">-DefaultProfile</span></span>
<span data-ttu-id="57059-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57059-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57059-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="57059-118">-DpsName</span></span>
<span data-ttu-id="57059-119">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="57059-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="57059-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="57059-120">-DpsObject</span></span>
<span data-ttu-id="57059-121">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="57059-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="57059-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57059-122">-PassThru</span></span>
<span data-ttu-id="57059-123">Boolean 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57059-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="57059-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57059-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="57059-125">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="57059-125">-RegistrationId</span></span>
<span data-ttu-id="57059-126">개별 등록 등록 id입니다.</span><span class="sxs-lookup"><span data-stu-id="57059-126">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="57059-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57059-127">-ResourceGroupName</span></span>
<span data-ttu-id="57059-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57059-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="57059-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57059-129">-ResourceId</span></span>
<span data-ttu-id="57059-130">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="57059-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="57059-131">-확인</span><span class="sxs-lookup"><span data-stu-id="57059-131">-Confirm</span></span>
<span data-ttu-id="57059-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="57059-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57059-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57059-133">-WhatIf</span></span>
<span data-ttu-id="57059-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="57059-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57059-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57059-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57059-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57059-136">CommonParameters</span></span>
<span data-ttu-id="57059-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57059-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57059-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57059-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57059-139">입력</span><span class="sxs-lookup"><span data-stu-id="57059-139">INPUTS</span></span>

### <span data-ttu-id="57059-140">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="57059-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="57059-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="57059-141">System.String</span></span>

## <span data-ttu-id="57059-142">출력</span><span class="sxs-lookup"><span data-stu-id="57059-142">OUTPUTS</span></span>

### <span data-ttu-id="57059-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="57059-143">System.Boolean</span></span>

## <span data-ttu-id="57059-144">상속자</span><span class="sxs-lookup"><span data-stu-id="57059-144">NOTES</span></span>

## <span data-ttu-id="57059-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57059-145">RELATED LINKS</span></span>
