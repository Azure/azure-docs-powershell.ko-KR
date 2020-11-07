---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
ms.openlocfilehash: 73d82366cc0120e057d0c083e7f6da0b3cdebb76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703623"
---
# <span data-ttu-id="c25f3-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="c25f3-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="c25f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c25f3-102">SYNOPSIS</span></span>
<span data-ttu-id="c25f3-103">리소스 잠금을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c25f3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c25f3-104">SYNTAX</span></span>

### <span data-ttu-id="c25f3-105">지정 된 범위에 있는 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-105">A lock at the specified scope.</span></span> <span data-ttu-id="c25f3-106">기본값</span><span class="sxs-lookup"><span data-stu-id="c25f3-106">(Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c25f3-107">리소스 그룹 범위에서 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-107">A lock at the resource group scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c25f3-108">리소스 그룹 리소스 범위에서 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-108">A lock at the resource group resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c25f3-109">구독 범위에서 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-109">A lock at the subscription scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c25f3-110">구독 리소스 범위에서 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-110">A lock at the subscription resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c25f3-111">테 넌 트 리소스 범위에서 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-111">A lock at the tenant resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c25f3-112">잠금 (Id 기준)</span><span class="sxs-lookup"><span data-stu-id="c25f3-112">A lock, by Id.</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c25f3-113">설명은</span><span class="sxs-lookup"><span data-stu-id="c25f3-113">DESCRIPTION</span></span>
<span data-ttu-id="c25f3-114">**Set-AzureRmResourceLock** cmdlet은 리소스 잠금을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-114">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="c25f3-115">예제의</span><span class="sxs-lookup"><span data-stu-id="c25f3-115">EXAMPLES</span></span>

### <span data-ttu-id="c25f3-116">예제 1: 잠금에 대 한 노트 업데이트</span><span class="sxs-lookup"><span data-stu-id="c25f3-116">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c25f3-117">이 명령은 ContosoSiteLock 이라는 잠금에 대 한 메모를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-117">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="c25f3-118">변수</span><span class="sxs-lookup"><span data-stu-id="c25f3-118">PARAMETERS</span></span>

### <span data-ttu-id="c25f3-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c25f3-119">-ApiVersion</span></span>
<span data-ttu-id="c25f3-120">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c25f3-121">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c25f3-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c25f3-122">-Force</span></span>
<span data-ttu-id="c25f3-123">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c25f3-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c25f3-124">-InformationAction</span></span>
<span data-ttu-id="c25f3-125">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c25f3-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c25f3-127">하기로</span><span class="sxs-lookup"><span data-stu-id="c25f3-127">Continue</span></span>
- <span data-ttu-id="c25f3-128">숨기기</span><span class="sxs-lookup"><span data-stu-id="c25f3-128">Ignore</span></span>
- <span data-ttu-id="c25f3-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="c25f3-129">Inquire</span></span>
- <span data-ttu-id="c25f3-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c25f3-130">SilentlyContinue</span></span>
- <span data-ttu-id="c25f3-131">중지가</span><span class="sxs-lookup"><span data-stu-id="c25f3-131">Stop</span></span>
- <span data-ttu-id="c25f3-132">대기</span><span class="sxs-lookup"><span data-stu-id="c25f3-132">Suspend</span></span>

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

### <span data-ttu-id="c25f3-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c25f3-133">-InformationVariable</span></span>
<span data-ttu-id="c25f3-134">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c25f3-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="c25f3-135">-LockId</span></span>
<span data-ttu-id="c25f3-136">이 cmdlet이 수정 하는 잠금의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-136">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c25f3-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="c25f3-137">-LockLevel</span></span>
<span data-ttu-id="c25f3-138">잠금의 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="c25f3-139">현재 유효한 값은 CanNotDelete입니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="c25f3-140">-LockName</span><span class="sxs-lookup"><span data-stu-id="c25f3-140">-LockName</span></span>
<span data-ttu-id="c25f3-141">이 cmdlet이 수정 하는 잠금의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-141">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope., A lock at the resource group scope., A lock at the resource group resource scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c25f3-142">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="c25f3-142">-LockNotes</span></span>
<span data-ttu-id="c25f3-143">잠금에 대 한 메모를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="c25f3-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="c25f3-144">-Pre</span></span>
<span data-ttu-id="c25f3-145">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c25f3-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c25f3-146">-ResourceGroupName</span></span>
<span data-ttu-id="c25f3-147">잠금이 적용 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-147">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c25f3-148">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="c25f3-148">-ResourceName</span></span>
<span data-ttu-id="c25f3-149">잠금이 적용 되는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="c25f3-150">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-150">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="c25f3-151">서버 `/` 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="c25f3-151">Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c25f3-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c25f3-152">-ResourceType</span></span>
<span data-ttu-id="c25f3-153">잠금이 적용 되는 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-153">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c25f3-154">-범위</span><span class="sxs-lookup"><span data-stu-id="c25f3-154">-Scope</span></span>
<span data-ttu-id="c25f3-155">잠금이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="c25f3-156">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-156">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="c25f3-157">`/subscriptions/`구독 ID `/resourceGroups/` 리소스 그룹 이름 `/providers/Microsoft.Sql/servers/` 서버 이름 `/databases/` 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="c25f3-157">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="c25f3-158">리소스 그룹을 지정 하려면 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-158">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="c25f3-159">`/subscriptions/`구독 ID `/resourceGroups/` 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c25f3-159">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c25f3-160">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="c25f3-160">-TenantLevel</span></span>
<span data-ttu-id="c25f3-161">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-161">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c25f3-162">-확인</span><span class="sxs-lookup"><span data-stu-id="c25f3-162">-Confirm</span></span>
<span data-ttu-id="c25f3-163">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c25f3-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c25f3-164">-WhatIf</span></span>
<span data-ttu-id="c25f3-165">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c25f3-166">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c25f3-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c25f3-167">-DefaultProfile</span></span>
<span data-ttu-id="c25f3-168">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c25f3-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25f3-169">CommonParameters</span></span>
<span data-ttu-id="c25f3-170">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25f3-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25f3-171">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c25f3-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25f3-172">입력</span><span class="sxs-lookup"><span data-stu-id="c25f3-172">INPUTS</span></span>

## <span data-ttu-id="c25f3-173">출력</span><span class="sxs-lookup"><span data-stu-id="c25f3-173">OUTPUTS</span></span>

### <span data-ttu-id="c25f3-174">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="c25f3-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c25f3-175">상속자</span><span class="sxs-lookup"><span data-stu-id="c25f3-175">NOTES</span></span>

## <span data-ttu-id="c25f3-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c25f3-176">RELATED LINKS</span></span>

[<span data-ttu-id="c25f3-177">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="c25f3-177">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="c25f3-178">새로운 AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="c25f3-178">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="c25f3-179">제거-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="c25f3-179">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


