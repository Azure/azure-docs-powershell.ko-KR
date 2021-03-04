---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 9fe0fad7ec353b3805bb941b62f6f6b6ee83e157
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986076"
---
# <span data-ttu-id="49946-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="49946-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="49946-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49946-102">SYNOPSIS</span></span>
<span data-ttu-id="49946-103">Event Grid 토픽의 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="49946-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="49946-104">구문</span><span class="sxs-lookup"><span data-stu-id="49946-104">SYNTAX</span></span>

### <span data-ttu-id="49946-105">TopicNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="49946-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49946-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="49946-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49946-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49946-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49946-108">설명</span><span class="sxs-lookup"><span data-stu-id="49946-108">DESCRIPTION</span></span>
<span data-ttu-id="49946-109">Event Grid 토픽의 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="49946-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="49946-110">이 항목은 Event Grid 항목의 태그를 바꾸는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49946-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="49946-111">예제</span><span class="sxs-lookup"><span data-stu-id="49946-111">EXAMPLES</span></span>

### <span data-ttu-id="49946-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="49946-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="49946-113">리소스 그룹 \` \` MyResourceGroupName에서 Event Grid 토픽 항목1의 속성을 설정하여 태그를 \` \` 지정된 태그 "부서" 및 "환경"으로 바 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="49946-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="49946-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="49946-114">PARAMETERS</span></span>

### <span data-ttu-id="49946-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49946-115">-DefaultProfile</span></span>
<span data-ttu-id="49946-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="49946-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49946-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="49946-117">-InboundIpRule</span></span>
<span data-ttu-id="49946-118">인바운드 IP 규칙 목록을 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="49946-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="49946-119">각 규칙은 CIDR 표기법(예: 10.0.0.0/8)의 IP 주소를 지정하고 IPMask의 일치 또는 일치 없음에 따라 수행할 해당 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="49946-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="49946-120">가능한 작업 값에는 허용만 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="49946-120">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49946-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49946-121">-InputObject</span></span>
<span data-ttu-id="49946-122">EventGrid 토픽 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="49946-122">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49946-123">-Name</span><span class="sxs-lookup"><span data-stu-id="49946-123">-Name</span></span>
<span data-ttu-id="49946-124">EventGrid 토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49946-124">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49946-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="49946-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="49946-126">공용 네트워크를 통해 트래픽을 허용하는지 여부를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="49946-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="49946-127">기본적으로 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="49946-127">By default it is enabled.</span></span> <span data-ttu-id="49946-128">InboundIpRule 매개 변수를 구성하여 특정 IP로 추가로 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49946-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="49946-129">허용된 값은 사용되지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49946-129">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:
Accepted values: enabled, disabled

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases:
Accepted values: enabled, disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49946-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49946-130">-ResourceGroupName</span></span>
<span data-ttu-id="49946-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49946-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49946-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49946-132">-ResourceId</span></span>
<span data-ttu-id="49946-133">EventGrid 토픽 ResourceID.</span><span class="sxs-lookup"><span data-stu-id="49946-133">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49946-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="49946-134">-Tag</span></span>
<span data-ttu-id="49946-135">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="49946-135">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49946-136">-확인</span><span class="sxs-lookup"><span data-stu-id="49946-136">-Confirm</span></span>
<span data-ttu-id="49946-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="49946-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49946-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49946-138">-WhatIf</span></span>
<span data-ttu-id="49946-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="49946-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49946-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49946-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49946-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49946-141">CommonParameters</span></span>
<span data-ttu-id="49946-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="49946-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49946-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49946-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49946-144">입력</span><span class="sxs-lookup"><span data-stu-id="49946-144">INPUTS</span></span>

### <span data-ttu-id="49946-145">System.String</span><span class="sxs-lookup"><span data-stu-id="49946-145">System.String</span></span>

### <span data-ttu-id="49946-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="49946-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="49946-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="49946-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="49946-148">출력</span><span class="sxs-lookup"><span data-stu-id="49946-148">OUTPUTS</span></span>

### <span data-ttu-id="49946-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="49946-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="49946-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="49946-150">NOTES</span></span>

## <span data-ttu-id="49946-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49946-151">RELATED LINKS</span></span>
