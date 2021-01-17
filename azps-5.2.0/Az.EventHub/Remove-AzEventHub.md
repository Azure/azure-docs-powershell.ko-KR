---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: daa63859c9649d9467f750f77d5b0e466d03ff56
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353162"
---
# <span data-ttu-id="5f1ea-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="5f1ea-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="5f1ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f1ea-102">SYNOPSIS</span></span>
<span data-ttu-id="5f1ea-103">지정된 이벤트 허브를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5f1ea-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="5f1ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="5f1ea-104">SYNTAX</span></span>

### <span data-ttu-id="5f1ea-105">EventhubDefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5f1ea-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f1ea-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5f1ea-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f1ea-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f1ea-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f1ea-108">설명</span><span class="sxs-lookup"><span data-stu-id="5f1ea-108">DESCRIPTION</span></span>
<span data-ttu-id="5f1ea-109">이 Remove-AzEventHub cmdlet은 지정된 네임스페이스에서 지정된 이벤트 허브를 제거하고 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5f1ea-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="5f1ea-110">예제</span><span class="sxs-lookup"><span data-stu-id="5f1ea-110">EXAMPLES</span></span>

### <span data-ttu-id="5f1ea-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5f1ea-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="5f1ea-112">Event Hub \` MyEventHubName을 \` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5f1ea-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="5f1ea-113">예제 2: InputObject - 변수 사용:</span><span class="sxs-lookup"><span data-stu-id="5f1ea-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="5f1ea-114">예제 3: 파이핑을 사용하는 InputObject:</span><span class="sxs-lookup"><span data-stu-id="5f1ea-114">Example 3: InputObject Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="5f1ea-115">예제 4: ResourceId - 변수 사용:</span><span class="sxs-lookup"><span data-stu-id="5f1ea-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="5f1ea-116">예제 5: ResourceId - 문자열 사용:</span><span class="sxs-lookup"><span data-stu-id="5f1ea-116">Example 5: ResourceId - Using string:</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="5f1ea-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f1ea-117">PARAMETERS</span></span>

### <span data-ttu-id="5f1ea-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f1ea-118">-AsJob</span></span>
<span data-ttu-id="5f1ea-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5f1ea-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f1ea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f1ea-120">-DefaultProfile</span></span>
<span data-ttu-id="5f1ea-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f1ea-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f1ea-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f1ea-122">-InputObject</span></span>
<span data-ttu-id="5f1ea-123">Eventhub 개체</span><span class="sxs-lookup"><span data-stu-id="5f1ea-123">Eventhub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f1ea-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5f1ea-124">-Name</span></span>
<span data-ttu-id="5f1ea-125">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="5f1ea-125">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f1ea-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5f1ea-126">-Namespace</span></span>
<span data-ttu-id="5f1ea-127">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="5f1ea-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f1ea-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f1ea-128">-PassThru</span></span>
<span data-ttu-id="5f1ea-129">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f1ea-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="5f1ea-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f1ea-130">-ResourceGroupName</span></span>
<span data-ttu-id="5f1ea-131">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5f1ea-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f1ea-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f1ea-132">-ResourceId</span></span>
<span data-ttu-id="5f1ea-133">Eventhub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="5f1ea-133">Eventhub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f1ea-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f1ea-134">-Confirm</span></span>
<span data-ttu-id="5f1ea-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f1ea-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f1ea-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f1ea-136">-WhatIf</span></span>
<span data-ttu-id="5f1ea-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5f1ea-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f1ea-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5f1ea-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f1ea-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f1ea-139">CommonParameters</span></span>
<span data-ttu-id="5f1ea-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5f1ea-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f1ea-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5f1ea-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f1ea-142">입력</span><span class="sxs-lookup"><span data-stu-id="5f1ea-142">INPUTS</span></span>

### <span data-ttu-id="5f1ea-143">System.String</span><span class="sxs-lookup"><span data-stu-id="5f1ea-143">System.String</span></span>

### <span data-ttu-id="5f1ea-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="5f1ea-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="5f1ea-145">출력</span><span class="sxs-lookup"><span data-stu-id="5f1ea-145">OUTPUTS</span></span>

### <span data-ttu-id="5f1ea-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5f1ea-146">System.Boolean</span></span>

## <span data-ttu-id="5f1ea-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5f1ea-147">NOTES</span></span>

## <span data-ttu-id="5f1ea-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f1ea-148">RELATED LINKS</span></span>
