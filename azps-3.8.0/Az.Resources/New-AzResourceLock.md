---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 8c4352f6345bc6de76208d6821aadd6c249174ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878113"
---
# <span data-ttu-id="eb2ae-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="eb2ae-101">New-AzResourceLock</span></span>

## <span data-ttu-id="eb2ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="eb2ae-103">리소스 잠금을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-103">Creates a resource lock.</span></span>

## <span data-ttu-id="eb2ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eb2ae-104">SYNTAX</span></span>

### <span data-ttu-id="eb2ae-105">BySpecifiedScope (기본값)</span><span class="sxs-lookup"><span data-stu-id="eb2ae-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb2ae-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eb2ae-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb2ae-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="eb2ae-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb2ae-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="eb2ae-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb2ae-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="eb2ae-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb2ae-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="eb2ae-110">ByTenantLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb2ae-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="eb2ae-111">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb2ae-112">설명은</span><span class="sxs-lookup"><span data-stu-id="eb2ae-112">DESCRIPTION</span></span>
<span data-ttu-id="eb2ae-113">**AzResourceLock** cmdlet은 리소스 잠금을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-113">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="eb2ae-114">예제의</span><span class="sxs-lookup"><span data-stu-id="eb2ae-114">EXAMPLES</span></span>

### <span data-ttu-id="eb2ae-115">예제 1: 웹 사이트에서 자원 잠금 만들기</span><span class="sxs-lookup"><span data-stu-id="eb2ae-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="eb2ae-116">이 명령은 웹 사이트에 리소스 잠금을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="eb2ae-117">변수</span><span class="sxs-lookup"><span data-stu-id="eb2ae-117">PARAMETERS</span></span>

### <span data-ttu-id="eb2ae-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="eb2ae-118">-ApiVersion</span></span>
<span data-ttu-id="eb2ae-119">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="eb2ae-120">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="eb2ae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb2ae-121">-DefaultProfile</span></span>
<span data-ttu-id="eb2ae-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="eb2ae-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb2ae-123">-Force</span><span class="sxs-lookup"><span data-stu-id="eb2ae-123">-Force</span></span>
<span data-ttu-id="eb2ae-124">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eb2ae-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="eb2ae-125">-LockId</span></span>
<span data-ttu-id="eb2ae-126">잠금의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-126">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="eb2ae-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="eb2ae-127">-LockLevel</span></span>
<span data-ttu-id="eb2ae-128">잠금의 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-128">Specifies the level for the lock.</span></span>
<span data-ttu-id="eb2ae-129">현재 유효한 값은 CanNotDelete, ReadOnly입니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-129">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="eb2ae-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="eb2ae-130">-LockName</span></span>
<span data-ttu-id="eb2ae-131">잠금의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-131">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="eb2ae-132">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="eb2ae-132">-LockNotes</span></span>
<span data-ttu-id="eb2ae-133">잠금에 대 한 메모를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-133">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="eb2ae-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="eb2ae-134">-Pre</span></span>
<span data-ttu-id="eb2ae-135">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="eb2ae-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb2ae-136">-ResourceGroupName</span></span>
<span data-ttu-id="eb2ae-137">잠금이 적용 되거나 잠금이 적용 되는 리소스 그룹을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-137">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="eb2ae-138">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="eb2ae-138">-ResourceName</span></span>
<span data-ttu-id="eb2ae-139">잠금이 적용 되는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-139">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="eb2ae-140">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="eb2ae-140">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="eb2ae-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="eb2ae-141">-ResourceType</span></span>
<span data-ttu-id="eb2ae-142">잠금이 적용 되는 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-142">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="eb2ae-143">-범위</span><span class="sxs-lookup"><span data-stu-id="eb2ae-143">-Scope</span></span>
<span data-ttu-id="eb2ae-144">잠금이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="eb2ae-145">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. `/subscriptions/` 구독 id `/resourceGroups/` 리소스 그룹 이름 `/providers/Microsoft.Sql/servers/` 서버 이름 `/databases/` 데이터베이스 이름 리소스 그룹을 지정 하려면 다음 형식을 사용 합니다. `/subscriptions/` 구독 ID `/resourceGroups/` 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="eb2ae-145">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="eb2ae-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="eb2ae-146">-TenantLevel</span></span>
<span data-ttu-id="eb2ae-147">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="eb2ae-148">-확인</span><span class="sxs-lookup"><span data-stu-id="eb2ae-148">-Confirm</span></span>
<span data-ttu-id="eb2ae-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb2ae-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb2ae-150">-WhatIf</span></span>
<span data-ttu-id="eb2ae-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb2ae-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb2ae-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb2ae-153">CommonParameters</span></span>
<span data-ttu-id="eb2ae-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb2ae-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eb2ae-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb2ae-156">입력</span><span class="sxs-lookup"><span data-stu-id="eb2ae-156">INPUTS</span></span>

### <span data-ttu-id="eb2ae-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eb2ae-157">System.String</span></span>

### <span data-ttu-id="eb2ae-158">Microsoft. Azure.. m a. 잠금. LockLevel</span><span class="sxs-lookup"><span data-stu-id="eb2ae-158">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="eb2ae-159">출력</span><span class="sxs-lookup"><span data-stu-id="eb2ae-159">OUTPUTS</span></span>

### <span data-ttu-id="eb2ae-160">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="eb2ae-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="eb2ae-161">상속자</span><span class="sxs-lookup"><span data-stu-id="eb2ae-161">NOTES</span></span>

## <span data-ttu-id="eb2ae-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb2ae-162">RELATED LINKS</span></span>

[<span data-ttu-id="eb2ae-163">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="eb2ae-163">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="eb2ae-164">제거-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="eb2ae-164">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="eb2ae-165">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="eb2ae-165">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


