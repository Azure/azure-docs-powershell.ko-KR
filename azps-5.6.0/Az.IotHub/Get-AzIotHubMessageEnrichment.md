---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 18a6d5db9ecf7cf02604a883b49545650413ee28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987966"
---
# <span data-ttu-id="b8a89-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="b8a89-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="b8a89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8a89-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a89-103">IoT Hub에 대한 모든 메시지 보강 또는 특정 메시지 보강을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a89-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="b8a89-104">구문</span><span class="sxs-lookup"><span data-stu-id="b8a89-104">SYNTAX</span></span>

### <span data-ttu-id="b8a89-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b8a89-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8a89-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b8a89-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8a89-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b8a89-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8a89-108">설명</span><span class="sxs-lookup"><span data-stu-id="b8a89-108">DESCRIPTION</span></span>
<span data-ttu-id="b8a89-109">Azure IoT Hub의 메시지 보강에 대한 자세한 설명은 https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="b8a89-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="b8a89-110">예제</span><span class="sxs-lookup"><span data-stu-id="b8a89-110">EXAMPLES</span></span>

### <span data-ttu-id="b8a89-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8a89-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="b8a89-112">MyIotHub의 모든 메시지 보강 목록</span><span class="sxs-lookup"><span data-stu-id="b8a89-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="b8a89-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="b8a89-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="b8a89-114">"newKey" 메시지 보강에 대한 세부 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a89-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="b8a89-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b8a89-115">PARAMETERS</span></span>

### <span data-ttu-id="b8a89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a89-116">-DefaultProfile</span></span>
<span data-ttu-id="b8a89-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8a89-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8a89-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8a89-118">-InputObject</span></span>
<span data-ttu-id="b8a89-119">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="b8a89-119">IotHub object</span></span>

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

### <span data-ttu-id="b8a89-120">-Key</span><span class="sxs-lookup"><span data-stu-id="b8a89-120">-Key</span></span>
<span data-ttu-id="b8a89-121">보강의 키입니다.</span><span class="sxs-lookup"><span data-stu-id="b8a89-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="b8a89-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b8a89-122">-Name</span></span>
<span data-ttu-id="b8a89-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="b8a89-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b8a89-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8a89-124">-ResourceGroupName</span></span>
<span data-ttu-id="b8a89-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="b8a89-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b8a89-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8a89-126">-ResourceId</span></span>
<span data-ttu-id="b8a89-127">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b8a89-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b8a89-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a89-128">CommonParameters</span></span>
<span data-ttu-id="b8a89-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a89-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a89-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b8a89-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a89-131">입력</span><span class="sxs-lookup"><span data-stu-id="b8a89-131">INPUTS</span></span>

### <span data-ttu-id="b8a89-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b8a89-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b8a89-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b8a89-133">System.String</span></span>

## <span data-ttu-id="b8a89-134">출력</span><span class="sxs-lookup"><span data-stu-id="b8a89-134">OUTPUTS</span></span>

### <span data-ttu-id="b8a89-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="b8a89-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="b8a89-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span><span class="sxs-lookup"><span data-stu-id="b8a89-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="b8a89-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b8a89-137">NOTES</span></span>

## <span data-ttu-id="b8a89-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8a89-138">RELATED LINKS</span></span>
