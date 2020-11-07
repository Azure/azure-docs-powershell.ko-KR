---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 27d35f0c5b0e947624827d01d1182a09912cb9fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699155"
---
# <span data-ttu-id="e7b86-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="e7b86-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="e7b86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7b86-102">SYNOPSIS</span></span>
<span data-ttu-id="e7b86-103">지정 된 Service Bus 네임 스페이스에서 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b86-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e7b86-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7b86-104">SYNTAX</span></span>

### <span data-ttu-id="e7b86-105">TopicPropertiesSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e7b86-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7b86-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e7b86-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7b86-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e7b86-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7b86-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e7b86-108">DESCRIPTION</span></span>
<span data-ttu-id="e7b86-109">**AzServiceBusTopic** cmdlet은 지정 된 Service Bus 네임 스페이스에서 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b86-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e7b86-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e7b86-110">EXAMPLES</span></span>

### <span data-ttu-id="e7b86-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e7b86-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="e7b86-112">`SB-Topic_exampl1`네임 스페이스에서 항목을 제거 `SB-Example1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b86-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="e7b86-113">예제 2.1-InputObject-Using 변수:</span><span class="sxs-lookup"><span data-stu-id="e7b86-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="e7b86-114">예제 2.2-InputObject-Using 파이핑:</span><span class="sxs-lookup"><span data-stu-id="e7b86-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="e7b86-115">예제 3.1-변수를 사용 하는 ResourceId:</span><span class="sxs-lookup"><span data-stu-id="e7b86-115">Example 3.1 - ResourceId Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="e7b86-116">예제 3.2-문자열 값을 사용 하는 ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7b86-116">Example 3.2 - ResourceId Using String value</span></span>
```
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="e7b86-117">변수</span><span class="sxs-lookup"><span data-stu-id="e7b86-117">PARAMETERS</span></span>

### <span data-ttu-id="e7b86-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7b86-118">-AsJob</span></span>
<span data-ttu-id="e7b86-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e7b86-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7b86-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7b86-120">-DefaultProfile</span></span>
<span data-ttu-id="e7b86-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7b86-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7b86-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7b86-122">-InputObject</span></span>
<span data-ttu-id="e7b86-123">Service Bus 항목 개체</span><span class="sxs-lookup"><span data-stu-id="e7b86-123">Service Bus Topic Object</span></span>

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

### <span data-ttu-id="e7b86-124">-이름</span><span class="sxs-lookup"><span data-stu-id="e7b86-124">-Name</span></span>
<span data-ttu-id="e7b86-125">주제 이름</span><span class="sxs-lookup"><span data-stu-id="e7b86-125">Topic Name</span></span>

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

### <span data-ttu-id="e7b86-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e7b86-126">-Namespace</span></span>
<span data-ttu-id="e7b86-127">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="e7b86-127">Namespace Name</span></span>

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

### <span data-ttu-id="e7b86-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7b86-128">-PassThru</span></span>
<span data-ttu-id="e7b86-129">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b86-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e7b86-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7b86-130">-ResourceGroupName</span></span>
<span data-ttu-id="e7b86-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7b86-131">The name of the resource group</span></span>

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

### <span data-ttu-id="e7b86-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7b86-132">-ResourceId</span></span>
<span data-ttu-id="e7b86-133">Service Bus 항목 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="e7b86-133">Service Bus Topic Resource Id</span></span>

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

### <span data-ttu-id="e7b86-134">-확인</span><span class="sxs-lookup"><span data-stu-id="e7b86-134">-Confirm</span></span>
<span data-ttu-id="e7b86-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b86-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7b86-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7b86-136">-WhatIf</span></span>
<span data-ttu-id="e7b86-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7b86-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7b86-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b86-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7b86-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7b86-139">CommonParameters</span></span>
<span data-ttu-id="e7b86-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b86-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7b86-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7b86-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7b86-142">입력</span><span class="sxs-lookup"><span data-stu-id="e7b86-142">INPUTS</span></span>

### <span data-ttu-id="e7b86-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e7b86-143">System.String</span></span>

### <span data-ttu-id="e7b86-144">ServiceBus. a. m/.Ppstop특성</span><span class="sxs-lookup"><span data-stu-id="e7b86-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="e7b86-145">출력</span><span class="sxs-lookup"><span data-stu-id="e7b86-145">OUTPUTS</span></span>

### <span data-ttu-id="e7b86-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e7b86-146">System.Boolean</span></span>

## <span data-ttu-id="e7b86-147">상속자</span><span class="sxs-lookup"><span data-stu-id="e7b86-147">NOTES</span></span>

## <span data-ttu-id="e7b86-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7b86-148">RELATED LINKS</span></span>
