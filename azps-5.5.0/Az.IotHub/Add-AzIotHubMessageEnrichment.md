---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 04c65bf74d6c32dcaf93d2183936f9c0980aae4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188244"
---
# <span data-ttu-id="e9a36-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e9a36-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="e9a36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9a36-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a36-103">IoT Hub에서 선택한 엔드포인트에 대한 메시지 보강을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9a36-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="e9a36-104">구문</span><span class="sxs-lookup"><span data-stu-id="e9a36-104">SYNTAX</span></span>

### <span data-ttu-id="e9a36-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e9a36-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9a36-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e9a36-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9a36-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e9a36-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9a36-108">설명</span><span class="sxs-lookup"><span data-stu-id="e9a36-108">DESCRIPTION</span></span>
<span data-ttu-id="e9a36-109">IoT Hub당 최대 10개 메시지 보강을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a36-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="e9a36-110">이러한 속성은 선택한 엔드포인트로 전송된 메시지에 애플리케이션 속성으로 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9a36-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="e9a36-111">자세한 내용은 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="e9a36-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="e9a36-112">예제</span><span class="sxs-lookup"><span data-stu-id="e9a36-112">EXAMPLES</span></span>

### <span data-ttu-id="e9a36-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9a36-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="e9a36-114">키 "newKey" 및 값 "newValue"로 새 보강을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a36-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="e9a36-115">이 새로운 보강은 "endpoint1" 및 "endpoint2" 엔드포인트에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9a36-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="e9a36-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9a36-116">PARAMETERS</span></span>

### <span data-ttu-id="e9a36-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9a36-117">-DefaultProfile</span></span>
<span data-ttu-id="e9a36-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a36-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9a36-119">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="e9a36-119">-Endpoint</span></span>
<span data-ttu-id="e9a36-120">보강을 적용할 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a36-120">Endpoint(s) to apply enrichments to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9a36-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9a36-121">-InputObject</span></span>
<span data-ttu-id="e9a36-122">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="e9a36-122">IotHub object</span></span>

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

### <span data-ttu-id="e9a36-123">-Key</span><span class="sxs-lookup"><span data-stu-id="e9a36-123">-Key</span></span>
<span data-ttu-id="e9a36-124">보강의 키입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a36-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="e9a36-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e9a36-125">-Name</span></span>
<span data-ttu-id="e9a36-126">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="e9a36-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e9a36-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9a36-127">-ResourceGroupName</span></span>
<span data-ttu-id="e9a36-128">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="e9a36-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e9a36-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9a36-129">-ResourceId</span></span>
<span data-ttu-id="e9a36-130">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e9a36-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e9a36-131">-Value</span><span class="sxs-lookup"><span data-stu-id="e9a36-131">-Value</span></span>
<span data-ttu-id="e9a36-132">보강의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a36-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="e9a36-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9a36-133">-Confirm</span></span>
<span data-ttu-id="e9a36-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9a36-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9a36-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9a36-135">-WhatIf</span></span>
<span data-ttu-id="e9a36-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e9a36-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9a36-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9a36-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9a36-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9a36-138">CommonParameters</span></span>
<span data-ttu-id="e9a36-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a36-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a36-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e9a36-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a36-141">입력</span><span class="sxs-lookup"><span data-stu-id="e9a36-141">INPUTS</span></span>

### <span data-ttu-id="e9a36-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e9a36-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e9a36-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e9a36-143">System.String</span></span>

## <span data-ttu-id="e9a36-144">출력</span><span class="sxs-lookup"><span data-stu-id="e9a36-144">OUTPUTS</span></span>

### <span data-ttu-id="e9a36-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="e9a36-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="e9a36-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e9a36-146">NOTES</span></span>

## <span data-ttu-id="e9a36-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9a36-147">RELATED LINKS</span></span>
