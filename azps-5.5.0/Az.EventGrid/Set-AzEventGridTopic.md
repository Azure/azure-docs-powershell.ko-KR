---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 6a6b373fcbe38aac7e4e8d3972206955942eb18e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204144"
---
# <span data-ttu-id="0db0e-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="0db0e-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="0db0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0db0e-102">SYNOPSIS</span></span>
<span data-ttu-id="0db0e-103">Event Grid 토픽의 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="0db0e-104">구문</span><span class="sxs-lookup"><span data-stu-id="0db0e-104">SYNTAX</span></span>

### <span data-ttu-id="0db0e-105">TopicNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0db0e-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0db0e-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0db0e-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0db0e-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0db0e-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0db0e-108">설명</span><span class="sxs-lookup"><span data-stu-id="0db0e-108">DESCRIPTION</span></span>
<span data-ttu-id="0db0e-109">Event Grid 토픽의 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="0db0e-110">Event Grid 토픽의 태그를 바꾸는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="0db0e-111">예제</span><span class="sxs-lookup"><span data-stu-id="0db0e-111">EXAMPLES</span></span>

### <span data-ttu-id="0db0e-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="0db0e-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="0db0e-113">태그를 지정된 태그 "Department" 및 "Environment"로 바꾸기 위해 리소스 그룹 \` \` \` MyResourceGroupName에서 Event Grid 항목 Topic1의 \` 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="0db0e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0db0e-114">PARAMETERS</span></span>

### <span data-ttu-id="0db0e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db0e-115">-DefaultProfile</span></span>
<span data-ttu-id="0db0e-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0db0e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0db0e-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="0db0e-117">-InboundIpRule</span></span>
<span data-ttu-id="0db0e-118">인바운드 IP 규칙 목록을 나타내는 해시 가능한.</span><span class="sxs-lookup"><span data-stu-id="0db0e-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="0db0e-119">각 규칙은 CIDR 표기법의 IP 주소(예: 10.0.0.0/8)와 IpMask 일치 또는 일치 없음에 따라 수행할 해당 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="0db0e-120">가능한 작업 값에는 허용만 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-120">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="0db0e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0db0e-121">-InputObject</span></span>
<span data-ttu-id="0db0e-122">EventGrid 토픽 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-122">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="0db0e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0db0e-123">-Name</span></span>
<span data-ttu-id="0db0e-124">EventGrid 토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-124">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="0db0e-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0db0e-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="0db0e-126">공용 네트워크를 통해 트래픽이 허용되는지 여부를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="0db0e-127">기본적으로 사용하도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-127">By default it is enabled.</span></span> <span data-ttu-id="0db0e-128">InboundIpRule 매개 변수를 구성하여 특정 IP로 추가로 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="0db0e-129">허용되는 값은 사용되지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-129">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="0db0e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db0e-130">-ResourceGroupName</span></span>
<span data-ttu-id="0db0e-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="0db0e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0db0e-132">-ResourceId</span></span>
<span data-ttu-id="0db0e-133">EventGrid 토픽 ResourceID.</span><span class="sxs-lookup"><span data-stu-id="0db0e-133">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="0db0e-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="0db0e-134">-Tag</span></span>
<span data-ttu-id="0db0e-135">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-135">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="0db0e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0db0e-136">-Confirm</span></span>
<span data-ttu-id="0db0e-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0db0e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0db0e-138">-WhatIf</span></span>
<span data-ttu-id="0db0e-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0db0e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0db0e-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0db0e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db0e-141">CommonParameters</span></span>
<span data-ttu-id="0db0e-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0db0e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db0e-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0db0e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db0e-144">입력</span><span class="sxs-lookup"><span data-stu-id="0db0e-144">INPUTS</span></span>

### <span data-ttu-id="0db0e-145">System.String</span><span class="sxs-lookup"><span data-stu-id="0db0e-145">System.String</span></span>

### <span data-ttu-id="0db0e-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="0db0e-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="0db0e-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0db0e-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0db0e-148">출력</span><span class="sxs-lookup"><span data-stu-id="0db0e-148">OUTPUTS</span></span>

### <span data-ttu-id="0db0e-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="0db0e-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="0db0e-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0db0e-150">NOTES</span></span>

## <span data-ttu-id="0db0e-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0db0e-151">RELATED LINKS</span></span>
