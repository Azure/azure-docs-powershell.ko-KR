---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 445108b2413673e2ce48dcbfac9f3fa0cdb45982
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993351"
---
# <span data-ttu-id="ca71c-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="ca71c-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="ca71c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca71c-102">SYNOPSIS</span></span>
<span data-ttu-id="ca71c-103">지정된 Service Bus 네임스페이스에서 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ca71c-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ca71c-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca71c-104">SYNTAX</span></span>

### <span data-ttu-id="ca71c-105">TopicPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ca71c-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca71c-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ca71c-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca71c-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ca71c-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca71c-108">설명</span><span class="sxs-lookup"><span data-stu-id="ca71c-108">DESCRIPTION</span></span>
<span data-ttu-id="ca71c-109">**Remove-AzServiceBusTopic** cmdlet은 지정된 Service Bus 네임스페이스에서 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ca71c-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ca71c-110">예제</span><span class="sxs-lookup"><span data-stu-id="ca71c-110">EXAMPLES</span></span>

### <span data-ttu-id="ca71c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ca71c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="ca71c-112">네임스페이스에서 `SB-Topic_exampl1` 토픽을 `SB-Example1` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ca71c-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="ca71c-113">예제 2: InputObject - 변수 사용:</span><span class="sxs-lookup"><span data-stu-id="ca71c-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="ca71c-114">예제 3: InputObject - 배관 사용:</span><span class="sxs-lookup"><span data-stu-id="ca71c-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="ca71c-115">예제 4: 변수를 사용하는 ResourceId:</span><span class="sxs-lookup"><span data-stu-id="ca71c-115">Example 4: ResourceId Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="ca71c-116">예제 5: 문자열 값을 사용하는 ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca71c-116">Example 5: ResourceId Using String value</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="ca71c-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ca71c-117">PARAMETERS</span></span>

### <span data-ttu-id="ca71c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca71c-118">-AsJob</span></span>
<span data-ttu-id="ca71c-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ca71c-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca71c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca71c-120">-DefaultProfile</span></span>
<span data-ttu-id="ca71c-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca71c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca71c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca71c-122">-InputObject</span></span>
<span data-ttu-id="ca71c-123">Service Bus 토픽 개체</span><span class="sxs-lookup"><span data-stu-id="ca71c-123">Service Bus Topic Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: TopicInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca71c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ca71c-124">-Name</span></span>
<span data-ttu-id="ca71c-125">토픽 이름</span><span class="sxs-lookup"><span data-stu-id="ca71c-125">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca71c-126">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="ca71c-126">-Namespace</span></span>
<span data-ttu-id="ca71c-127">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="ca71c-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca71c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca71c-128">-PassThru</span></span>
<span data-ttu-id="ca71c-129">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca71c-129">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca71c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca71c-130">-ResourceGroupName</span></span>
<span data-ttu-id="ca71c-131">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="ca71c-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca71c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca71c-132">-ResourceId</span></span>
<span data-ttu-id="ca71c-133">Service Bus 토픽 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ca71c-133">Service Bus Topic Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: TopicResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca71c-134">-확인</span><span class="sxs-lookup"><span data-stu-id="ca71c-134">-Confirm</span></span>
<span data-ttu-id="ca71c-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca71c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca71c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca71c-136">-WhatIf</span></span>
<span data-ttu-id="ca71c-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ca71c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca71c-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca71c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca71c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca71c-139">CommonParameters</span></span>
<span data-ttu-id="ca71c-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca71c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca71c-141">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ca71c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca71c-142">입력</span><span class="sxs-lookup"><span data-stu-id="ca71c-142">INPUTS</span></span>

### <span data-ttu-id="ca71c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="ca71c-143">System.String</span></span>

### <span data-ttu-id="ca71c-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="ca71c-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="ca71c-145">출력</span><span class="sxs-lookup"><span data-stu-id="ca71c-145">OUTPUTS</span></span>

### <span data-ttu-id="ca71c-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ca71c-146">System.Boolean</span></span>

## <span data-ttu-id="ca71c-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca71c-147">NOTES</span></span>

## <span data-ttu-id="ca71c-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca71c-148">RELATED LINKS</span></span>
