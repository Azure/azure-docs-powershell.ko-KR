---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 6a6b373fcbe38aac7e4e8d3972206955942eb18e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214976"
---
# <span data-ttu-id="a8059-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="a8059-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="a8059-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8059-102">SYNOPSIS</span></span>
<span data-ttu-id="a8059-103">이벤트 그리드 항목의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="a8059-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8059-104">SYNTAX</span></span>

### <span data-ttu-id="a8059-105">TopicNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a8059-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8059-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8059-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8059-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8059-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8059-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a8059-108">DESCRIPTION</span></span>
<span data-ttu-id="a8059-109">이벤트 그리드 항목의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="a8059-110">이를 사용 하 여 이벤트 그리드 항목의 태그를 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="a8059-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a8059-111">EXAMPLES</span></span>

### <span data-ttu-id="a8059-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a8059-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="a8059-113">\` \` \` \` 태그를 지정 된 태그 "부서" 및 "환경"으로 바꾸도록 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 항목 Topic1의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="a8059-114">변수</span><span class="sxs-lookup"><span data-stu-id="a8059-114">PARAMETERS</span></span>

### <span data-ttu-id="a8059-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8059-115">-DefaultProfile</span></span>
<span data-ttu-id="a8059-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a8059-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8059-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="a8059-117">-InboundIpRule</span></span>
<span data-ttu-id="a8059-118">인바운드 IP 규칙의 목록을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="a8059-119">각 규칙은 IP 주소를 CIDR 표기법으로 지정 합니다 (예: 10.0.0.0/8). 일치 여부를 기준으로 수행 되는 해당 작업과 함께 IpMask와 일치 하는 항목이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="a8059-120">사용할 수 있는 작업 값에 허용만 포함</span><span class="sxs-lookup"><span data-stu-id="a8059-120">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="a8059-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8059-121">-InputObject</span></span>
<span data-ttu-id="a8059-122">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="a8059-122">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="a8059-123">-이름</span><span class="sxs-lookup"><span data-stu-id="a8059-123">-Name</span></span>
<span data-ttu-id="a8059-124">EventGrid 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-124">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="a8059-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="a8059-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="a8059-126">공용 네트워크를 통해 트래픽이 허용 되는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="a8059-127">기본적으로 사용 하도록 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-127">By default it is enabled.</span></span> <span data-ttu-id="a8059-128">InboundIpRule 매개 변수를 구성 하 여 특정 Ip로 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="a8059-129">허용 되는 값은 비활성화 되 고 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-129">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="a8059-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8059-130">-ResourceGroupName</span></span>
<span data-ttu-id="a8059-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="a8059-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8059-132">-ResourceId</span></span>
<span data-ttu-id="a8059-133">EventGrid 항목 ResourceID.</span><span class="sxs-lookup"><span data-stu-id="a8059-133">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="a8059-134">태그</span><span class="sxs-lookup"><span data-stu-id="a8059-134">-Tag</span></span>
<span data-ttu-id="a8059-135">리소스 태그를 나타내는 Hashtables입니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-135">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="a8059-136">-확인</span><span class="sxs-lookup"><span data-stu-id="a8059-136">-Confirm</span></span>
<span data-ttu-id="a8059-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8059-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8059-138">-WhatIf</span></span>
<span data-ttu-id="a8059-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8059-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8059-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8059-141">CommonParameters</span></span>
<span data-ttu-id="a8059-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8059-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8059-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a8059-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8059-144">입력</span><span class="sxs-lookup"><span data-stu-id="a8059-144">INPUTS</span></span>

### <span data-ttu-id="a8059-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a8059-145">System.String</span></span>

### <span data-ttu-id="a8059-146">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="a8059-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="a8059-147">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="a8059-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a8059-148">출력</span><span class="sxs-lookup"><span data-stu-id="a8059-148">OUTPUTS</span></span>

### <span data-ttu-id="a8059-149">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="a8059-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="a8059-150">상속자</span><span class="sxs-lookup"><span data-stu-id="a8059-150">NOTES</span></span>

## <span data-ttu-id="a8059-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8059-151">RELATED LINKS</span></span>
