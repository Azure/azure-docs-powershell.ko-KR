---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubMessageEnrichment.md
ms.openlocfilehash: caae747f7accd76db1424d14274416f0de97122d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876749"
---
# <span data-ttu-id="4fd8f-101">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4fd8f-101">Add-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="4fd8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fd8f-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd8f-103">IoT Hub에서 선택한 끝점에 대 한 메시지 보강를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-103">Creates a message enrichment for chosen endpoints in your IoT Hub.</span></span>

## <span data-ttu-id="4fd8f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4fd8f-104">SYNTAX</span></span>

### <span data-ttu-id="4fd8f-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4fd8f-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key] <String> -Value <String>
 -Endpoint <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fd8f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4fd8f-106">InputObjectSet</span></span>
```
Add-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fd8f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4fd8f-107">ResourceIdSet</span></span>
```
Add-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key] <String> -Value <String> -Endpoint <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fd8f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4fd8f-108">DESCRIPTION</span></span>
<span data-ttu-id="4fd8f-109">IoT Hub 당 최대 10 개의 메시지 enrichments를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-109">Add up to 10 message enrichments per IoT Hub.</span></span> <span data-ttu-id="4fd8f-110">이는 선택한 끝점으로 전송 된 메시지에 응용 프로그램 속성으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-110">These are added as application properties to messages sent to chosen endpoint(s).</span></span>
<span data-ttu-id="4fd8f-111">자세히 알아보려면 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="4fd8f-111">To know more, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="4fd8f-112">예제의</span><span class="sxs-lookup"><span data-stu-id="4fd8f-112">EXAMPLES</span></span>

### <span data-ttu-id="4fd8f-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="4fd8f-113">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Value "newValue" -Endpoint endpoint1,endpoint2

Key          : newKey
Value        : newValue
Endpoint(s)  : { endpoint1, endpoint2 }
```

<span data-ttu-id="4fd8f-114">키 "newKey" 및 value "newValue" 인 새 보강를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-114">Add a new enrichment with key "newKey" and value "newValue".</span></span> <span data-ttu-id="4fd8f-115">이 새 보강 "endpoint1" 및 "endpoint2" 끝점에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-115">This new enrichment is applied to "endpoint1" and "endpoint2" endpoints.</span></span>

## <span data-ttu-id="4fd8f-116">변수</span><span class="sxs-lookup"><span data-stu-id="4fd8f-116">PARAMETERS</span></span>

### <span data-ttu-id="4fd8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd8f-117">-DefaultProfile</span></span>
<span data-ttu-id="4fd8f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fd8f-119">-끝점</span><span class="sxs-lookup"><span data-stu-id="4fd8f-119">-Endpoint</span></span>
<span data-ttu-id="4fd8f-120">Enrichments를 적용할 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-120">Endpoint(s) to apply enrichments to.</span></span>

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

### <span data-ttu-id="4fd8f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fd8f-121">-InputObject</span></span>
<span data-ttu-id="4fd8f-122">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="4fd8f-122">IotHub object</span></span>

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

### <span data-ttu-id="4fd8f-123">-키</span><span class="sxs-lookup"><span data-stu-id="4fd8f-123">-Key</span></span>
<span data-ttu-id="4fd8f-124">보강의 키입니다.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-124">The enrichment's key.</span></span>

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

### <span data-ttu-id="4fd8f-125">-이름</span><span class="sxs-lookup"><span data-stu-id="4fd8f-125">-Name</span></span>
<span data-ttu-id="4fd8f-126">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="4fd8f-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4fd8f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fd8f-127">-ResourceGroupName</span></span>
<span data-ttu-id="4fd8f-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4fd8f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fd8f-129">-ResourceId</span></span>
<span data-ttu-id="4fd8f-130">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="4fd8f-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4fd8f-131">-값</span><span class="sxs-lookup"><span data-stu-id="4fd8f-131">-Value</span></span>
<span data-ttu-id="4fd8f-132">보강의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-132">The enrichment's value.</span></span>

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

### <span data-ttu-id="4fd8f-133">-확인</span><span class="sxs-lookup"><span data-stu-id="4fd8f-133">-Confirm</span></span>
<span data-ttu-id="4fd8f-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fd8f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fd8f-135">-WhatIf</span></span>
<span data-ttu-id="4fd8f-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fd8f-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fd8f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd8f-138">CommonParameters</span></span>
<span data-ttu-id="4fd8f-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fd8f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd8f-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fd8f-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd8f-141">입력</span><span class="sxs-lookup"><span data-stu-id="4fd8f-141">INPUTS</span></span>

### <span data-ttu-id="4fd8f-142">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="4fd8f-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4fd8f-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4fd8f-143">System.String</span></span>

## <span data-ttu-id="4fd8f-144">출력</span><span class="sxs-lookup"><span data-stu-id="4fd8f-144">OUTPUTS</span></span>

### <span data-ttu-id="4fd8f-145">IotHub. PSEnrichmentMetadata/. \*</span><span class="sxs-lookup"><span data-stu-id="4fd8f-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

## <span data-ttu-id="4fd8f-146">상속자</span><span class="sxs-lookup"><span data-stu-id="4fd8f-146">NOTES</span></span>

## <span data-ttu-id="4fd8f-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fd8f-147">RELATED LINKS</span></span>
