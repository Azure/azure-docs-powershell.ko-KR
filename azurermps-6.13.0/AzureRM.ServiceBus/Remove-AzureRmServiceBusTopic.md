---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: 8434893dd3661bbfb1f78a4973dc206f44e9f400
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526032"
---
# <span data-ttu-id="205e8-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="205e8-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="205e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="205e8-102">SYNOPSIS</span></span>
<span data-ttu-id="205e8-103">지정 된 Service Bus 네임 스페이스에서 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="205e8-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="205e8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="205e8-104">SYNTAX</span></span>

### <span data-ttu-id="205e8-105">TopicPropertiesSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="205e8-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="205e8-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="205e8-106">TopicInputObjectSet</span></span>
```
Remove-AzureRmServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="205e8-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="205e8-107">TopicResourceIdSet</span></span>
```
Remove-AzureRmServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="205e8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="205e8-108">DESCRIPTION</span></span>
<span data-ttu-id="205e8-109">**AzureRmServiceBusTopic** cmdlet은 지정 된 Service Bus 네임 스페이스에서 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="205e8-109">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="205e8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="205e8-110">EXAMPLES</span></span>

### <span data-ttu-id="205e8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="205e8-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="205e8-112">`SB-Topic_exampl1`네임 스페이스에서 항목을 제거 `SB-Example1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="205e8-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="205e8-113">예제 2.1-InputObject-Using 변수:</span><span class="sxs-lookup"><span data-stu-id="205e8-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusTopic <parmas>
PS C:\> Remove-AzureRmServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="205e8-114">예제 2.2-InputObject-Using 파이핑:</span><span class="sxs-lookup"><span data-stu-id="205e8-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic <parmas> | Remove-AzureRmServiceBusTopic
```

### <span data-ttu-id="205e8-115">예제 3.1-변수를 사용 하는 ResourceId:</span><span class="sxs-lookup"><span data-stu-id="205e8-115">Example 3.1 - ResourceId Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusTopic <params>
PS C:\> Remove-AzureRmServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="205e8-116">예제 3.2-문자열 값을 사용 하는 ResourceId</span><span class="sxs-lookup"><span data-stu-id="205e8-116">Example 3.2 - ResourceId Using String value</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="205e8-117">변수</span><span class="sxs-lookup"><span data-stu-id="205e8-117">PARAMETERS</span></span>

### <span data-ttu-id="205e8-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="205e8-118">-AsJob</span></span>
<span data-ttu-id="205e8-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="205e8-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="205e8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="205e8-120">-DefaultProfile</span></span>
<span data-ttu-id="205e8-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="205e8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205e8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="205e8-122">-InputObject</span></span>
<span data-ttu-id="205e8-123">Service Bus 항목 개체</span><span class="sxs-lookup"><span data-stu-id="205e8-123">Service Bus Topic Object</span></span>

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

### <span data-ttu-id="205e8-124">-이름</span><span class="sxs-lookup"><span data-stu-id="205e8-124">-Name</span></span>
<span data-ttu-id="205e8-125">주제 이름</span><span class="sxs-lookup"><span data-stu-id="205e8-125">Topic Name</span></span>

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

### <span data-ttu-id="205e8-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="205e8-126">-Namespace</span></span>
<span data-ttu-id="205e8-127">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="205e8-127">Namespace Name</span></span>

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

### <span data-ttu-id="205e8-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="205e8-128">-PassThru</span></span>
<span data-ttu-id="205e8-129">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="205e8-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="205e8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="205e8-130">-ResourceGroupName</span></span>
<span data-ttu-id="205e8-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="205e8-131">The name of the resource group</span></span>

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

### <span data-ttu-id="205e8-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="205e8-132">-ResourceId</span></span>
<span data-ttu-id="205e8-133">Service Bus 항목 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="205e8-133">Service Bus Topic Resource Id</span></span>

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

### <span data-ttu-id="205e8-134">-확인</span><span class="sxs-lookup"><span data-stu-id="205e8-134">-Confirm</span></span>
<span data-ttu-id="205e8-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="205e8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="205e8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="205e8-136">-WhatIf</span></span>
<span data-ttu-id="205e8-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="205e8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="205e8-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="205e8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="205e8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205e8-139">CommonParameters</span></span>
<span data-ttu-id="205e8-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="205e8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205e8-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="205e8-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205e8-142">입력</span><span class="sxs-lookup"><span data-stu-id="205e8-142">INPUTS</span></span>

### <span data-ttu-id="205e8-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="205e8-143">System.String</span></span>

### <span data-ttu-id="205e8-144">ServiceBus. a. m/.Ppstop특성</span><span class="sxs-lookup"><span data-stu-id="205e8-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="205e8-145">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="205e8-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="205e8-146">출력</span><span class="sxs-lookup"><span data-stu-id="205e8-146">OUTPUTS</span></span>

### <span data-ttu-id="205e8-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="205e8-147">System.Boolean</span></span>

## <span data-ttu-id="205e8-148">상속자</span><span class="sxs-lookup"><span data-stu-id="205e8-148">NOTES</span></span>

## <span data-ttu-id="205e8-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="205e8-149">RELATED LINKS</span></span>
