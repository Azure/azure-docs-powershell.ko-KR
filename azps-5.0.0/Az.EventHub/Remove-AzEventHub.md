---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: daa63859c9649d9467f750f77d5b0e466d03ff56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215460"
---
# <span data-ttu-id="7fcdf-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="7fcdf-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="7fcdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fcdf-102">SYNOPSIS</span></span>
<span data-ttu-id="7fcdf-103">지정 된 이벤트 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fcdf-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="7fcdf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7fcdf-104">SYNTAX</span></span>

### <span data-ttu-id="7fcdf-105">EventhubDefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7fcdf-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fcdf-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7fcdf-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fcdf-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fcdf-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fcdf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7fcdf-108">DESCRIPTION</span></span>
<span data-ttu-id="7fcdf-109">Remove-AzEventHub cmdlet은 주어진 네임 스페이스에서 지정 된 이벤트 허브를 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fcdf-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="7fcdf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7fcdf-110">EXAMPLES</span></span>

### <span data-ttu-id="7fcdf-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7fcdf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="7fcdf-112">이벤트 허브 MyEventHubName를 \` 제거 \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fcdf-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="7fcdf-113">예제 2: InputObject를 사용 하는 변수:</span><span class="sxs-lookup"><span data-stu-id="7fcdf-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="7fcdf-114">예제 3: 파이핑을 사용 하는 InputObject:</span><span class="sxs-lookup"><span data-stu-id="7fcdf-114">Example 3: InputObject Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="7fcdf-115">예제 4: ResourceId를 사용 하는 변수:</span><span class="sxs-lookup"><span data-stu-id="7fcdf-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="7fcdf-116">예 5: ResourceId-string을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fcdf-116">Example 5: ResourceId - Using string:</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="7fcdf-117">변수</span><span class="sxs-lookup"><span data-stu-id="7fcdf-117">PARAMETERS</span></span>

### <span data-ttu-id="7fcdf-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fcdf-118">-AsJob</span></span>
<span data-ttu-id="7fcdf-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7fcdf-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fcdf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fcdf-120">-DefaultProfile</span></span>
<span data-ttu-id="7fcdf-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7fcdf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fcdf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fcdf-122">-InputObject</span></span>
<span data-ttu-id="7fcdf-123">Eventhub 개체</span><span class="sxs-lookup"><span data-stu-id="7fcdf-123">Eventhub Object</span></span>

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

### <span data-ttu-id="7fcdf-124">-이름</span><span class="sxs-lookup"><span data-stu-id="7fcdf-124">-Name</span></span>
<span data-ttu-id="7fcdf-125">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="7fcdf-125">EventHub Name</span></span>

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

### <span data-ttu-id="7fcdf-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7fcdf-126">-Namespace</span></span>
<span data-ttu-id="7fcdf-127">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="7fcdf-127">Namespace Name</span></span>

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

### <span data-ttu-id="7fcdf-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fcdf-128">-PassThru</span></span>
<span data-ttu-id="7fcdf-129">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fcdf-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7fcdf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fcdf-130">-ResourceGroupName</span></span>
<span data-ttu-id="7fcdf-131">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7fcdf-131">Resource Group Name</span></span>

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

### <span data-ttu-id="7fcdf-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fcdf-132">-ResourceId</span></span>
<span data-ttu-id="7fcdf-133">Eventhub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="7fcdf-133">Eventhub Resource Id</span></span>

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

### <span data-ttu-id="7fcdf-134">-확인</span><span class="sxs-lookup"><span data-stu-id="7fcdf-134">-Confirm</span></span>
<span data-ttu-id="7fcdf-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fcdf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fcdf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fcdf-136">-WhatIf</span></span>
<span data-ttu-id="7fcdf-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7fcdf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fcdf-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7fcdf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fcdf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fcdf-139">CommonParameters</span></span>
<span data-ttu-id="7fcdf-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fcdf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fcdf-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fcdf-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fcdf-142">입력</span><span class="sxs-lookup"><span data-stu-id="7fcdf-142">INPUTS</span></span>

### <span data-ttu-id="7fcdf-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7fcdf-143">System.String</span></span>

### <span data-ttu-id="7fcdf-144">PSEventHubAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="7fcdf-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="7fcdf-145">출력</span><span class="sxs-lookup"><span data-stu-id="7fcdf-145">OUTPUTS</span></span>

### <span data-ttu-id="7fcdf-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7fcdf-146">System.Boolean</span></span>

## <span data-ttu-id="7fcdf-147">상속자</span><span class="sxs-lookup"><span data-stu-id="7fcdf-147">NOTES</span></span>

## <span data-ttu-id="7fcdf-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7fcdf-148">RELATED LINKS</span></span>
