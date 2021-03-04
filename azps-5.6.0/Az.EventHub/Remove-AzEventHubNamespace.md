---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: dca9094ac66e889b5a00899f6d48d6317279c1fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955920"
---
# <span data-ttu-id="86987-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="86987-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="86987-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86987-102">SYNOPSIS</span></span>
<span data-ttu-id="86987-103">지정된 Event Hubs 네임스페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="86987-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="86987-104">구문</span><span class="sxs-lookup"><span data-stu-id="86987-104">SYNTAX</span></span>

### <span data-ttu-id="86987-105">네임스페이스ParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="86987-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86987-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="86987-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86987-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86987-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86987-108">설명</span><span class="sxs-lookup"><span data-stu-id="86987-108">DESCRIPTION</span></span>
<span data-ttu-id="86987-109">Remove-AzEventHubNamespace cmdlet은 지정된 Event Hubs 네임스페이스를 제거하고 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="86987-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="86987-110">예제</span><span class="sxs-lookup"><span data-stu-id="86987-110">EXAMPLES</span></span>

### <span data-ttu-id="86987-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="86987-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="86987-112">리소스 그룹 \` \` \` MyResourceGroupName에서 Event Hubs 네임스페이스 MyNamespaceName을 \` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="86987-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="86987-113">예제 2: InputObject - 변수 사용:</span><span class="sxs-lookup"><span data-stu-id="86987-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="86987-114">예제 3: InputObject - 배관 사용:</span><span class="sxs-lookup"><span data-stu-id="86987-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="86987-115">예제 4: ResourceId - 변수 사용</span><span class="sxs-lookup"><span data-stu-id="86987-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="86987-116">예제 5: ResourceId - 배관 사용:</span><span class="sxs-lookup"><span data-stu-id="86987-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="86987-117">예제 6: ResourceId - 문자열 사용:</span><span class="sxs-lookup"><span data-stu-id="86987-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="86987-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="86987-118">PARAMETERS</span></span>

### <span data-ttu-id="86987-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86987-119">-AsJob</span></span>
<span data-ttu-id="86987-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="86987-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86987-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86987-121">-DefaultProfile</span></span>
<span data-ttu-id="86987-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86987-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86987-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86987-123">-InputObject</span></span>
<span data-ttu-id="86987-124">EventHubs 네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="86987-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="86987-125">-Name</span><span class="sxs-lookup"><span data-stu-id="86987-125">-Name</span></span>
<span data-ttu-id="86987-126">EventHub 네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="86987-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="86987-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86987-127">-PassThru</span></span>
<span data-ttu-id="86987-128">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="86987-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="86987-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86987-129">-ResourceGroupName</span></span>
<span data-ttu-id="86987-130">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="86987-130">Resource Group Name</span></span>

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

### <span data-ttu-id="86987-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86987-131">-ResourceId</span></span>
<span data-ttu-id="86987-132">EventHubs 네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="86987-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="86987-133">-확인</span><span class="sxs-lookup"><span data-stu-id="86987-133">-Confirm</span></span>
<span data-ttu-id="86987-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="86987-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86987-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86987-135">-WhatIf</span></span>
<span data-ttu-id="86987-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="86987-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86987-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86987-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86987-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86987-138">CommonParameters</span></span>
<span data-ttu-id="86987-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="86987-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86987-140">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="86987-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86987-141">입력</span><span class="sxs-lookup"><span data-stu-id="86987-141">INPUTS</span></span>

### <span data-ttu-id="86987-142">System.String</span><span class="sxs-lookup"><span data-stu-id="86987-142">System.String</span></span>

### <span data-ttu-id="86987-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="86987-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="86987-144">출력</span><span class="sxs-lookup"><span data-stu-id="86987-144">OUTPUTS</span></span>

### <span data-ttu-id="86987-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="86987-145">System.Void</span></span>

## <span data-ttu-id="86987-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="86987-146">NOTES</span></span>

## <span data-ttu-id="86987-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86987-147">RELATED LINKS</span></span>
