---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 6340db7446671660df08449529b6678cf79a2af9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218713"
---
# <span data-ttu-id="d8ae0-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d8ae0-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="d8ae0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8ae0-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ae0-103">새 Azure 이벤트 그리드 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="d8ae0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8ae0-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8ae0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d8ae0-105">DESCRIPTION</span></span>
<span data-ttu-id="d8ae0-106">새 Azure 이벤트 그리드 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="d8ae0-107">도메인을 만든 후에는 응용 프로그램에서 항목 끝점에 이벤트를 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="d8ae0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d8ae0-108">EXAMPLES</span></span>

### <span data-ttu-id="d8ae0-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="d8ae0-109">Example 1</span></span>

<span data-ttu-id="d8ae0-110">\` \` \` \` 리소스 그룹 MyResourceGroupName에서 지정 된 지리적 위치 westus2에 이벤트 \` 그리드 도메인 Domain1을 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="d8ae0-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

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

### <span data-ttu-id="d8ae0-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="d8ae0-111">Example 2</span></span>

<span data-ttu-id="d8ae0-112">지정 된 \` \` \` \` \` \` 태그 "부서" 및 "환경"이 있는 리소스 그룹 MyResourceGroupName에서 지정 된 지리적 위치 westus2에 이벤트 그리드 도메인 Domain1을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

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

## <span data-ttu-id="d8ae0-113">변수</span><span class="sxs-lookup"><span data-stu-id="d8ae0-113">PARAMETERS</span></span>

### <span data-ttu-id="d8ae0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ae0-114">-DefaultProfile</span></span>
<span data-ttu-id="d8ae0-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8ae0-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="d8ae0-116">-InboundIpRule</span></span>
<span data-ttu-id="d8ae0-117">인바운드 IP 규칙의 목록을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="d8ae0-118">각 규칙은 IP 주소를 CIDR 표기법으로 지정 합니다 (예: 10.0.0.0/8). 일치 여부를 기준으로 수행 되는 해당 작업과 함께 IpMask와 일치 하는 항목이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="d8ae0-119">사용할 수 있는 작업 값에 허용만 포함</span><span class="sxs-lookup"><span data-stu-id="d8ae0-119">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="d8ae0-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="d8ae0-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="d8ae0-121">공백으로 구분 된 key = value 형식의 값으로 입력 매핑 필드를 나타내는 Hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="d8ae0-122">허용 되는 키 이름은 subject, eventtype 및 dataversion입니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="d8ae0-123">InputSchemaHelp만 customeventschema 경우 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="d8ae0-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="d8ae0-124">-InputMappingField</span></span>
<span data-ttu-id="d8ae0-125">공백으로 구분 된 key = value 형식의 입력 매핑 필드를 나타내는 Hashtable</span><span class="sxs-lookup"><span data-stu-id="d8ae0-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="d8ae0-126">허용 되는 키 이름은 id, topic, eventtime, subject, eventtype, dataversion입니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="d8ae0-127">InputSchemaHelp만 customeventschema 경우 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="d8ae0-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="d8ae0-128">-InputSchema</span></span>
<span data-ttu-id="d8ae0-129">항목에 대 한 입력 이벤트의 스키마입니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="d8ae0-130">허용 되는 값은 eventgridschema, customeventschema 또는 cloudeventv01Schema입니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="d8ae0-131">기본값은 eventgridschema입니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-131">Default value is eventgridschema.</span></span> <span data-ttu-id="d8ae0-132">Customeventschema가 지정 된 경우 InputMappingField 또는/및 InputMappingDefaultValue 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

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

### <span data-ttu-id="d8ae0-133">-위치</span><span class="sxs-lookup"><span data-stu-id="d8ae0-133">-Location</span></span>
<span data-ttu-id="d8ae0-134">도메인의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-134">The location of the domain.</span></span>

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

### <span data-ttu-id="d8ae0-135">-이름</span><span class="sxs-lookup"><span data-stu-id="d8ae0-135">-Name</span></span>
<span data-ttu-id="d8ae0-136">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-136">EventGrid domain name.</span></span>

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

### <span data-ttu-id="d8ae0-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="d8ae0-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="d8ae0-138">공용 네트워크를 통해 트래픽이 허용 되는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="d8ae0-139">기본적으로 사용 하도록 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-139">By default it is enabled.</span></span> <span data-ttu-id="d8ae0-140">InboundIpRule 매개 변수를 구성 하 여 특정 Ip로 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="d8ae0-141">허용 되는 값은 비활성화 되 고 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-141">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="d8ae0-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8ae0-142">-ResourceGroupName</span></span>
<span data-ttu-id="d8ae0-143">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="d8ae0-144">태그</span><span class="sxs-lookup"><span data-stu-id="d8ae0-144">-Tag</span></span>
<span data-ttu-id="d8ae0-145">리소스 태그를 나타내는 Hashtable</span><span class="sxs-lookup"><span data-stu-id="d8ae0-145">Hashtable which represents resource Tags.</span></span>

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

### <span data-ttu-id="d8ae0-146">-확인</span><span class="sxs-lookup"><span data-stu-id="d8ae0-146">-Confirm</span></span>
<span data-ttu-id="d8ae0-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8ae0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8ae0-148">-WhatIf</span></span>
<span data-ttu-id="d8ae0-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8ae0-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8ae0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ae0-151">CommonParameters</span></span>
<span data-ttu-id="d8ae0-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ae0-153">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d8ae0-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ae0-154">입력</span><span class="sxs-lookup"><span data-stu-id="d8ae0-154">INPUTS</span></span>

### <span data-ttu-id="d8ae0-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d8ae0-155">System.String</span></span>

### <span data-ttu-id="d8ae0-156">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="d8ae0-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d8ae0-157">출력</span><span class="sxs-lookup"><span data-stu-id="d8ae0-157">OUTPUTS</span></span>

### <span data-ttu-id="d8ae0-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="d8ae0-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="d8ae0-159">상속자</span><span class="sxs-lookup"><span data-stu-id="d8ae0-159">NOTES</span></span>

## <span data-ttu-id="d8ae0-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8ae0-160">RELATED LINKS</span></span>
