---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 566594fef5741808e4f27ccb6d1996783b5c880b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489880"
---
# <span data-ttu-id="95fd3-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="95fd3-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="95fd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="95fd3-103">Azure IoT Hub Device Provisioning Service 인증서를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="95fd3-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="95fd3-104">구문</span><span class="sxs-lookup"><span data-stu-id="95fd3-104">SYNTAX</span></span>

### <span data-ttu-id="95fd3-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="95fd3-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95fd3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="95fd3-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95fd3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="95fd3-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95fd3-108">설명</span><span class="sxs-lookup"><span data-stu-id="95fd3-108">DESCRIPTION</span></span>
<span data-ttu-id="95fd3-109">Azure IoT Hub Device Provisioning Service의 CA 인증서에 대한 자세한 설명은 https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="95fd3-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="95fd3-110">예제</span><span class="sxs-lookup"><span data-stu-id="95fd3-110">EXAMPLES</span></span>

### <span data-ttu-id="95fd3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="95fd3-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="95fd3-112">Azure IoT Hub 디바이스 프로비전 서비스에서 "mycertificate"를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="95fd3-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="95fd3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95fd3-113">PARAMETERS</span></span>

### <span data-ttu-id="95fd3-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="95fd3-114">-CertificateName</span></span>
<span data-ttu-id="95fd3-115">인증서의 이름</span><span class="sxs-lookup"><span data-stu-id="95fd3-115">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95fd3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95fd3-116">-DefaultProfile</span></span>
<span data-ttu-id="95fd3-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95fd3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95fd3-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="95fd3-118">-Etag</span></span>
<span data-ttu-id="95fd3-119">인증서의 Etag</span><span class="sxs-lookup"><span data-stu-id="95fd3-119">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95fd3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95fd3-120">-InputObject</span></span>
<span data-ttu-id="95fd3-121">IoT Device Provisioning Service Certificate 개체</span><span class="sxs-lookup"><span data-stu-id="95fd3-121">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95fd3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="95fd3-122">-Name</span></span>
<span data-ttu-id="95fd3-123">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="95fd3-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="95fd3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95fd3-124">-PassThru</span></span>
<span data-ttu-id="95fd3-125">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="95fd3-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="95fd3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95fd3-126">-ResourceGroupName</span></span>
<span data-ttu-id="95fd3-127">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="95fd3-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="95fd3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95fd3-128">-ResourceId</span></span>
<span data-ttu-id="95fd3-129">IoT Device Provisioning Service 인증서 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="95fd3-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="95fd3-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95fd3-130">-Confirm</span></span>
<span data-ttu-id="95fd3-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="95fd3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95fd3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95fd3-132">-WhatIf</span></span>
<span data-ttu-id="95fd3-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="95fd3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95fd3-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95fd3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95fd3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95fd3-135">CommonParameters</span></span>
<span data-ttu-id="95fd3-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="95fd3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95fd3-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="95fd3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95fd3-138">입력</span><span class="sxs-lookup"><span data-stu-id="95fd3-138">INPUTS</span></span>

### <span data-ttu-id="95fd3-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="95fd3-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="95fd3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="95fd3-140">System.String</span></span>

## <span data-ttu-id="95fd3-141">출력</span><span class="sxs-lookup"><span data-stu-id="95fd3-141">OUTPUTS</span></span>

### <span data-ttu-id="95fd3-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="95fd3-142">System.Boolean</span></span>

## <span data-ttu-id="95fd3-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="95fd3-143">NOTES</span></span>

## <span data-ttu-id="95fd3-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95fd3-144">RELATED LINKS</span></span>
