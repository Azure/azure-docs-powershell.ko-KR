---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
ms.openlocfilehash: 44e6451542a75e97a57890261a9a5f312e5ec466
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200145"
---
# <span data-ttu-id="9b402-101">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="9b402-101">Add-AzIotHubModule</span></span>

## <span data-ttu-id="9b402-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b402-102">SYNOPSIS</span></span>
<span data-ttu-id="9b402-103">IoT Hub의 대상 IoT 디바이스에 모듈을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b402-103">Create a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="9b402-104">구문</span><span class="sxs-lookup"><span data-stu-id="9b402-104">SYNTAX</span></span>

### <span data-ttu-id="9b402-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9b402-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b402-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9b402-106">InputObjectSet</span></span>
```
Add-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b402-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9b402-107">ResourceIdSet</span></span>
```
Add-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b402-108">설명</span><span class="sxs-lookup"><span data-stu-id="9b402-108">DESCRIPTION</span></span>
<span data-ttu-id="9b402-109">IoT Hub에서 다른 권한 부여 유형을 사용하여 대상 IoT 디바이스에 모듈을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b402-109">Create a module on a target IoT device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="9b402-110">예제</span><span class="sxs-lookup"><span data-stu-id="9b402-110">EXAMPLES</span></span>

### <span data-ttu-id="9b402-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9b402-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod shared_private_key

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  : 
```

<span data-ttu-id="9b402-112">기본 권한 부여(공유 개인 키)를 사용하여 대상 IoT 디바이스에 모듈을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b402-112">Create a module on a target IoT device with default authorization (shared private key).</span></span>

## <span data-ttu-id="9b402-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b402-113">PARAMETERS</span></span>

### <span data-ttu-id="9b402-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="9b402-114">-AuthMethod</span></span>
<span data-ttu-id="9b402-115">엔터티를 만들 권한 부여 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="9b402-115">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b402-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b402-116">-DefaultProfile</span></span>
<span data-ttu-id="9b402-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b402-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b402-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="9b402-118">-DeviceId</span></span>
<span data-ttu-id="9b402-119">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9b402-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b402-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b402-120">-InputObject</span></span>
<span data-ttu-id="9b402-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="9b402-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b402-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9b402-122">-IotHubName</span></span>
<span data-ttu-id="9b402-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="9b402-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9b402-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="9b402-124">-ModuleId</span></span>
<span data-ttu-id="9b402-125">대상 모듈 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9b402-125">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b402-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="9b402-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="9b402-127">기본 키에 사용할 명시적 자체 서명된 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="9b402-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="9b402-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b402-128">-ResourceGroupName</span></span>
<span data-ttu-id="9b402-129">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="9b402-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9b402-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b402-130">-ResourceId</span></span>
<span data-ttu-id="9b402-131">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9b402-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9b402-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="9b402-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="9b402-133">보조 키에 사용할 명시적 자체 서명된 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="9b402-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b402-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b402-134">-Confirm</span></span>
<span data-ttu-id="9b402-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b402-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b402-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b402-136">-WhatIf</span></span>
<span data-ttu-id="9b402-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9b402-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b402-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b402-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b402-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b402-139">CommonParameters</span></span>
<span data-ttu-id="9b402-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9b402-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b402-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9b402-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b402-142">입력</span><span class="sxs-lookup"><span data-stu-id="9b402-142">INPUTS</span></span>

### <span data-ttu-id="9b402-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9b402-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9b402-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9b402-144">System.String</span></span>

## <span data-ttu-id="9b402-145">출력</span><span class="sxs-lookup"><span data-stu-id="9b402-145">OUTPUTS</span></span>

### <span data-ttu-id="9b402-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span><span class="sxs-lookup"><span data-stu-id="9b402-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="9b402-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9b402-147">NOTES</span></span>

## <span data-ttu-id="9b402-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b402-148">RELATED LINKS</span></span>