---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 91694efaeaf1a24018269706f3ee388feb7218ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034287"
---
# <span data-ttu-id="5c747-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5c747-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="5c747-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c747-102">SYNOPSIS</span></span>
<span data-ttu-id="5c747-103">IoT Hub의 모든 메시지 enrichments 또는 특정 메시지 보강를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c747-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="5c747-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5c747-104">SYNTAX</span></span>

### <span data-ttu-id="5c747-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5c747-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c747-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5c747-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c747-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5c747-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c747-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5c747-108">DESCRIPTION</span></span>
<span data-ttu-id="5c747-109">Azure IoT Hub의 메시지 enrichments에 대 한 자세한 설명은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="5c747-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="5c747-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5c747-110">EXAMPLES</span></span>

### <span data-ttu-id="5c747-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5c747-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="5c747-112">MyIotHub의 모든 메시지 enrichments를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c747-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="5c747-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="5c747-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="5c747-114">"NewKey" 메시지 보강에 대 한 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c747-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="5c747-115">변수</span><span class="sxs-lookup"><span data-stu-id="5c747-115">PARAMETERS</span></span>

### <span data-ttu-id="5c747-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c747-116">-DefaultProfile</span></span>
<span data-ttu-id="5c747-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c747-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c747-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c747-118">-InputObject</span></span>
<span data-ttu-id="5c747-119">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="5c747-119">IotHub object</span></span>

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

### <span data-ttu-id="5c747-120">-키</span><span class="sxs-lookup"><span data-stu-id="5c747-120">-Key</span></span>
<span data-ttu-id="5c747-121">보강의 키입니다.</span><span class="sxs-lookup"><span data-stu-id="5c747-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="5c747-122">-이름</span><span class="sxs-lookup"><span data-stu-id="5c747-122">-Name</span></span>
<span data-ttu-id="5c747-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="5c747-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5c747-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c747-124">-ResourceGroupName</span></span>
<span data-ttu-id="5c747-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c747-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5c747-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c747-126">-ResourceId</span></span>
<span data-ttu-id="5c747-127">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="5c747-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5c747-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c747-128">CommonParameters</span></span>
<span data-ttu-id="5c747-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c747-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c747-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c747-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c747-131">입력</span><span class="sxs-lookup"><span data-stu-id="5c747-131">INPUTS</span></span>

### <span data-ttu-id="5c747-132">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="5c747-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5c747-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5c747-133">System.String</span></span>

## <span data-ttu-id="5c747-134">출력</span><span class="sxs-lookup"><span data-stu-id="5c747-134">OUTPUTS</span></span>

### <span data-ttu-id="5c747-135">IotHub. PSEnrichmentMetadata/. \*</span><span class="sxs-lookup"><span data-stu-id="5c747-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="5c747-136">IotHub를 PSEnrichmentProperties []으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c747-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="5c747-137">상속자</span><span class="sxs-lookup"><span data-stu-id="5c747-137">NOTES</span></span>

## <span data-ttu-id="5c747-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c747-138">RELATED LINKS</span></span>
