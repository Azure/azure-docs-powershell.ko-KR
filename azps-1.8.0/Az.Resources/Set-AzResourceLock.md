---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: f1220db034a2cdcc81ffbd7a146fee8e2c7201be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699307"
---
# <span data-ttu-id="177b3-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="177b3-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="177b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="177b3-102">SYNOPSIS</span></span>
<span data-ttu-id="177b3-103">리소스 잠금을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="177b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="177b3-104">SYNTAX</span></span>

### <span data-ttu-id="177b3-105">BySpecifiedScope (기본값)</span><span class="sxs-lookup"><span data-stu-id="177b3-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="177b3-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="177b3-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="177b3-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="177b3-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="177b3-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="177b3-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="177b3-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="177b3-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="177b3-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="177b3-110">ByTenantLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="177b3-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="177b3-111">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="177b3-112">설명은</span><span class="sxs-lookup"><span data-stu-id="177b3-112">DESCRIPTION</span></span>
<span data-ttu-id="177b3-113">**Set-AzResourceLock** cmdlet은 리소스 잠금을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-113">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="177b3-114">예제의</span><span class="sxs-lookup"><span data-stu-id="177b3-114">EXAMPLES</span></span>

### <span data-ttu-id="177b3-115">예제 1: 잠금에 대 한 노트 업데이트</span><span class="sxs-lookup"><span data-stu-id="177b3-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="177b3-116">이 명령은 ContosoSiteLock 이라는 잠금에 대 한 메모를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="177b3-117">변수</span><span class="sxs-lookup"><span data-stu-id="177b3-117">PARAMETERS</span></span>

### <span data-ttu-id="177b3-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="177b3-118">-ApiVersion</span></span>
<span data-ttu-id="177b3-119">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="177b3-120">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="177b3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="177b3-121">-DefaultProfile</span></span>
<span data-ttu-id="177b3-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="177b3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="177b3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="177b3-123">-Force</span></span>
<span data-ttu-id="177b3-124">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="177b3-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="177b3-125">-LockId</span></span>
<span data-ttu-id="177b3-126">이 cmdlet이 수정 하는 잠금의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-126">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="177b3-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="177b3-127">-LockLevel</span></span>
<span data-ttu-id="177b3-128">잠금의 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-128">Specifies the level for the lock.</span></span>
<span data-ttu-id="177b3-129">현재 유효한 값은 CanNotDelete입니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-129">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="177b3-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="177b3-130">-LockName</span></span>
<span data-ttu-id="177b3-131">이 cmdlet이 수정 하는 잠금의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-131">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="177b3-132">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="177b3-132">-LockNotes</span></span>
<span data-ttu-id="177b3-133">잠금에 대 한 메모를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-133">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="177b3-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="177b3-134">-Pre</span></span>
<span data-ttu-id="177b3-135">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="177b3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="177b3-136">-ResourceGroupName</span></span>
<span data-ttu-id="177b3-137">잠금이 적용 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-137">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="177b3-138">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="177b3-138">-ResourceName</span></span>
<span data-ttu-id="177b3-139">잠금이 적용 되는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-139">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="177b3-140">예를 들어 데이터베이스를 지정 하려면 서버 데이터베이스 형식으로 다음을 사용 합니다. `/`</span><span class="sxs-lookup"><span data-stu-id="177b3-140">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="177b3-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="177b3-141">-ResourceType</span></span>
<span data-ttu-id="177b3-142">잠금이 적용 되는 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-142">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="177b3-143">-범위</span><span class="sxs-lookup"><span data-stu-id="177b3-143">-Scope</span></span>
<span data-ttu-id="177b3-144">잠금이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="177b3-145">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. `/subscriptions/` 구독 id `/resourceGroups/` 리소스 그룹 이름 `/providers/Microsoft.Sql/servers/` 서버 이름 `/databases/` 데이터베이스 이름 리소스 그룹을 지정 하려면 다음 형식을 사용 합니다. `/subscriptions/` 구독 ID `/resourceGroups/` 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="177b3-145">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="177b3-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="177b3-146">-TenantLevel</span></span>
<span data-ttu-id="177b3-147">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-147">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="177b3-148">-확인</span><span class="sxs-lookup"><span data-stu-id="177b3-148">-Confirm</span></span>
<span data-ttu-id="177b3-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="177b3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="177b3-150">-WhatIf</span></span>
<span data-ttu-id="177b3-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="177b3-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="177b3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="177b3-153">CommonParameters</span></span>
<span data-ttu-id="177b3-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="177b3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="177b3-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="177b3-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="177b3-156">입력</span><span class="sxs-lookup"><span data-stu-id="177b3-156">INPUTS</span></span>

### <span data-ttu-id="177b3-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="177b3-157">System.String</span></span>

### <span data-ttu-id="177b3-158">Microsoft. Azure.. m a. 잠금. LockLevel</span><span class="sxs-lookup"><span data-stu-id="177b3-158">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="177b3-159">출력</span><span class="sxs-lookup"><span data-stu-id="177b3-159">OUTPUTS</span></span>

### <span data-ttu-id="177b3-160">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="177b3-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="177b3-161">상속자</span><span class="sxs-lookup"><span data-stu-id="177b3-161">NOTES</span></span>

## <span data-ttu-id="177b3-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="177b3-162">RELATED LINKS</span></span>

[<span data-ttu-id="177b3-163">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="177b3-163">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="177b3-164">새로운 AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="177b3-164">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="177b3-165">제거-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="177b3-165">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


