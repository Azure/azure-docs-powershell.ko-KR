---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 64de44e74b5c6ea21d9d49b1911bcd34a74a374a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702946"
---
# <span data-ttu-id="3edff-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="3edff-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="3edff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3edff-102">SYNOPSIS</span></span>
<span data-ttu-id="3edff-103">Azure IoT Hub 디바이스 프로비저닝 서비스 인증서를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3edff-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3edff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3edff-104">SYNTAX</span></span>

### <span data-ttu-id="3edff-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3edff-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3edff-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3edff-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3edff-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3edff-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3edff-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3edff-108">DESCRIPTION</span></span>
<span data-ttu-id="3edff-109">Azure IoT Hub Device 프로비저닝 서비스의 CA 인증서에 대 한 자세한 설명은을 참조 https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates 하세요.</span><span class="sxs-lookup"><span data-stu-id="3edff-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="3edff-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3edff-110">EXAMPLES</span></span>

### <span data-ttu-id="3edff-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3edff-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="3edff-112">Azure IoT Hub 디바이스 프로비저닝 서비스에서 "mycertificate"를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3edff-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="3edff-113">변수</span><span class="sxs-lookup"><span data-stu-id="3edff-113">PARAMETERS</span></span>

### <span data-ttu-id="3edff-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="3edff-114">-CertificateName</span></span>
<span data-ttu-id="3edff-115">인증서 이름</span><span class="sxs-lookup"><span data-stu-id="3edff-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="3edff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3edff-116">-DefaultProfile</span></span>
<span data-ttu-id="3edff-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3edff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3edff-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="3edff-118">-Etag</span></span>
<span data-ttu-id="3edff-119">인증서의 Etag</span><span class="sxs-lookup"><span data-stu-id="3edff-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="3edff-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3edff-120">-InputObject</span></span>
<span data-ttu-id="3edff-121">IoT Device 프로 비전 서비스 인증서 개체</span><span class="sxs-lookup"><span data-stu-id="3edff-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="3edff-122">-이름</span><span class="sxs-lookup"><span data-stu-id="3edff-122">-Name</span></span>
<span data-ttu-id="3edff-123">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="3edff-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="3edff-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3edff-124">-PassThru</span></span>
<span data-ttu-id="3edff-125">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="3edff-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3edff-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3edff-126">-ResourceGroupName</span></span>
<span data-ttu-id="3edff-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3edff-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3edff-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3edff-128">-ResourceId</span></span>
<span data-ttu-id="3edff-129">IoT Device 프로 비전 서비스 인증서 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="3edff-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="3edff-130">-확인</span><span class="sxs-lookup"><span data-stu-id="3edff-130">-Confirm</span></span>
<span data-ttu-id="3edff-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3edff-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3edff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3edff-132">-WhatIf</span></span>
<span data-ttu-id="3edff-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3edff-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3edff-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3edff-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3edff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3edff-135">CommonParameters</span></span>
<span data-ttu-id="3edff-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3edff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3edff-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3edff-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3edff-138">입력</span><span class="sxs-lookup"><span data-stu-id="3edff-138">INPUTS</span></span>

### <span data-ttu-id="3edff-139">DeviceProvisioningServices. PSCertificateResponse/. \*</span><span class="sxs-lookup"><span data-stu-id="3edff-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="3edff-140">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3edff-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="3edff-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3edff-141">System.String</span></span>

## <span data-ttu-id="3edff-142">출력</span><span class="sxs-lookup"><span data-stu-id="3edff-142">OUTPUTS</span></span>

### <span data-ttu-id="3edff-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="3edff-143">System.Boolean</span></span>

## <span data-ttu-id="3edff-144">상속자</span><span class="sxs-lookup"><span data-stu-id="3edff-144">NOTES</span></span>

## <span data-ttu-id="3edff-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3edff-145">RELATED LINKS</span></span>
