---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 29f2b961637a398470f6455d0d2330ce5fd863a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353102"
---
# <span data-ttu-id="600c1-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="600c1-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="600c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="600c1-102">SYNOPSIS</span></span>
<span data-ttu-id="600c1-103">지정된 Event Hubs 네임스페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="600c1-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="600c1-104">구문</span><span class="sxs-lookup"><span data-stu-id="600c1-104">SYNTAX</span></span>

### <span data-ttu-id="600c1-105">NamespaceParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="600c1-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="600c1-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="600c1-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="600c1-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="600c1-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="600c1-108">설명</span><span class="sxs-lookup"><span data-stu-id="600c1-108">DESCRIPTION</span></span>
<span data-ttu-id="600c1-109">이 Remove-AzEventHubNamespace cmdlet은 지정된 Event Hubs 네임스페이스를 제거하고 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="600c1-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="600c1-110">예제</span><span class="sxs-lookup"><span data-stu-id="600c1-110">EXAMPLES</span></span>

### <span data-ttu-id="600c1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="600c1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="600c1-112">리소스 그룹 \` MyResourceGroupName에서 Event Hubs 네임스페이스 \` \` MyNamespaceName을 \` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="600c1-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="600c1-113">예제 2: InputObject - 변수 사용:</span><span class="sxs-lookup"><span data-stu-id="600c1-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="600c1-114">예제 3: InputObject - 파이핑 사용:</span><span class="sxs-lookup"><span data-stu-id="600c1-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="600c1-115">예제 4: ResourceId - 변수 사용</span><span class="sxs-lookup"><span data-stu-id="600c1-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="600c1-116">예제 5: ResourceId - 파이핑 사용:</span><span class="sxs-lookup"><span data-stu-id="600c1-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="600c1-117">예제 6: ResourceId - 문자열 사용:</span><span class="sxs-lookup"><span data-stu-id="600c1-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="600c1-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="600c1-118">PARAMETERS</span></span>

### <span data-ttu-id="600c1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="600c1-119">-AsJob</span></span>
<span data-ttu-id="600c1-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="600c1-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="600c1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="600c1-121">-DefaultProfile</span></span>
<span data-ttu-id="600c1-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="600c1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="600c1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="600c1-123">-InputObject</span></span>
<span data-ttu-id="600c1-124">EventHubs 네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="600c1-124">EventHubs Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="600c1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="600c1-125">-Name</span></span>
<span data-ttu-id="600c1-126">EventHub 네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="600c1-126">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600c1-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="600c1-127">-PassThru</span></span>
<span data-ttu-id="600c1-128">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="600c1-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="600c1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="600c1-129">-ResourceGroupName</span></span>
<span data-ttu-id="600c1-130">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="600c1-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600c1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="600c1-131">-ResourceId</span></span>
<span data-ttu-id="600c1-132">EventHubs 네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="600c1-132">EventHubs Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600c1-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="600c1-133">-Confirm</span></span>
<span data-ttu-id="600c1-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="600c1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="600c1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="600c1-135">-WhatIf</span></span>
<span data-ttu-id="600c1-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="600c1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="600c1-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="600c1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="600c1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="600c1-138">CommonParameters</span></span>
<span data-ttu-id="600c1-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="600c1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="600c1-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="600c1-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="600c1-141">입력</span><span class="sxs-lookup"><span data-stu-id="600c1-141">INPUTS</span></span>

### <span data-ttu-id="600c1-142">System.String</span><span class="sxs-lookup"><span data-stu-id="600c1-142">System.String</span></span>

### <span data-ttu-id="600c1-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="600c1-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="600c1-144">출력</span><span class="sxs-lookup"><span data-stu-id="600c1-144">OUTPUTS</span></span>

### <span data-ttu-id="600c1-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="600c1-145">System.Void</span></span>

## <span data-ttu-id="600c1-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="600c1-146">NOTES</span></span>

## <span data-ttu-id="600c1-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="600c1-147">RELATED LINKS</span></span>
