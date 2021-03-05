---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: df81f976f571a59f68d51ef734f1bc3ea5536015
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991251"
---
# <span data-ttu-id="e9a22-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="e9a22-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="e9a22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9a22-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a22-103">새 Azure Event Grid 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="e9a22-104">구문</span><span class="sxs-lookup"><span data-stu-id="e9a22-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9a22-105">설명</span><span class="sxs-lookup"><span data-stu-id="e9a22-105">DESCRIPTION</span></span>
<span data-ttu-id="e9a22-106">새 Azure Event Grid 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="e9a22-107">토픽을 만든 후 애플리케이션은 토픽 엔드포인트에 이벤트를 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="e9a22-108">예제</span><span class="sxs-lookup"><span data-stu-id="e9a22-108">EXAMPLES</span></span>

### <span data-ttu-id="e9a22-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9a22-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="e9a22-110">리소스 그룹 \` \` \` \` \` MyResourceGroupName 에서 지정된 지리적 위치 westus2에서 Event Grid 토픽1을 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e9a22-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="e9a22-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="e9a22-112">지정된 지리적 위치 westus2에서 Event Grid 토픽1을 리소스 그룹 \` \` \` \` \` MyResourceGroupName에 \` 지정된 태그 "부서" 및 "환경"으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="e9a22-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e9a22-113">PARAMETERS</span></span>

### <span data-ttu-id="e9a22-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9a22-114">-DefaultProfile</span></span>
<span data-ttu-id="e9a22-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e9a22-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9a22-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="e9a22-116">-InboundIpRule</span></span>
<span data-ttu-id="e9a22-117">인바운드 IP 규칙 목록을 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="e9a22-118">각 규칙은 CIDR 표기법(예: 10.0.0.0/8)의 IP 주소를 지정하고 IPMask의 일치 또는 일치 없음에 따라 수행할 해당 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="e9a22-119">가능한 작업 값에는 허용만 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-119">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a22-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="e9a22-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="e9a22-121">공간 구분 키 = 값 형식의 기본값이 있는 입력 매핑 필드를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="e9a22-122">허용되는 키 이름은 제목, eventtype 및 dataversion입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="e9a22-123">InputSchemaHelp가 customeventschema일 때만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a22-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="e9a22-124">-InputMappingField</span></span>
<span data-ttu-id="e9a22-125">공간 구분 키 = 값 형식의 입력 매핑 필드를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="e9a22-126">허용되는 키 이름은 id, 토픽, eventtime, 제목, eventtype 및 dataversion입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="e9a22-127">InputSchemaHelp가 customeventschema일 때만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a22-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="e9a22-128">-InputSchema</span></span>
<span data-ttu-id="e9a22-129">토픽에 대한 입력 이벤트의척도입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="e9a22-130">허용되는 값은 eventgridschema, customeventschema 또는 cloudeventv01Schema입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="e9a22-131">기본값은 eventgridschema입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-131">Default value is eventgridschema.</span></span> <span data-ttu-id="e9a22-132">customeventschema를 지정한 경우 InputMappingField 또는/및 InputMappingDefaultValue 매개 변수도 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EventGridSchema, CustomEventSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a22-133">-Location</span><span class="sxs-lookup"><span data-stu-id="e9a22-133">-Location</span></span>
<span data-ttu-id="e9a22-134">토픽의 위치</span><span class="sxs-lookup"><span data-stu-id="e9a22-134">The location of the topic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a22-135">-Name</span><span class="sxs-lookup"><span data-stu-id="e9a22-135">-Name</span></span>
<span data-ttu-id="e9a22-136">토픽의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-136">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a22-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="e9a22-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="e9a22-138">공용 네트워크를 통해 트래픽을 허용하는지 여부를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="e9a22-139">기본적으로 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-139">By default it is enabled.</span></span> <span data-ttu-id="e9a22-140">InboundIpRule 매개 변수를 구성하여 특정 IP로 추가로 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="e9a22-141">허용된 값은 사용되지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-141">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a22-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9a22-142">-ResourceGroupName</span></span>
<span data-ttu-id="e9a22-143">토픽을 만들어야 하는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-143">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a22-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="e9a22-144">-Tag</span></span>
<span data-ttu-id="e9a22-145">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-145">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9a22-146">-확인</span><span class="sxs-lookup"><span data-stu-id="e9a22-146">-Confirm</span></span>
<span data-ttu-id="e9a22-147">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9a22-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9a22-148">-WhatIf</span></span>
<span data-ttu-id="e9a22-149">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9a22-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9a22-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9a22-151">CommonParameters</span></span>
<span data-ttu-id="e9a22-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a22-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a22-153">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9a22-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a22-154">입력</span><span class="sxs-lookup"><span data-stu-id="e9a22-154">INPUTS</span></span>

### <span data-ttu-id="e9a22-155">System.String</span><span class="sxs-lookup"><span data-stu-id="e9a22-155">System.String</span></span>

### <span data-ttu-id="e9a22-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e9a22-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e9a22-157">출력</span><span class="sxs-lookup"><span data-stu-id="e9a22-157">OUTPUTS</span></span>

### <span data-ttu-id="e9a22-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="e9a22-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="e9a22-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e9a22-159">NOTES</span></span>

## <span data-ttu-id="e9a22-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9a22-160">RELATED LINKS</span></span>
