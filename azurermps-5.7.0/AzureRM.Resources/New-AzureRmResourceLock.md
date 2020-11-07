---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
ms.openlocfilehash: 0b3498ba3107e2312b596143820036286b925b6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702360"
---
# <span data-ttu-id="34b94-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="34b94-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="34b94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34b94-102">SYNOPSIS</span></span>
<span data-ttu-id="34b94-103">리소스 잠금을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34b94-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34b94-104">SYNTAX</span></span>

### <span data-ttu-id="34b94-105">BySpecifiedScope (기본값)</span><span class="sxs-lookup"><span data-stu-id="34b94-105">BySpecifiedScope (Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34b94-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="34b94-106">ByResourceGroup</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34b94-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="34b94-107">ByResourceGroupLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34b94-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="34b94-108">BySubscription</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34b94-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="34b94-109">BySubscriptionLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34b94-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="34b94-110">ByTenantLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34b94-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="34b94-111">ByLockId</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34b94-112">설명은</span><span class="sxs-lookup"><span data-stu-id="34b94-112">DESCRIPTION</span></span>
<span data-ttu-id="34b94-113">**AzureRmResourceLock** cmdlet은 리소스 잠금을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-113">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="34b94-114">예제의</span><span class="sxs-lookup"><span data-stu-id="34b94-114">EXAMPLES</span></span>

### <span data-ttu-id="34b94-115">예제 1: 웹 사이트에서 자원 잠금 만들기</span><span class="sxs-lookup"><span data-stu-id="34b94-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="34b94-116">이 명령은 웹 사이트에 리소스 잠금을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="34b94-117">변수</span><span class="sxs-lookup"><span data-stu-id="34b94-117">PARAMETERS</span></span>

### <span data-ttu-id="34b94-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="34b94-118">-ApiVersion</span></span>
<span data-ttu-id="34b94-119">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="34b94-120">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b94-121">-DefaultProfile</span></span>
<span data-ttu-id="34b94-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="34b94-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-123">-Force</span><span class="sxs-lookup"><span data-stu-id="34b94-123">-Force</span></span>
<span data-ttu-id="34b94-124">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="34b94-125">-InformationAction</span></span>
<span data-ttu-id="34b94-126">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="34b94-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="34b94-128">하기로</span><span class="sxs-lookup"><span data-stu-id="34b94-128">Continue</span></span>
- <span data-ttu-id="34b94-129">숨기기</span><span class="sxs-lookup"><span data-stu-id="34b94-129">Ignore</span></span>
- <span data-ttu-id="34b94-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="34b94-130">Inquire</span></span>
- <span data-ttu-id="34b94-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="34b94-131">SilentlyContinue</span></span>
- <span data-ttu-id="34b94-132">중지가</span><span class="sxs-lookup"><span data-stu-id="34b94-132">Stop</span></span>
- <span data-ttu-id="34b94-133">대기</span><span class="sxs-lookup"><span data-stu-id="34b94-133">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="34b94-134">-InformationVariable</span></span>
<span data-ttu-id="34b94-135">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-135">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="34b94-136">-LockId</span></span>
<span data-ttu-id="34b94-137">잠금의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-137">Specifies the ID of the lock.</span></span>

```yaml
Type: String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="34b94-138">-LockLevel</span></span>
<span data-ttu-id="34b94-139">잠금의 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="34b94-140">현재 유효한 값은 CanNotDelete, ReadOnly입니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-140">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

```yaml
Type: LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="34b94-141">-LockName</span></span>
<span data-ttu-id="34b94-142">잠금의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-142">Specifies the name of the lock.</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="34b94-143">-LockNotes</span></span>
<span data-ttu-id="34b94-144">잠금에 대 한 메모를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-144">Specifies the notes for the lock.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="34b94-145">-Pre</span></span>
<span data-ttu-id="34b94-146">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34b94-147">-ResourceGroupName</span></span>
<span data-ttu-id="34b94-148">잠금이 적용 되거나 잠금이 적용 되는 리소스 그룹을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-148">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-149">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="34b94-149">-ResourceName</span></span>
<span data-ttu-id="34b94-150">잠금이 적용 되는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="34b94-151">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-151">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="34b94-152">-ResourceType</span></span>
<span data-ttu-id="34b94-153">잠금이 적용 되는 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-153">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-154">-범위</span><span class="sxs-lookup"><span data-stu-id="34b94-154">-Scope</span></span>
<span data-ttu-id="34b94-155">잠금이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="34b94-156">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-156">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="34b94-157">`/subscriptions/`구독 ID `/resourceGroups/` 리소스 그룹 이름 `/providers/Microsoft.Sql/servers/` 서버 이름 `/databases/` 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="34b94-157">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="34b94-158">리소스 그룹을 지정 하려면 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-158">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="34b94-159">`/subscriptions/`구독 ID `/resourceGroups/` 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="34b94-159">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-160">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="34b94-160">-TenantLevel</span></span>
<span data-ttu-id="34b94-161">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-161">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-162">-확인</span><span class="sxs-lookup"><span data-stu-id="34b94-162">-Confirm</span></span>
<span data-ttu-id="34b94-163">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-163">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34b94-164">-WhatIf</span></span>
<span data-ttu-id="34b94-165">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34b94-166">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-166">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34b94-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b94-167">CommonParameters</span></span>
<span data-ttu-id="34b94-168">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b94-169">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34b94-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b94-170">입력</span><span class="sxs-lookup"><span data-stu-id="34b94-170">INPUTS</span></span>

### <span data-ttu-id="34b94-171">않아야</span><span class="sxs-lookup"><span data-stu-id="34b94-171">None</span></span>
<span data-ttu-id="34b94-172">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34b94-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="34b94-173">출력</span><span class="sxs-lookup"><span data-stu-id="34b94-173">OUTPUTS</span></span>

### <span data-ttu-id="34b94-174">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="34b94-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="34b94-175">상속자</span><span class="sxs-lookup"><span data-stu-id="34b94-175">NOTES</span></span>

## <span data-ttu-id="34b94-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34b94-176">RELATED LINKS</span></span>

[<span data-ttu-id="34b94-177">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="34b94-177">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="34b94-178">제거-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="34b94-178">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="34b94-179">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="34b94-179">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


