---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6df8d5539bf340df5e00ad69ac557bc2cbb8ccaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530342"
---
# <span data-ttu-id="3a81d-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="3a81d-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="3a81d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a81d-102">SYNOPSIS</span></span>
<span data-ttu-id="3a81d-103">지정 된 이벤트 허브 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a81d-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a81d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3a81d-104">SYNTAX</span></span>

### <span data-ttu-id="3a81d-105">NamespaceParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3a81d-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a81d-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3a81d-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a81d-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a81d-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a81d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3a81d-108">DESCRIPTION</span></span>
<span data-ttu-id="3a81d-109">Remove-AzureRmEventHubNamespace cmdlet은 지정 된 이벤트 허브 네임 스페이스를 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a81d-109">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="3a81d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3a81d-110">EXAMPLES</span></span>

### <span data-ttu-id="3a81d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3a81d-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="3a81d-112">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 허브 네임 스페이스 MyNamespaceName를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="3a81d-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3a81d-113">예제 2.1-InputObject-Using 변수:</span><span class="sxs-lookup"><span data-stu-id="3a81d-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzureRmEventHubNamespace <params> 
PS C:\> Remove-AzureRmEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="3a81d-114">예제 2.1-InputObject-Using 파이핑:</span><span class="sxs-lookup"><span data-stu-id="3a81d-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace <params> | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="3a81d-115">예제 3.1-ResourceId-변수 사용</span><span class="sxs-lookup"><span data-stu-id="3a81d-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubNamespace <params>
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="3a81d-116">예제 3.2-ResourceId-파이핑을 사용:</span><span class="sxs-lookup"><span data-stu-id="3a81d-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzureRmResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="3a81d-117">예제 3.3-ResourceId-문자열을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a81d-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="3a81d-118">변수</span><span class="sxs-lookup"><span data-stu-id="3a81d-118">PARAMETERS</span></span>

### <span data-ttu-id="3a81d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a81d-119">-AsJob</span></span>
<span data-ttu-id="3a81d-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3a81d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a81d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a81d-121">-DefaultProfile</span></span>
<span data-ttu-id="3a81d-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a81d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a81d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a81d-123">-InputObject</span></span>
<span data-ttu-id="3a81d-124">EventHubs 네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="3a81d-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="3a81d-125">-이름</span><span class="sxs-lookup"><span data-stu-id="3a81d-125">-Name</span></span>
<span data-ttu-id="3a81d-126">EventHub 네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="3a81d-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="3a81d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a81d-127">-PassThru</span></span>
<span data-ttu-id="3a81d-128">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a81d-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="3a81d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a81d-129">-ResourceGroupName</span></span>
<span data-ttu-id="3a81d-130">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3a81d-130">Resource Group Name</span></span>

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

### <span data-ttu-id="3a81d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a81d-131">-ResourceId</span></span>
<span data-ttu-id="3a81d-132">EventHubs 네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="3a81d-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="3a81d-133">-확인</span><span class="sxs-lookup"><span data-stu-id="3a81d-133">-Confirm</span></span>
<span data-ttu-id="3a81d-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a81d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a81d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a81d-135">-WhatIf</span></span>
<span data-ttu-id="3a81d-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a81d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a81d-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a81d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a81d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a81d-138">CommonParameters</span></span>
<span data-ttu-id="3a81d-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a81d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a81d-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a81d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a81d-141">입력</span><span class="sxs-lookup"><span data-stu-id="3a81d-141">INPUTS</span></span>

### <span data-ttu-id="3a81d-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3a81d-142">System.String</span></span>

### <span data-ttu-id="3a81d-143">PSNamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="3a81d-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="3a81d-144">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3a81d-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="3a81d-145">출력</span><span class="sxs-lookup"><span data-stu-id="3a81d-145">OUTPUTS</span></span>

### <span data-ttu-id="3a81d-146">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="3a81d-146">System.Void</span></span>

## <span data-ttu-id="3a81d-147">상속자</span><span class="sxs-lookup"><span data-stu-id="3a81d-147">NOTES</span></span>

## <span data-ttu-id="3a81d-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a81d-148">RELATED LINKS</span></span>
