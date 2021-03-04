---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 285acdcd7e913d4fb502fb656057f1fc81d6dfcd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967744"
---
# <span data-ttu-id="50237-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="50237-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="50237-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50237-102">SYNOPSIS</span></span>
<span data-ttu-id="50237-103">관리되는 애플리케이션 정의 제거</span><span class="sxs-lookup"><span data-stu-id="50237-103">Removes a managed application definition</span></span>

## <span data-ttu-id="50237-104">구문</span><span class="sxs-lookup"><span data-stu-id="50237-104">SYNTAX</span></span>

### <span data-ttu-id="50237-105">RemoveByNameAndResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="50237-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50237-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="50237-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50237-107">설명</span><span class="sxs-lookup"><span data-stu-id="50237-107">DESCRIPTION</span></span>
<span data-ttu-id="50237-108">**Remove-AzManagedApplicationDefinition** cmdlet은 관리되는 애플리케이션 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="50237-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="50237-109">예제</span><span class="sxs-lookup"><span data-stu-id="50237-109">EXAMPLES</span></span>

### <span data-ttu-id="50237-110">예제 1: 리소스 ID로 관리되는 애플리케이션 정의 제거</span><span class="sxs-lookup"><span data-stu-id="50237-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="50237-111">첫 번째 명령은 Get-AzManagedApplicationDefinition cmdlet을 사용하여 myAppDef라는 관리되는 애플리케이션 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="50237-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="50237-112">명령은 이 변수를 $ApplicationDefinition 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="50237-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="50237-113">두 번째 명령은 리소스의 **ResourceId** 속성에 의해 식별된 관리되는 애플리케이션 정의를 $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="50237-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="50237-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="50237-114">PARAMETERS</span></span>

### <span data-ttu-id="50237-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="50237-115">-ApiVersion</span></span>
<span data-ttu-id="50237-116">설정하면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="50237-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="50237-117">지정하지 않으면 API 버전이 사용 가능한 최신 버전으로 자동으로 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="50237-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50237-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50237-118">-DefaultProfile</span></span>
<span data-ttu-id="50237-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50237-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50237-120">-Force</span><span class="sxs-lookup"><span data-stu-id="50237-120">-Force</span></span>
<span data-ttu-id="50237-121">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50237-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="50237-122">-Id</span><span class="sxs-lookup"><span data-stu-id="50237-122">-Id</span></span>
<span data-ttu-id="50237-123">구독을 포함하여 완전히 자격을 갖춘 관리되는 애플리케이션 정의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="50237-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="50237-124">예: /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="50237-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50237-125">-Name</span><span class="sxs-lookup"><span data-stu-id="50237-125">-Name</span></span>
<span data-ttu-id="50237-126">관리되는 애플리케이션 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50237-126">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50237-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="50237-127">-Pre</span></span>
<span data-ttu-id="50237-128">설정하면 cmdlet이 사용할 버전을 자동으로 결정할 때 미리 릴리스 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="50237-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="50237-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50237-129">-ResourceGroupName</span></span>
<span data-ttu-id="50237-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50237-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50237-131">-확인</span><span class="sxs-lookup"><span data-stu-id="50237-131">-Confirm</span></span>
<span data-ttu-id="50237-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="50237-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50237-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50237-133">-WhatIf</span></span>
<span data-ttu-id="50237-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="50237-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50237-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50237-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50237-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50237-136">CommonParameters</span></span>
<span data-ttu-id="50237-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="50237-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50237-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50237-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50237-139">입력</span><span class="sxs-lookup"><span data-stu-id="50237-139">INPUTS</span></span>

### <span data-ttu-id="50237-140">System.String</span><span class="sxs-lookup"><span data-stu-id="50237-140">System.String</span></span>

## <span data-ttu-id="50237-141">출력</span><span class="sxs-lookup"><span data-stu-id="50237-141">OUTPUTS</span></span>

### <span data-ttu-id="50237-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="50237-142">System.Boolean</span></span>

## <span data-ttu-id="50237-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="50237-143">NOTES</span></span>

## <span data-ttu-id="50237-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50237-144">RELATED LINKS</span></span>
