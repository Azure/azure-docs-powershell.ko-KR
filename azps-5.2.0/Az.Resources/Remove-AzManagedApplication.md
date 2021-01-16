---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 17a28da26aa26860b7fd4a28ec922932bb089da3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355562"
---
# <span data-ttu-id="83d9f-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="83d9f-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="83d9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="83d9f-103">관리되는 애플리케이션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="83d9f-103">Removes a managed application</span></span>

## <span data-ttu-id="83d9f-104">구문</span><span class="sxs-lookup"><span data-stu-id="83d9f-104">SYNTAX</span></span>

### <span data-ttu-id="83d9f-105">RemoveByNameAndResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="83d9f-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83d9f-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="83d9f-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83d9f-107">설명</span><span class="sxs-lookup"><span data-stu-id="83d9f-107">DESCRIPTION</span></span>
<span data-ttu-id="83d9f-108">**Remove-AzManagedApplication** cmdlet은 관리되는 애플리케이션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="83d9f-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="83d9f-109">예제</span><span class="sxs-lookup"><span data-stu-id="83d9f-109">EXAMPLES</span></span>

### <span data-ttu-id="83d9f-110">예제 1: 리소스 ID로 관리되는 애플리케이션 제거</span><span class="sxs-lookup"><span data-stu-id="83d9f-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="83d9f-111">첫 번째 명령은 Get-AzManagedApplication cmdlet을 사용하여 myApp이라는 관리되는 애플리케이션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83d9f-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="83d9f-112">이 명령은 $Application 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="83d9f-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="83d9f-113">두 번째 명령은 리소스의 **ResourceId** 속성으로 식별된 관리되는 애플리케이션을 $Application.</span><span class="sxs-lookup"><span data-stu-id="83d9f-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="83d9f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83d9f-114">PARAMETERS</span></span>

### <span data-ttu-id="83d9f-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="83d9f-115">-ApiVersion</span></span>
<span data-ttu-id="83d9f-116">설정되면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="83d9f-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="83d9f-117">지정하지 않으면 API 버전이 사용 가능한 최신 버전으로 자동으로 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="83d9f-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="83d9f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d9f-118">-DefaultProfile</span></span>
<span data-ttu-id="83d9f-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83d9f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83d9f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="83d9f-120">-Force</span></span>
<span data-ttu-id="83d9f-121">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83d9f-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="83d9f-122">-Id</span><span class="sxs-lookup"><span data-stu-id="83d9f-122">-Id</span></span>
<span data-ttu-id="83d9f-123">구독을 포함하여 정식으로 관리되는 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="83d9f-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="83d9f-124">예: /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="83d9f-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="83d9f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="83d9f-125">-Name</span></span>
<span data-ttu-id="83d9f-126">관리되는 애플리케이션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83d9f-126">The managed application name.</span></span>

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

### <span data-ttu-id="83d9f-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="83d9f-127">-Pre</span></span>
<span data-ttu-id="83d9f-128">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="83d9f-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="83d9f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83d9f-129">-ResourceGroupName</span></span>
<span data-ttu-id="83d9f-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83d9f-130">The resource group name.</span></span>

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

### <span data-ttu-id="83d9f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83d9f-131">-Confirm</span></span>
<span data-ttu-id="83d9f-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="83d9f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83d9f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83d9f-133">-WhatIf</span></span>
<span data-ttu-id="83d9f-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="83d9f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83d9f-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83d9f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83d9f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d9f-136">CommonParameters</span></span>
<span data-ttu-id="83d9f-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="83d9f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d9f-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="83d9f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d9f-139">입력</span><span class="sxs-lookup"><span data-stu-id="83d9f-139">INPUTS</span></span>

### <span data-ttu-id="83d9f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="83d9f-140">System.String</span></span>

## <span data-ttu-id="83d9f-141">출력</span><span class="sxs-lookup"><span data-stu-id="83d9f-141">OUTPUTS</span></span>

### <span data-ttu-id="83d9f-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="83d9f-142">System.Boolean</span></span>

## <span data-ttu-id="83d9f-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="83d9f-143">NOTES</span></span>

## <span data-ttu-id="83d9f-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83d9f-144">RELATED LINKS</span></span>
