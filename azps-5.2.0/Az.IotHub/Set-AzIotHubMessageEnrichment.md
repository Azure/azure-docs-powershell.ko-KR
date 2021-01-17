---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 3420c4103f8e502b2d8ca208dd107ced629c0f3a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332198"
---
# <span data-ttu-id="9abf9-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="9abf9-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="9abf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9abf9-102">SYNOPSIS</span></span>
<span data-ttu-id="9abf9-103">IoT Hub에서 메시지 보강을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9abf9-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="9abf9-104">구문</span><span class="sxs-lookup"><span data-stu-id="9abf9-104">SYNTAX</span></span>

### <span data-ttu-id="9abf9-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9abf9-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9abf9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9abf9-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9abf9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9abf9-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9abf9-108">설명</span><span class="sxs-lookup"><span data-stu-id="9abf9-108">DESCRIPTION</span></span>
<span data-ttu-id="9abf9-109">Azure IoT Hub의 메시지 보강에 대한 자세한 설명은 다음을 참조하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="9abf9-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="9abf9-110">예제</span><span class="sxs-lookup"><span data-stu-id="9abf9-110">EXAMPLES</span></span>

### <span data-ttu-id="9abf9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9abf9-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="9abf9-112">보강의 값을 키 "newKey"에 대한 "updatedValue"로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9abf9-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="9abf9-113">Azure IoT Hub의 메시지 보강에 대한 자세한 설명은 다음을 참조하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="9abf9-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="9abf9-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="9abf9-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="9abf9-115">보강의 엔드포인트를 키 "newKey"에 대한 "endpoint1, endpoint2, endpoint3"으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9abf9-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="9abf9-116">Azure IoT Hub의 메시지 보강에 대한 자세한 설명은 다음을 참조하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="9abf9-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="9abf9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9abf9-117">PARAMETERS</span></span>

### <span data-ttu-id="9abf9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9abf9-118">-DefaultProfile</span></span>
<span data-ttu-id="9abf9-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9abf9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9abf9-120">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="9abf9-120">-Endpoint</span></span>
<span data-ttu-id="9abf9-121">보강을 적용할 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="9abf9-121">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="9abf9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9abf9-122">-InputObject</span></span>
<span data-ttu-id="9abf9-123">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="9abf9-123">IotHub Object</span></span>

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

### <span data-ttu-id="9abf9-124">-Key</span><span class="sxs-lookup"><span data-stu-id="9abf9-124">-Key</span></span>
<span data-ttu-id="9abf9-125">보강의 키입니다.</span><span class="sxs-lookup"><span data-stu-id="9abf9-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="9abf9-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9abf9-126">-Name</span></span>
<span data-ttu-id="9abf9-127">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="9abf9-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9abf9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9abf9-128">-ResourceGroupName</span></span>
<span data-ttu-id="9abf9-129">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="9abf9-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9abf9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9abf9-130">-ResourceId</span></span>
<span data-ttu-id="9abf9-131">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9abf9-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9abf9-132">-Value</span><span class="sxs-lookup"><span data-stu-id="9abf9-132">-Value</span></span>
<span data-ttu-id="9abf9-133">보강의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9abf9-133">The enrichment's value.</span></span>

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

### <span data-ttu-id="9abf9-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9abf9-134">-Confirm</span></span>
<span data-ttu-id="9abf9-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9abf9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9abf9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9abf9-136">-WhatIf</span></span>
<span data-ttu-id="9abf9-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9abf9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9abf9-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9abf9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9abf9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9abf9-139">CommonParameters</span></span>
<span data-ttu-id="9abf9-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9abf9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9abf9-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9abf9-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9abf9-142">입력</span><span class="sxs-lookup"><span data-stu-id="9abf9-142">INPUTS</span></span>

### <span data-ttu-id="9abf9-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9abf9-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9abf9-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9abf9-144">System.String</span></span>

## <span data-ttu-id="9abf9-145">출력</span><span class="sxs-lookup"><span data-stu-id="9abf9-145">OUTPUTS</span></span>

### <span data-ttu-id="9abf9-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="9abf9-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="9abf9-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9abf9-147">NOTES</span></span>

## <span data-ttu-id="9abf9-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9abf9-148">RELATED LINKS</span></span>
