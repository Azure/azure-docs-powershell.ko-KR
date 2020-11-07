---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 4d5ddbc4dff2922b90bc6d1117ff32473afd9042
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700828"
---
# <span data-ttu-id="c388e-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="c388e-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="c388e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c388e-102">SYNOPSIS</span></span>
<span data-ttu-id="c388e-103">지정 된 이벤트 허브 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c388e-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="c388e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c388e-104">SYNTAX</span></span>

### <span data-ttu-id="c388e-105">NamespaceParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c388e-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c388e-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c388e-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c388e-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c388e-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c388e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c388e-108">DESCRIPTION</span></span>
<span data-ttu-id="c388e-109">Remove-AzEventHubNamespace cmdlet은 지정 된 이벤트 허브 네임 스페이스를 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c388e-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="c388e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c388e-110">EXAMPLES</span></span>

### <span data-ttu-id="c388e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c388e-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="c388e-112">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 허브 네임 스페이스 MyNamespaceName를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="c388e-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c388e-113">예제 2.1-InputObject-Using 변수:</span><span class="sxs-lookup"><span data-stu-id="c388e-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="c388e-114">예제 2.1-InputObject-Using 파이핑:</span><span class="sxs-lookup"><span data-stu-id="c388e-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="c388e-115">예제 3.1-ResourceId-변수 사용</span><span class="sxs-lookup"><span data-stu-id="c388e-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="c388e-116">예제 3.2-ResourceId-파이핑을 사용:</span><span class="sxs-lookup"><span data-stu-id="c388e-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="c388e-117">예제 3.3-ResourceId-문자열을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c388e-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="c388e-118">변수</span><span class="sxs-lookup"><span data-stu-id="c388e-118">PARAMETERS</span></span>

### <span data-ttu-id="c388e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c388e-119">-AsJob</span></span>
<span data-ttu-id="c388e-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c388e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c388e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c388e-121">-DefaultProfile</span></span>
<span data-ttu-id="c388e-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c388e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c388e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c388e-123">-InputObject</span></span>
<span data-ttu-id="c388e-124">EventHubs 네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="c388e-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="c388e-125">-이름</span><span class="sxs-lookup"><span data-stu-id="c388e-125">-Name</span></span>
<span data-ttu-id="c388e-126">EventHub 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="c388e-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="c388e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c388e-127">-PassThru</span></span>
<span data-ttu-id="c388e-128">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c388e-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c388e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c388e-129">-ResourceGroupName</span></span>
<span data-ttu-id="c388e-130">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c388e-130">Resource Group Name</span></span>

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

### <span data-ttu-id="c388e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c388e-131">-ResourceId</span></span>
<span data-ttu-id="c388e-132">EventHubs 네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="c388e-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="c388e-133">-확인</span><span class="sxs-lookup"><span data-stu-id="c388e-133">-Confirm</span></span>
<span data-ttu-id="c388e-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c388e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c388e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c388e-135">-WhatIf</span></span>
<span data-ttu-id="c388e-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c388e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c388e-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c388e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c388e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c388e-138">CommonParameters</span></span>
<span data-ttu-id="c388e-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c388e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c388e-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c388e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c388e-141">입력</span><span class="sxs-lookup"><span data-stu-id="c388e-141">INPUTS</span></span>

### <span data-ttu-id="c388e-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c388e-142">System.String</span></span>

### <span data-ttu-id="c388e-143">PSNamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="c388e-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="c388e-144">출력</span><span class="sxs-lookup"><span data-stu-id="c388e-144">OUTPUTS</span></span>

### <span data-ttu-id="c388e-145">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="c388e-145">System.Void</span></span>

## <span data-ttu-id="c388e-146">상속자</span><span class="sxs-lookup"><span data-stu-id="c388e-146">NOTES</span></span>

## <span data-ttu-id="c388e-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c388e-147">RELATED LINKS</span></span>
