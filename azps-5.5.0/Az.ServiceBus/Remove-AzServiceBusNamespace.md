---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 49b6a29410bd6c670e74b072a48b6f2a79e8fd0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189108"
---
# <span data-ttu-id="782a4-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="782a4-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="782a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="782a4-102">SYNOPSIS</span></span>
<span data-ttu-id="782a4-103">지정된 리소스 그룹에서 네임스페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="782a4-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="782a4-104">구문</span><span class="sxs-lookup"><span data-stu-id="782a4-104">SYNTAX</span></span>

### <span data-ttu-id="782a4-105">NamespacePropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="782a4-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="782a4-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="782a4-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="782a4-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="782a4-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="782a4-108">설명</span><span class="sxs-lookup"><span data-stu-id="782a4-108">DESCRIPTION</span></span>
<span data-ttu-id="782a4-109">**Remove-AzServiceBusNamespace** cmdlet은 지정된 리소스 그룹에서 네임스페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="782a4-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="782a4-110">예제</span><span class="sxs-lookup"><span data-stu-id="782a4-110">EXAMPLES</span></span>

### <span data-ttu-id="782a4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="782a4-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="782a4-112">지정된 리소스 그룹에서 Service Bus `SB-Example1` 네임스페이스를 `Default-ServiceBus-WestUS` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="782a4-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="782a4-113">예제 2.1 - InputObject - 변수 사용:</span><span class="sxs-lookup"><span data-stu-id="782a4-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="782a4-114">다음을 통해 제공된 Service Bus 네임스페이스를 $inputobject.</span><span class="sxs-lookup"><span data-stu-id="782a4-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="782a4-115">예제 2.2 - InputObject - 파이핑 사용:</span><span class="sxs-lookup"><span data-stu-id="782a4-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="782a4-116">Piping을 사용하여 Service Bus 네임스페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="782a4-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="782a4-117">예제 3 - ResourceId</span><span class="sxs-lookup"><span data-stu-id="782a4-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="782a4-118">-ResourceId 매개 변수에 대한 ARM 또는 파이핑을 통해 $resourceid ID를 통해 제공된 Service Bus 네임스페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="782a4-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="782a4-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="782a4-119">PARAMETERS</span></span>

### <span data-ttu-id="782a4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="782a4-120">-AsJob</span></span>
<span data-ttu-id="782a4-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="782a4-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="782a4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="782a4-122">-DefaultProfile</span></span>
<span data-ttu-id="782a4-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="782a4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="782a4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="782a4-124">-InputObject</span></span>
<span data-ttu-id="782a4-125">Service Bus 네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="782a4-125">Service Bus Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="782a4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="782a4-126">-Name</span></span>
<span data-ttu-id="782a4-127">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="782a4-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="782a4-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="782a4-128">-PassThru</span></span>
<span data-ttu-id="782a4-129">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="782a4-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="782a4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="782a4-130">-ResourceGroupName</span></span>
<span data-ttu-id="782a4-131">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="782a4-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="782a4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="782a4-132">-ResourceId</span></span>
<span data-ttu-id="782a4-133">Service Bus 네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="782a4-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="782a4-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="782a4-134">-Confirm</span></span>
<span data-ttu-id="782a4-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="782a4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="782a4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="782a4-136">-WhatIf</span></span>
<span data-ttu-id="782a4-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="782a4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="782a4-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="782a4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="782a4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="782a4-139">CommonParameters</span></span>
<span data-ttu-id="782a4-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="782a4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="782a4-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="782a4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="782a4-142">입력</span><span class="sxs-lookup"><span data-stu-id="782a4-142">INPUTS</span></span>

### <span data-ttu-id="782a4-143">System.String</span><span class="sxs-lookup"><span data-stu-id="782a4-143">System.String</span></span>

### <span data-ttu-id="782a4-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="782a4-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="782a4-145">출력</span><span class="sxs-lookup"><span data-stu-id="782a4-145">OUTPUTS</span></span>

### <span data-ttu-id="782a4-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="782a4-146">System.Boolean</span></span>

## <span data-ttu-id="782a4-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="782a4-147">NOTES</span></span>

## <span data-ttu-id="782a4-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="782a4-148">RELATED LINKS</span></span>
