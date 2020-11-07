---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: ccb491742d9a66a7e6eb300d7e75be0dcfac687e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880309"
---
# <span data-ttu-id="3fab2-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="3fab2-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="3fab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fab2-102">SYNOPSIS</span></span>
<span data-ttu-id="3fab2-103">리소스 잠금을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fab2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3fab2-104">SYNTAX</span></span>

### <span data-ttu-id="3fab2-105">BySpecifiedScope (기본값)</span><span class="sxs-lookup"><span data-stu-id="3fab2-105">BySpecifiedScope (Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3fab2-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3fab2-106">ByResourceGroup</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3fab2-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="3fab2-107">ByResourceGroupLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fab2-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="3fab2-108">BySubscription</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3fab2-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="3fab2-109">BySubscriptionLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fab2-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="3fab2-110">ByTenantLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fab2-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="3fab2-111">ByLockId</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3fab2-112">설명은</span><span class="sxs-lookup"><span data-stu-id="3fab2-112">DESCRIPTION</span></span>
<span data-ttu-id="3fab2-113">**Set-AzureRmResourceLock** cmdlet은 리소스 잠금을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-113">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="3fab2-114">예제의</span><span class="sxs-lookup"><span data-stu-id="3fab2-114">EXAMPLES</span></span>

### <span data-ttu-id="3fab2-115">예제 1: 잠금에 대 한 노트 업데이트</span><span class="sxs-lookup"><span data-stu-id="3fab2-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="3fab2-116">이 명령은 ContosoSiteLock 이라는 잠금에 대 한 메모를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="3fab2-117">변수</span><span class="sxs-lookup"><span data-stu-id="3fab2-117">PARAMETERS</span></span>

### <span data-ttu-id="3fab2-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3fab2-118">-ApiVersion</span></span>
<span data-ttu-id="3fab2-119">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3fab2-120">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3fab2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fab2-121">-DefaultProfile</span></span>
<span data-ttu-id="3fab2-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3fab2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fab2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="3fab2-123">-Force</span></span>
<span data-ttu-id="3fab2-124">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3fab2-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3fab2-125">-InformationAction</span></span>
<span data-ttu-id="3fab2-126">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="3fab2-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3fab2-128">하기로</span><span class="sxs-lookup"><span data-stu-id="3fab2-128">Continue</span></span>
- <span data-ttu-id="3fab2-129">숨기기</span><span class="sxs-lookup"><span data-stu-id="3fab2-129">Ignore</span></span>
- <span data-ttu-id="3fab2-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="3fab2-130">Inquire</span></span>
- <span data-ttu-id="3fab2-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3fab2-131">SilentlyContinue</span></span>
- <span data-ttu-id="3fab2-132">중지가</span><span class="sxs-lookup"><span data-stu-id="3fab2-132">Stop</span></span>
- <span data-ttu-id="3fab2-133">대기</span><span class="sxs-lookup"><span data-stu-id="3fab2-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fab2-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3fab2-134">-InformationVariable</span></span>
<span data-ttu-id="3fab2-135">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fab2-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="3fab2-136">-LockId</span></span>
<span data-ttu-id="3fab2-137">이 cmdlet이 수정 하는 잠금의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-137">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3fab2-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="3fab2-138">-LockLevel</span></span>
<span data-ttu-id="3fab2-139">잠금의 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="3fab2-140">현재 유효한 값은 CanNotDelete입니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-140">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fab2-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="3fab2-141">-LockName</span></span>
<span data-ttu-id="3fab2-142">이 cmdlet이 수정 하는 잠금의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-142">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3fab2-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="3fab2-143">-LockNotes</span></span>
<span data-ttu-id="3fab2-144">잠금에 대 한 메모를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="3fab2-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="3fab2-145">-Pre</span></span>
<span data-ttu-id="3fab2-146">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3fab2-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fab2-147">-ResourceGroupName</span></span>
<span data-ttu-id="3fab2-148">잠금이 적용 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-148">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="3fab2-149">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="3fab2-149">-ResourceName</span></span>
<span data-ttu-id="3fab2-150">잠금이 적용 되는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="3fab2-151">예를 들어 데이터베이스를 지정 하려면 서버 데이터베이스 형식으로 다음을 사용 합니다. `/`</span><span class="sxs-lookup"><span data-stu-id="3fab2-151">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="3fab2-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3fab2-152">-ResourceType</span></span>
<span data-ttu-id="3fab2-153">잠금이 적용 되는 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-153">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="3fab2-154">-범위</span><span class="sxs-lookup"><span data-stu-id="3fab2-154">-Scope</span></span>
<span data-ttu-id="3fab2-155">잠금이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="3fab2-156">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. `/subscriptions/` 구독 id `/resourceGroups/` 리소스 그룹 이름 `/providers/Microsoft.Sql/servers/` 서버 이름 `/databases/` 데이터베이스 이름 리소스 그룹을 지정 하려면 다음 형식을 사용 합니다. `/subscriptions/` 구독 ID `/resourceGroups/` 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3fab2-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="3fab2-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="3fab2-157">-TenantLevel</span></span>
<span data-ttu-id="3fab2-158">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="3fab2-159">-확인</span><span class="sxs-lookup"><span data-stu-id="3fab2-159">-Confirm</span></span>
<span data-ttu-id="3fab2-160">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fab2-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fab2-161">-WhatIf</span></span>
<span data-ttu-id="3fab2-162">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fab2-163">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fab2-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fab2-164">CommonParameters</span></span>
<span data-ttu-id="3fab2-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fab2-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fab2-166">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fab2-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fab2-167">입력</span><span class="sxs-lookup"><span data-stu-id="3fab2-167">INPUTS</span></span>

## <span data-ttu-id="3fab2-168">출력</span><span class="sxs-lookup"><span data-stu-id="3fab2-168">OUTPUTS</span></span>

## <span data-ttu-id="3fab2-169">상속자</span><span class="sxs-lookup"><span data-stu-id="3fab2-169">NOTES</span></span>

## <span data-ttu-id="3fab2-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3fab2-170">RELATED LINKS</span></span>

[<span data-ttu-id="3fab2-171">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="3fab2-171">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="3fab2-172">새로운 AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="3fab2-172">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="3fab2-173">제거-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="3fab2-173">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


