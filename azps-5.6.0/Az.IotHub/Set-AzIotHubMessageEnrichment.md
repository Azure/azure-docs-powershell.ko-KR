---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 0e9b26b4bd22d167dffbee4449aa811381960732
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004128"
---
# <span data-ttu-id="d4e31-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d4e31-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="d4e31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4e31-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e31-103">IoT Hub에서 메시지 보강을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e31-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="d4e31-104">구문</span><span class="sxs-lookup"><span data-stu-id="d4e31-104">SYNTAX</span></span>

### <span data-ttu-id="d4e31-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d4e31-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e31-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d4e31-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e31-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d4e31-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4e31-108">설명</span><span class="sxs-lookup"><span data-stu-id="d4e31-108">DESCRIPTION</span></span>
<span data-ttu-id="d4e31-109">Azure IoT Hub의 메시지 보강에 대한 자세한 설명은 https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="d4e31-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="d4e31-110">예제</span><span class="sxs-lookup"><span data-stu-id="d4e31-110">EXAMPLES</span></span>

### <span data-ttu-id="d4e31-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d4e31-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="d4e31-112">키 "newKey"에 대한 보강 값을 "updatedValue"로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e31-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="d4e31-113">Azure IoT Hub의 메시지 보강에 대한 자세한 설명은 https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="d4e31-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="d4e31-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="d4e31-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="d4e31-115">보강의 엔드포인트를 키 "newKey"에 대해 "엔드포인트1, 엔드포인트2, 엔드포인트3"으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e31-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="d4e31-116">Azure IoT Hub의 메시지 보강에 대한 자세한 설명은 https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="d4e31-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="d4e31-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d4e31-117">PARAMETERS</span></span>

### <span data-ttu-id="d4e31-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e31-118">-DefaultProfile</span></span>
<span data-ttu-id="d4e31-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e31-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4e31-120">-엔드포인트</span><span class="sxs-lookup"><span data-stu-id="d4e31-120">-Endpoint</span></span>
<span data-ttu-id="d4e31-121">엔드포인트를 적용하여 보강을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e31-121">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e31-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4e31-122">-InputObject</span></span>
<span data-ttu-id="d4e31-123">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="d4e31-123">IotHub Object</span></span>

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

### <span data-ttu-id="d4e31-124">-Key</span><span class="sxs-lookup"><span data-stu-id="d4e31-124">-Key</span></span>
<span data-ttu-id="d4e31-125">보강의 키입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e31-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="d4e31-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d4e31-126">-Name</span></span>
<span data-ttu-id="d4e31-127">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="d4e31-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d4e31-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e31-128">-ResourceGroupName</span></span>
<span data-ttu-id="d4e31-129">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="d4e31-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d4e31-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4e31-130">-ResourceId</span></span>
<span data-ttu-id="d4e31-131">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d4e31-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d4e31-132">-Value</span><span class="sxs-lookup"><span data-stu-id="d4e31-132">-Value</span></span>
<span data-ttu-id="d4e31-133">보강의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e31-133">The enrichment's value.</span></span>

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

### <span data-ttu-id="d4e31-134">-확인</span><span class="sxs-lookup"><span data-stu-id="d4e31-134">-Confirm</span></span>
<span data-ttu-id="d4e31-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4e31-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4e31-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e31-136">-WhatIf</span></span>
<span data-ttu-id="d4e31-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d4e31-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4e31-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4e31-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4e31-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e31-139">CommonParameters</span></span>
<span data-ttu-id="d4e31-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e31-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e31-141">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d4e31-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e31-142">입력</span><span class="sxs-lookup"><span data-stu-id="d4e31-142">INPUTS</span></span>

### <span data-ttu-id="d4e31-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d4e31-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d4e31-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d4e31-144">System.String</span></span>

## <span data-ttu-id="d4e31-145">출력</span><span class="sxs-lookup"><span data-stu-id="d4e31-145">OUTPUTS</span></span>

### <span data-ttu-id="d4e31-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="d4e31-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="d4e31-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d4e31-147">NOTES</span></span>

## <span data-ttu-id="d4e31-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4e31-148">RELATED LINKS</span></span>
