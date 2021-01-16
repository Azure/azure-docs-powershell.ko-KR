---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 91694efaeaf1a24018269706f3ee388feb7218ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358576"
---
# <span data-ttu-id="9bb5d-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="9bb5d-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="9bb5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bb5d-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb5d-103">IoT Hub에 대한 모든 메시지 보강 또는 특정 메시지 보강을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="9bb5d-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="9bb5d-104">구문</span><span class="sxs-lookup"><span data-stu-id="9bb5d-104">SYNTAX</span></span>

### <span data-ttu-id="9bb5d-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9bb5d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bb5d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9bb5d-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bb5d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9bb5d-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9bb5d-108">설명</span><span class="sxs-lookup"><span data-stu-id="9bb5d-108">DESCRIPTION</span></span>
<span data-ttu-id="9bb5d-109">Azure IoT Hub의 메시지 보강에 대한 자세한 설명은 다음을 참조하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="9bb5d-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="9bb5d-110">예제</span><span class="sxs-lookup"><span data-stu-id="9bb5d-110">EXAMPLES</span></span>

### <span data-ttu-id="9bb5d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9bb5d-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="9bb5d-112">MyIotHub의 모든 메시지 보강 나열</span><span class="sxs-lookup"><span data-stu-id="9bb5d-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="9bb5d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="9bb5d-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="9bb5d-114">"newKey" 메시지 보강에 대한 세부 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="9bb5d-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="9bb5d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bb5d-115">PARAMETERS</span></span>

### <span data-ttu-id="9bb5d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb5d-116">-DefaultProfile</span></span>
<span data-ttu-id="9bb5d-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9bb5d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bb5d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bb5d-118">-InputObject</span></span>
<span data-ttu-id="9bb5d-119">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="9bb5d-119">IotHub object</span></span>

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

### <span data-ttu-id="9bb5d-120">-Key</span><span class="sxs-lookup"><span data-stu-id="9bb5d-120">-Key</span></span>
<span data-ttu-id="9bb5d-121">보강의 키입니다.</span><span class="sxs-lookup"><span data-stu-id="9bb5d-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="9bb5d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9bb5d-122">-Name</span></span>
<span data-ttu-id="9bb5d-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="9bb5d-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9bb5d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bb5d-124">-ResourceGroupName</span></span>
<span data-ttu-id="9bb5d-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="9bb5d-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9bb5d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bb5d-126">-ResourceId</span></span>
<span data-ttu-id="9bb5d-127">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9bb5d-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9bb5d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb5d-128">CommonParameters</span></span>
<span data-ttu-id="9bb5d-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9bb5d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb5d-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9bb5d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb5d-131">입력</span><span class="sxs-lookup"><span data-stu-id="9bb5d-131">INPUTS</span></span>

### <span data-ttu-id="9bb5d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9bb5d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9bb5d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9bb5d-133">System.String</span></span>

## <span data-ttu-id="9bb5d-134">출력</span><span class="sxs-lookup"><span data-stu-id="9bb5d-134">OUTPUTS</span></span>

### <span data-ttu-id="9bb5d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="9bb5d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="9bb5d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span><span class="sxs-lookup"><span data-stu-id="9bb5d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="9bb5d-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9bb5d-137">NOTES</span></span>

## <span data-ttu-id="9bb5d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9bb5d-138">RELATED LINKS</span></span>
