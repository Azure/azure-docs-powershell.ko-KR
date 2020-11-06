---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
ms.openlocfilehash: 31ed4d8765599fcc99f58870b347a14cdaf00162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531995"
---
# <span data-ttu-id="dc62a-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="dc62a-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="dc62a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc62a-102">SYNOPSIS</span></span>
<span data-ttu-id="dc62a-103">지정 된 이벤트 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc62a-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc62a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc62a-104">SYNTAX</span></span>

### <span data-ttu-id="dc62a-105">EventhubDefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="dc62a-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc62a-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dc62a-106">EventhubInputObjectSet</span></span>
```
Remove-AzureRmEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc62a-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc62a-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc62a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dc62a-108">DESCRIPTION</span></span>
<span data-ttu-id="dc62a-109">Remove-AzureRmEventHub cmdlet은 주어진 네임 스페이스에서 지정 된 이벤트 허브를 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc62a-109">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="dc62a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="dc62a-110">EXAMPLES</span></span>

### <span data-ttu-id="dc62a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="dc62a-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="dc62a-112">이벤트 허브 MyEventHubName를 \` 제거 \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc62a-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="dc62a-113">예제 2.1-InputObject-Using 변수:</span><span class="sxs-lookup"><span data-stu-id="dc62a-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmEventHub <params>
PS C:\> Remove-AzureRmEventHub -InputObject $inputobject
```

### <span data-ttu-id="dc62a-114">예제 2.2-파이핑을 사용한 InputObject:</span><span class="sxs-lookup"><span data-stu-id="dc62a-114">Example 2.2 - InputObject Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHub <params> | Remove-AzureRmEventHub
```

### <span data-ttu-id="dc62a-115">예제 3.1-ResourceId-변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc62a-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHub <params>
PS C:\> Remove-AzureRmEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="dc62a-116">예제 3.1-ResourceId-문자열을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc62a-116">Example 3.1 - ResourceId - Using string:</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="dc62a-117">변수</span><span class="sxs-lookup"><span data-stu-id="dc62a-117">PARAMETERS</span></span>

### <span data-ttu-id="dc62a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc62a-118">-AsJob</span></span>
<span data-ttu-id="dc62a-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dc62a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc62a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc62a-120">-DefaultProfile</span></span>
<span data-ttu-id="dc62a-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc62a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc62a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc62a-122">-InputObject</span></span>
<span data-ttu-id="dc62a-123">Eventhub 개체</span><span class="sxs-lookup"><span data-stu-id="dc62a-123">Eventhub Object</span></span>

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

### <span data-ttu-id="dc62a-124">-이름</span><span class="sxs-lookup"><span data-stu-id="dc62a-124">-Name</span></span>
<span data-ttu-id="dc62a-125">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="dc62a-125">EventHub Name</span></span>

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

### <span data-ttu-id="dc62a-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dc62a-126">-Namespace</span></span>
<span data-ttu-id="dc62a-127">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="dc62a-127">Namespace Name</span></span>

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

### <span data-ttu-id="dc62a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc62a-128">-PassThru</span></span>
<span data-ttu-id="dc62a-129">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc62a-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="dc62a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc62a-130">-ResourceGroupName</span></span>
<span data-ttu-id="dc62a-131">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="dc62a-131">Resource Group Name</span></span>

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

### <span data-ttu-id="dc62a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc62a-132">-ResourceId</span></span>
<span data-ttu-id="dc62a-133">Eventhub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="dc62a-133">Eventhub Resource Id</span></span>

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

### <span data-ttu-id="dc62a-134">-확인</span><span class="sxs-lookup"><span data-stu-id="dc62a-134">-Confirm</span></span>
<span data-ttu-id="dc62a-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc62a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc62a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc62a-136">-WhatIf</span></span>
<span data-ttu-id="dc62a-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dc62a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc62a-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc62a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc62a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc62a-139">CommonParameters</span></span>
<span data-ttu-id="dc62a-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc62a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc62a-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc62a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc62a-142">입력</span><span class="sxs-lookup"><span data-stu-id="dc62a-142">INPUTS</span></span>

### <span data-ttu-id="dc62a-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dc62a-143">System.String</span></span>

### <span data-ttu-id="dc62a-144">PSEventHubAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="dc62a-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>
<span data-ttu-id="dc62a-145">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dc62a-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="dc62a-146">출력</span><span class="sxs-lookup"><span data-stu-id="dc62a-146">OUTPUTS</span></span>

### <span data-ttu-id="dc62a-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="dc62a-147">System.Boolean</span></span>

## <span data-ttu-id="dc62a-148">상속자</span><span class="sxs-lookup"><span data-stu-id="dc62a-148">NOTES</span></span>

## <span data-ttu-id="dc62a-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc62a-149">RELATED LINKS</span></span>
