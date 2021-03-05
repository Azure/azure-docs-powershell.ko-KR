---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 9d24a8f3355c885a610cf371f4fadb716c6b159e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991293"
---
# <span data-ttu-id="7df47-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7df47-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="7df47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7df47-102">SYNOPSIS</span></span>
<span data-ttu-id="7df47-103">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="7df47-104">구문</span><span class="sxs-lookup"><span data-stu-id="7df47-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7df47-105">설명</span><span class="sxs-lookup"><span data-stu-id="7df47-105">DESCRIPTION</span></span>
<span data-ttu-id="7df47-106">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="7df47-107">도메인을 만든 후 애플리케이션은 토픽 엔드포인트에 이벤트를 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="7df47-108">예제</span><span class="sxs-lookup"><span data-stu-id="7df47-108">EXAMPLES</span></span>

### <span data-ttu-id="7df47-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="7df47-109">Example 1</span></span>

<span data-ttu-id="7df47-110">리소스 그룹 \` \` \` \` \` MyResourceGroupName 에서 지정된 지리적 위치 westus2에 Event Grid 도메인 도메인1을 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="7df47-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="7df47-111">Example 2</span></span>

<span data-ttu-id="7df47-112">지정된 지리적 위치 westus2에 Event Grid 도메인 \` 도메인1을 만듭니다. 리소스 그룹 \` \` \` \` MyResourceGroupName에서 \` 지정된 태그 "부서" 및 "환경"이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Department, Finance], [Environment, Test]}
```

## <span data-ttu-id="7df47-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7df47-113">PARAMETERS</span></span>

### <span data-ttu-id="7df47-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df47-114">-DefaultProfile</span></span>
<span data-ttu-id="7df47-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7df47-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="7df47-116">-InboundIpRule</span></span>
<span data-ttu-id="7df47-117">인바운드 IP 규칙 목록을 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="7df47-118">각 규칙은 CIDR 표기법(예: 10.0.0.0/8)의 IP 주소를 지정하고 IPMask의 일치 또는 일치 없음에 따라 수행할 해당 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="7df47-119">가능한 작업 값에는 허용만 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-119">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="7df47-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="7df47-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="7df47-121">공간 구분 키 = 값 형식의 기본값이 있는 입력 매핑 필드를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="7df47-122">허용되는 키 이름은 제목, eventtype 및 dataversion입니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="7df47-123">InputSchemaHelp가 customeventschema일 때만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="7df47-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="7df47-124">-InputMappingField</span></span>
<span data-ttu-id="7df47-125">공간 구분 키 = 값 형식의 입력 매핑 필드를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="7df47-126">허용되는 키 이름은 id, 토픽, eventtime, 제목, eventtype 및 dataversion입니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="7df47-127">InputSchemaHelp가 customeventschema일 때만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="7df47-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="7df47-128">-InputSchema</span></span>
<span data-ttu-id="7df47-129">토픽에 대한 입력 이벤트의척도입니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="7df47-130">허용되는 값은 eventgridschema, customeventschema 또는 cloudeventv01Schema입니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="7df47-131">기본값은 eventgridschema입니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-131">Default value is eventgridschema.</span></span> <span data-ttu-id="7df47-132">customeventschema를 지정한 경우 InputMappingField 또는/및 InputMappingDefaultValue 매개 변수도 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

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

### <span data-ttu-id="7df47-133">-Location</span><span class="sxs-lookup"><span data-stu-id="7df47-133">-Location</span></span>
<span data-ttu-id="7df47-134">도메인의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-134">The location of the domain.</span></span>

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

### <span data-ttu-id="7df47-135">-Name</span><span class="sxs-lookup"><span data-stu-id="7df47-135">-Name</span></span>
<span data-ttu-id="7df47-136">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-136">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7df47-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="7df47-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="7df47-138">공용 네트워크를 통해 트래픽을 허용하는지 여부를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="7df47-139">기본적으로 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-139">By default it is enabled.</span></span> <span data-ttu-id="7df47-140">InboundIpRule 매개 변수를 구성하여 특정 IP로 추가로 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="7df47-141">허용된 값은 사용되지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-141">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="7df47-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7df47-142">-ResourceGroupName</span></span>
<span data-ttu-id="7df47-143">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="7df47-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="7df47-144">-Tag</span></span>
<span data-ttu-id="7df47-145">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-145">Hashtable which represents resource Tags.</span></span>

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

### <span data-ttu-id="7df47-146">-확인</span><span class="sxs-lookup"><span data-stu-id="7df47-146">-Confirm</span></span>
<span data-ttu-id="7df47-147">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7df47-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7df47-148">-WhatIf</span></span>
<span data-ttu-id="7df47-149">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7df47-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7df47-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df47-151">CommonParameters</span></span>
<span data-ttu-id="7df47-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7df47-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df47-153">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7df47-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df47-154">입력</span><span class="sxs-lookup"><span data-stu-id="7df47-154">INPUTS</span></span>

### <span data-ttu-id="7df47-155">System.String</span><span class="sxs-lookup"><span data-stu-id="7df47-155">System.String</span></span>

### <span data-ttu-id="7df47-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7df47-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7df47-157">출력</span><span class="sxs-lookup"><span data-stu-id="7df47-157">OUTPUTS</span></span>

### <span data-ttu-id="7df47-158">Microsoft.Azure.Commands.EventGrid.Models.PSD오마인</span><span class="sxs-lookup"><span data-stu-id="7df47-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="7df47-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7df47-159">NOTES</span></span>

## <span data-ttu-id="7df47-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7df47-160">RELATED LINKS</span></span>
