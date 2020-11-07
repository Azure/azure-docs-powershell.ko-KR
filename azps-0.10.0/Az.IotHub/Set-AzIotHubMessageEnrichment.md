---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 4ecbbe9f37e4a2adf8d5ae5a06ef631d7a3b34cc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875852"
---
# <span data-ttu-id="c7bc9-101">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="c7bc9-101">Set-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="c7bc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="c7bc9-103">IoT hub의 메시지 보강를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bc9-103">Update a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="c7bc9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c7bc9-104">SYNTAX</span></span>

### <span data-ttu-id="c7bc9-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c7bc9-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7bc9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c7bc9-106">InputObjectSet</span></span>
```
Set-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> [-Value <String>]
 [-Endpoint <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7bc9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c7bc9-107">ResourceIdSet</span></span>
```
Set-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> [-Value <String>] [-Endpoint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7bc9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c7bc9-108">DESCRIPTION</span></span>
<span data-ttu-id="c7bc9-109">Azure IoT Hub의 메시지 enrichments에 대 한 자세한 설명은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="c7bc9-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="c7bc9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c7bc9-110">EXAMPLES</span></span>

### <span data-ttu-id="c7bc9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c7bc9-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "updatedValue"

Key         : newKey
Value       : updatedValue
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="c7bc9-112">"NewKey" 키에 대 한 보강 값을 "updatedValue"로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bc9-112">Updates enrichment's value to "updatedValue" for the key "newKey".</span></span>
<span data-ttu-id="c7bc9-113">Azure IoT Hub의 메시지 enrichments에 대 한 자세한 설명은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="c7bc9-113">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

### <span data-ttu-id="c7bc9-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="c7bc9-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Endpoint endpoint1,endpoint2,endpoint3

Key         : newKey
Value       : value1
Endpoint(s) : {endpoint1, endpoint2, endpoint3}
```

<span data-ttu-id="c7bc9-115">보강의 끝점을 "newKey" 키에 대 한 "endpoint1, endpoint2, endpoint3"로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bc9-115">Updates enrichment's endpoint to "endpoint1, endpoint2, endpoint3" for the key "newKey".</span></span>
<span data-ttu-id="c7bc9-116">Azure IoT Hub의 메시지 enrichments에 대 한 자세한 설명은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="c7bc9-116">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="c7bc9-117">변수</span><span class="sxs-lookup"><span data-stu-id="c7bc9-117">PARAMETERS</span></span>

### <span data-ttu-id="c7bc9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7bc9-118">-DefaultProfile</span></span>
<span data-ttu-id="c7bc9-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7bc9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7bc9-120">-끝점</span><span class="sxs-lookup"><span data-stu-id="c7bc9-120">-Endpoint</span></span>
<span data-ttu-id="c7bc9-121">Enrichments를 적용할 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="c7bc9-121">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="c7bc9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7bc9-122">-InputObject</span></span>
<span data-ttu-id="c7bc9-123">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="c7bc9-123">IotHub Object</span></span>

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

### <span data-ttu-id="c7bc9-124">-키</span><span class="sxs-lookup"><span data-stu-id="c7bc9-124">-Key</span></span>
<span data-ttu-id="c7bc9-125">보강의 키입니다.</span><span class="sxs-lookup"><span data-stu-id="c7bc9-125">The enrichment's key.</span></span>

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

### <span data-ttu-id="c7bc9-126">-이름</span><span class="sxs-lookup"><span data-stu-id="c7bc9-126">-Name</span></span>
<span data-ttu-id="c7bc9-127">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="c7bc9-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c7bc9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7bc9-128">-ResourceGroupName</span></span>
<span data-ttu-id="c7bc9-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7bc9-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c7bc9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7bc9-130">-ResourceId</span></span>
<span data-ttu-id="c7bc9-131">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="c7bc9-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c7bc9-132">-값</span><span class="sxs-lookup"><span data-stu-id="c7bc9-132">-Value</span></span>
<span data-ttu-id="c7bc9-133">보강의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c7bc9-133">The enrichment's value.</span></span>

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

### <span data-ttu-id="c7bc9-134">-확인</span><span class="sxs-lookup"><span data-stu-id="c7bc9-134">-Confirm</span></span>
<span data-ttu-id="c7bc9-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bc9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7bc9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7bc9-136">-WhatIf</span></span>
<span data-ttu-id="c7bc9-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c7bc9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7bc9-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7bc9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7bc9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7bc9-139">CommonParameters</span></span>
<span data-ttu-id="c7bc9-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bc9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7bc9-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7bc9-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7bc9-142">입력</span><span class="sxs-lookup"><span data-stu-id="c7bc9-142">INPUTS</span></span>

### <span data-ttu-id="c7bc9-143">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="c7bc9-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c7bc9-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c7bc9-144">System.String</span></span>

## <span data-ttu-id="c7bc9-145">출력</span><span class="sxs-lookup"><span data-stu-id="c7bc9-145">OUTPUTS</span></span>

### <span data-ttu-id="c7bc9-146">IotHub. PSEnrichmentMetadata/. \*</span><span class="sxs-lookup"><span data-stu-id="c7bc9-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="c7bc9-147">상속자</span><span class="sxs-lookup"><span data-stu-id="c7bc9-147">NOTES</span></span>

## <span data-ttu-id="c7bc9-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7bc9-148">RELATED LINKS</span></span>
