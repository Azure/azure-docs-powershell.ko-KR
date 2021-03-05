---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
ms.openlocfilehash: c5e31e1f1fcaf4e889e0b1f3bb85b55a4b0388b0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012080"
---
# <span data-ttu-id="76b73-101">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="76b73-101">Set-AzIotHubModule</span></span>

## <span data-ttu-id="76b73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76b73-102">SYNOPSIS</span></span>
<span data-ttu-id="76b73-103">IoT Hub의 대상 IoT 디바이스에서 모듈을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="76b73-103">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="76b73-104">구문</span><span class="sxs-lookup"><span data-stu-id="76b73-104">SYNTAX</span></span>

### <span data-ttu-id="76b73-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="76b73-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76b73-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="76b73-106">InputObjectSet</span></span>
```
Set-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76b73-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="76b73-107">ResourceIdSet</span></span>
```
Set-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76b73-108">설명</span><span class="sxs-lookup"><span data-stu-id="76b73-108">DESCRIPTION</span></span>
<span data-ttu-id="76b73-109">IoT Hub의 대상 IoT 디바이스에서 모듈을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="76b73-109">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="76b73-110">예제</span><span class="sxs-lookup"><span data-stu-id="76b73-110">EXAMPLES</span></span>

### <span data-ttu-id="76b73-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="76b73-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod "shared_private_key"

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

<span data-ttu-id="76b73-112">Iot 디바이스 모듈의 권한 부여 유형을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="76b73-112">Update authorization type of an Iot device module.</span></span>

## <span data-ttu-id="76b73-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="76b73-113">PARAMETERS</span></span>

### <span data-ttu-id="76b73-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="76b73-114">-AuthMethod</span></span>
<span data-ttu-id="76b73-115">엔터티를 만들 권한 부여 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="76b73-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="76b73-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76b73-116">-DefaultProfile</span></span>
<span data-ttu-id="76b73-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76b73-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76b73-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="76b73-118">-DeviceId</span></span>
<span data-ttu-id="76b73-119">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="76b73-119">Target Device Id.</span></span>

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

### <span data-ttu-id="76b73-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76b73-120">-InputObject</span></span>
<span data-ttu-id="76b73-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="76b73-121">IotHub object</span></span>

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

### <span data-ttu-id="76b73-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="76b73-122">-IotHubName</span></span>
<span data-ttu-id="76b73-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="76b73-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="76b73-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="76b73-124">-ModuleId</span></span>
<span data-ttu-id="76b73-125">대상 모듈 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="76b73-125">Target Module Id.</span></span>

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

### <span data-ttu-id="76b73-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="76b73-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="76b73-127">기본 키에 사용할 명시적 자체 서명된 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="76b73-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="76b73-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76b73-128">-ResourceGroupName</span></span>
<span data-ttu-id="76b73-129">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="76b73-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="76b73-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76b73-130">-ResourceId</span></span>
<span data-ttu-id="76b73-131">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="76b73-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="76b73-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="76b73-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="76b73-133">보조 키에 사용할 명시적 자체 서명된 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="76b73-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="76b73-134">-확인</span><span class="sxs-lookup"><span data-stu-id="76b73-134">-Confirm</span></span>
<span data-ttu-id="76b73-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="76b73-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76b73-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76b73-136">-WhatIf</span></span>
<span data-ttu-id="76b73-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="76b73-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76b73-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76b73-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76b73-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b73-139">CommonParameters</span></span>
<span data-ttu-id="76b73-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76b73-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b73-141">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76b73-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b73-142">입력</span><span class="sxs-lookup"><span data-stu-id="76b73-142">INPUTS</span></span>

### <span data-ttu-id="76b73-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="76b73-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="76b73-144">System.String</span><span class="sxs-lookup"><span data-stu-id="76b73-144">System.String</span></span>

## <span data-ttu-id="76b73-145">출력</span><span class="sxs-lookup"><span data-stu-id="76b73-145">OUTPUTS</span></span>

### <span data-ttu-id="76b73-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span><span class="sxs-lookup"><span data-stu-id="76b73-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="76b73-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="76b73-147">NOTES</span></span>

## <span data-ttu-id="76b73-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76b73-148">RELATED LINKS</span></span>