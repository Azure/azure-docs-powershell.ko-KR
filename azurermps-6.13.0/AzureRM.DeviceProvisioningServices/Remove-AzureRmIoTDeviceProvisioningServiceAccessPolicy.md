---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: b3a813623ed11a64a23dc35afe2f81c3f5de61da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532005"
---
# <span data-ttu-id="aa948-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aa948-101">Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="aa948-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa948-102">SYNOPSIS</span></span>
<span data-ttu-id="aa948-103">Azure IoT Hub 디바이스 프로비저닝 서비스에서 공유 액세스 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa948-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa948-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aa948-104">SYNTAX</span></span>

### <span data-ttu-id="aa948-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="aa948-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa948-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aa948-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa948-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="aa948-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa948-108">설명은</span><span class="sxs-lookup"><span data-stu-id="aa948-108">DESCRIPTION</span></span>
<span data-ttu-id="aa948-109">Azure IoT Hub Device 프로비저닝 서비스에 대 한 소개는를 참조 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 하세요.</span><span class="sxs-lookup"><span data-stu-id="aa948-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="aa948-110">예제의</span><span class="sxs-lookup"><span data-stu-id="aa948-110">EXAMPLES</span></span>

### <span data-ttu-id="aa948-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="aa948-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="aa948-112">Azure IoT Hub 디바이스 프로비저닝 서비스에서 공유 액세스 정책 "mypolicy"을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa948-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="aa948-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="aa948-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzureRmIoTDpsAccessPolicy
```

<span data-ttu-id="aa948-114">파이프라인을 사용 하 여 Azure IoT Hub 디바이스 프로비저닝 서비스에서 공유 액세스 정책 "mypolicy"을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa948-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="aa948-115">변수</span><span class="sxs-lookup"><span data-stu-id="aa948-115">PARAMETERS</span></span>

### <span data-ttu-id="aa948-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa948-116">-DefaultProfile</span></span>
<span data-ttu-id="aa948-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa948-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa948-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa948-118">-InputObject</span></span>
<span data-ttu-id="aa948-119">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="aa948-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa948-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="aa948-120">-KeyName</span></span>
<span data-ttu-id="aa948-121">IoT Device 프로 비전 서비스 액세스 정책 키 이름</span><span class="sxs-lookup"><span data-stu-id="aa948-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="aa948-122">-이름</span><span class="sxs-lookup"><span data-stu-id="aa948-122">-Name</span></span>
<span data-ttu-id="aa948-123">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="aa948-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="aa948-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa948-124">-PassThru</span></span>
<span data-ttu-id="aa948-125">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="aa948-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="aa948-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa948-126">-ResourceGroupName</span></span>
<span data-ttu-id="aa948-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa948-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="aa948-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa948-128">-ResourceId</span></span>
<span data-ttu-id="aa948-129">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="aa948-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="aa948-130">-확인</span><span class="sxs-lookup"><span data-stu-id="aa948-130">-Confirm</span></span>
<span data-ttu-id="aa948-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa948-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa948-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa948-132">-WhatIf</span></span>
<span data-ttu-id="aa948-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aa948-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa948-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa948-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa948-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa948-135">CommonParameters</span></span>
<span data-ttu-id="aa948-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa948-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa948-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa948-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa948-138">입력</span><span class="sxs-lookup"><span data-stu-id="aa948-138">INPUTS</span></span>

### <span data-ttu-id="aa948-139">DeviceProvisioningServices. Pssharedaccess서명 Authorizationrule를 Accessrightsdescription</span><span class="sxs-lookup"><span data-stu-id="aa948-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>
<span data-ttu-id="aa948-140">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aa948-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="aa948-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aa948-141">System.String</span></span>

## <span data-ttu-id="aa948-142">출력</span><span class="sxs-lookup"><span data-stu-id="aa948-142">OUTPUTS</span></span>

### <span data-ttu-id="aa948-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="aa948-143">System.Boolean</span></span>

## <span data-ttu-id="aa948-144">상속자</span><span class="sxs-lookup"><span data-stu-id="aa948-144">NOTES</span></span>

## <span data-ttu-id="aa948-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa948-145">RELATED LINKS</span></span>
