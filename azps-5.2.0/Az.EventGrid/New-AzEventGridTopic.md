---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 402d781c32b98362d504dd5167024932d82e64fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363721"
---
# <span data-ttu-id="98660-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="98660-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="98660-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98660-102">SYNOPSIS</span></span>
<span data-ttu-id="98660-103">새 Azure Event Grid 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="98660-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="98660-104">구문</span><span class="sxs-lookup"><span data-stu-id="98660-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98660-105">설명</span><span class="sxs-lookup"><span data-stu-id="98660-105">DESCRIPTION</span></span>
<span data-ttu-id="98660-106">새 Azure Event Grid 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="98660-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="98660-107">토픽이 만들어지면 애플리케이션은 토픽 엔드포인트에 이벤트를 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98660-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="98660-108">예제</span><span class="sxs-lookup"><span data-stu-id="98660-108">EXAMPLES</span></span>

### <span data-ttu-id="98660-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="98660-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="98660-110">리소스 그룹 \` \` \` \` \` MyResourceGroupName에서 지정된 지리적 위치 westus2에 Event Grid 토픽 Topic1을 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="98660-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="98660-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="98660-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="98660-112">지정된 지리적 위치 westus2에 Event Grid 토픽 토픽1을 만듭니다. 리소스 그룹 \` \` \` \` \` MyResourceGroupName에 \` 지정된 태그 "Department" 및 "Environment"가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98660-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="98660-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98660-113">PARAMETERS</span></span>

### <span data-ttu-id="98660-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98660-114">-DefaultProfile</span></span>
<span data-ttu-id="98660-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="98660-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98660-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="98660-116">-InboundIpRule</span></span>
<span data-ttu-id="98660-117">인바운드 IP 규칙 목록을 나타내는 해시 가능한.</span><span class="sxs-lookup"><span data-stu-id="98660-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="98660-118">각 규칙은 CIDR 표기법의 IP 주소(예: 10.0.0.0/8)와 IpMask 일치 또는 일치 없음에 따라 수행할 해당 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98660-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="98660-119">가능한 작업 값에는 허용만 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="98660-119">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="98660-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="98660-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="98660-121">공백으로 구분된 키 = 값 형식의 기본값이 있는 입력 매핑 필드를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="98660-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="98660-122">허용되는 키 이름은 subject, eventtype 및 dataversion입니다.</span><span class="sxs-lookup"><span data-stu-id="98660-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="98660-123">InputSchemaHelp가 customeventschema일 때만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="98660-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="98660-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="98660-124">-InputMappingField</span></span>
<span data-ttu-id="98660-125">공백으로 구분된 키 = 값 형식의 입력 매핑 필드를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="98660-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="98660-126">허용되는 키 이름은 id, topic, eventtime, subject, eventtype 및 dataversion입니다.</span><span class="sxs-lookup"><span data-stu-id="98660-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="98660-127">InputSchemaHelp가 customeventschema일 때만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="98660-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="98660-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="98660-128">-InputSchema</span></span>
<span data-ttu-id="98660-129">토픽에 대한 입력 이벤트의 schema입니다.</span><span class="sxs-lookup"><span data-stu-id="98660-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="98660-130">허용되는 값은 eventgridschema, customeventschema 또는 cloudeventv01Schema입니다.</span><span class="sxs-lookup"><span data-stu-id="98660-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="98660-131">기본값은 eventgridschema입니다.</span><span class="sxs-lookup"><span data-stu-id="98660-131">Default value is eventgridschema.</span></span> <span data-ttu-id="98660-132">customeventschema를 지정한 경우 InputMappingField 또는/및 InputMappingDefaultValue 매개 변수도 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="98660-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

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

### <span data-ttu-id="98660-133">-Location</span><span class="sxs-lookup"><span data-stu-id="98660-133">-Location</span></span>
<span data-ttu-id="98660-134">토픽의 위치</span><span class="sxs-lookup"><span data-stu-id="98660-134">The location of the topic</span></span>

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

### <span data-ttu-id="98660-135">-Name</span><span class="sxs-lookup"><span data-stu-id="98660-135">-Name</span></span>
<span data-ttu-id="98660-136">항목의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98660-136">The name of the topic.</span></span>

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

### <span data-ttu-id="98660-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="98660-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="98660-138">공용 네트워크를 통해 트래픽이 허용되는지 여부를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="98660-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="98660-139">기본적으로 사용하도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="98660-139">By default it is enabled.</span></span> <span data-ttu-id="98660-140">InboundIpRule 매개 변수를 구성하여 특정 IP로 추가로 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98660-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="98660-141">허용되는 값은 사용되지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98660-141">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="98660-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98660-142">-ResourceGroupName</span></span>
<span data-ttu-id="98660-143">토픽을 만들어야 하는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="98660-143">The resource group in which the topic should be created.</span></span>

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

### <span data-ttu-id="98660-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="98660-144">-Tag</span></span>
<span data-ttu-id="98660-145">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="98660-145">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="98660-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98660-146">-Confirm</span></span>
<span data-ttu-id="98660-147">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="98660-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98660-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98660-148">-WhatIf</span></span>
<span data-ttu-id="98660-149">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="98660-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98660-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98660-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98660-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98660-151">CommonParameters</span></span>
<span data-ttu-id="98660-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="98660-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98660-153">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="98660-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98660-154">입력</span><span class="sxs-lookup"><span data-stu-id="98660-154">INPUTS</span></span>

### <span data-ttu-id="98660-155">System.String</span><span class="sxs-lookup"><span data-stu-id="98660-155">System.String</span></span>

### <span data-ttu-id="98660-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="98660-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="98660-157">출력</span><span class="sxs-lookup"><span data-stu-id="98660-157">OUTPUTS</span></span>

### <span data-ttu-id="98660-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="98660-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="98660-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="98660-159">NOTES</span></span>

## <span data-ttu-id="98660-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98660-160">RELATED LINKS</span></span>