---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: c532633de593294c6b5dbe0e09b9615a1d5355a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495416"
---
# <span data-ttu-id="f10c5-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f10c5-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="f10c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f10c5-102">SYNOPSIS</span></span>
<span data-ttu-id="f10c5-103">리소스 잠금을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="f10c5-104">구문</span><span class="sxs-lookup"><span data-stu-id="f10c5-104">SYNTAX</span></span>

### <span data-ttu-id="f10c5-105">BySpecifiedScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="f10c5-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f10c5-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f10c5-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f10c5-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="f10c5-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f10c5-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="f10c5-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f10c5-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="f10c5-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f10c5-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="f10c5-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f10c5-111">설명</span><span class="sxs-lookup"><span data-stu-id="f10c5-111">DESCRIPTION</span></span>
<span data-ttu-id="f10c5-112">**Set-AzResourceLock** cmdlet은 리소스 잠금을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="f10c5-113">예제</span><span class="sxs-lookup"><span data-stu-id="f10c5-113">EXAMPLES</span></span>

### <span data-ttu-id="f10c5-114">예제 1: 잠금에 대한 노트 업데이트</span><span class="sxs-lookup"><span data-stu-id="f10c5-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f10c5-115">이 명령은 ContosoSiteLock이라는 잠금에 대한 메모를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="f10c5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f10c5-116">PARAMETERS</span></span>

### <span data-ttu-id="f10c5-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f10c5-117">-ApiVersion</span></span>
<span data-ttu-id="f10c5-118">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f10c5-119">버전을 지정하지 않으면 이 cmdlet은 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f10c5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f10c5-120">-DefaultProfile</span></span>
<span data-ttu-id="f10c5-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f10c5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f10c5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f10c5-122">-Force</span></span>
<span data-ttu-id="f10c5-123">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f10c5-124">-LockId</span><span class="sxs-lookup"><span data-stu-id="f10c5-124">-LockId</span></span>
<span data-ttu-id="f10c5-125">이 cmdlet이 수정하는 잠금의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10c5-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="f10c5-126">-LockLevel</span></span>
<span data-ttu-id="f10c5-127">잠금 수준을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="f10c5-128">현재 유효한 값은 CanNotDelete뿐입니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-128">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10c5-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="f10c5-129">-LockName</span></span>
<span data-ttu-id="f10c5-130">이 cmdlet이 수정하는 잠금의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10c5-131">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="f10c5-131">-LockNotes</span></span>
<span data-ttu-id="f10c5-132">잠금에 대한 노트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-132">Specifies the notes for the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10c5-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="f10c5-133">-Pre</span></span>
<span data-ttu-id="f10c5-134">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f10c5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f10c5-135">-ResourceGroupName</span></span>
<span data-ttu-id="f10c5-136">잠금이 적용되는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-136">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10c5-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f10c5-137">-ResourceName</span></span>
<span data-ttu-id="f10c5-138">잠금이 적용되는 리소스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="f10c5-139">예를 들어 데이터베이스를 지정하려면 서버 데이터베이스 형식을 `/` 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10c5-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f10c5-140">-ResourceType</span></span>
<span data-ttu-id="f10c5-141">잠금이 적용되는 리소스 종류를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-141">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10c5-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="f10c5-142">-Scope</span></span>
<span data-ttu-id="f10c5-143">잠금이 적용되는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="f10c5-144">예를 들어 데이터베이스를 지정하려면 다음 형식을 사용합니다. 구독 ID 리소스 그룹 이름 서버 이름 데이터베이스 이름 리소스 그룹을 지정하려면 다음 형식을 사용합니다. 구독 ID 리소스 그룹 `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` `/databases/` `/subscriptions/` `/resourceGroups/` 이름</span><span class="sxs-lookup"><span data-stu-id="f10c5-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10c5-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f10c5-145">-Confirm</span></span>
<span data-ttu-id="f10c5-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f10c5-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f10c5-147">-WhatIf</span></span>
<span data-ttu-id="f10c5-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f10c5-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f10c5-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f10c5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f10c5-150">CommonParameters</span></span>
<span data-ttu-id="f10c5-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f10c5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f10c5-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f10c5-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f10c5-153">입력</span><span class="sxs-lookup"><span data-stu-id="f10c5-153">INPUTS</span></span>

### <span data-ttu-id="f10c5-154">System.String</span><span class="sxs-lookup"><span data-stu-id="f10c5-154">System.String</span></span>

### <span data-ttu-id="f10c5-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span><span class="sxs-lookup"><span data-stu-id="f10c5-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="f10c5-156">출력</span><span class="sxs-lookup"><span data-stu-id="f10c5-156">OUTPUTS</span></span>

### <span data-ttu-id="f10c5-157">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f10c5-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f10c5-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f10c5-158">NOTES</span></span>

## <span data-ttu-id="f10c5-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f10c5-159">RELATED LINKS</span></span>

[<span data-ttu-id="f10c5-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f10c5-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="f10c5-161">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f10c5-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="f10c5-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f10c5-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


