---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: c719eee4800b404d691d478a989fdfdb3e7be09d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535643"
---
# <span data-ttu-id="37abb-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="37abb-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="37abb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37abb-102">SYNOPSIS</span></span>
<span data-ttu-id="37abb-103">리소스 잠금을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37abb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="37abb-104">SYNTAX</span></span>

### <span data-ttu-id="37abb-105">ByLockId (기본값)</span><span class="sxs-lookup"><span data-stu-id="37abb-105">ByLockId (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37abb-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="37abb-106">ByResourceGroup</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37abb-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="37abb-107">ByResourceGroupLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37abb-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="37abb-108">BySpecifiedScope</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37abb-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="37abb-109">BySubscription</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37abb-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="37abb-110">BySubscriptionLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37abb-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="37abb-111">ByTenantLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37abb-112">설명은</span><span class="sxs-lookup"><span data-stu-id="37abb-112">DESCRIPTION</span></span>
<span data-ttu-id="37abb-113">**AzureRmResourceLock** Cmdlet은 Azure 리소스 잠금을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="37abb-114">예제의</span><span class="sxs-lookup"><span data-stu-id="37abb-114">EXAMPLES</span></span>

### <span data-ttu-id="37abb-115">예제 1: 잠금 제거</span><span class="sxs-lookup"><span data-stu-id="37abb-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="37abb-116">이 명령은 ContosoSiteLock 라는 잠금을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="37abb-117">변수</span><span class="sxs-lookup"><span data-stu-id="37abb-117">PARAMETERS</span></span>

### <span data-ttu-id="37abb-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="37abb-118">-ApiVersion</span></span>
<span data-ttu-id="37abb-119">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="37abb-120">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="37abb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37abb-121">-DefaultProfile</span></span>
<span data-ttu-id="37abb-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="37abb-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37abb-123">-Force</span><span class="sxs-lookup"><span data-stu-id="37abb-123">-Force</span></span>
<span data-ttu-id="37abb-124">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="37abb-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="37abb-125">-InformationAction</span></span>
<span data-ttu-id="37abb-126">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="37abb-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37abb-128">하기로</span><span class="sxs-lookup"><span data-stu-id="37abb-128">Continue</span></span>
- <span data-ttu-id="37abb-129">숨기기</span><span class="sxs-lookup"><span data-stu-id="37abb-129">Ignore</span></span>
- <span data-ttu-id="37abb-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="37abb-130">Inquire</span></span>
- <span data-ttu-id="37abb-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="37abb-131">SilentlyContinue</span></span>
- <span data-ttu-id="37abb-132">중지가</span><span class="sxs-lookup"><span data-stu-id="37abb-132">Stop</span></span>
- <span data-ttu-id="37abb-133">대기</span><span class="sxs-lookup"><span data-stu-id="37abb-133">Suspend</span></span>

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

### <span data-ttu-id="37abb-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="37abb-134">-InformationVariable</span></span>
<span data-ttu-id="37abb-135">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="37abb-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="37abb-136">-LockId</span></span>
<span data-ttu-id="37abb-137">이 cmdlet이 제거 하는 잠금의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="37abb-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="37abb-138">-LockName</span></span>
<span data-ttu-id="37abb-139">이 cmdlet이 제거 하는 잠금의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-139">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37abb-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="37abb-140">-Pre</span></span>
<span data-ttu-id="37abb-141">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="37abb-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37abb-142">-ResourceGroupName</span></span>
<span data-ttu-id="37abb-143">잠금이 적용 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-143">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="37abb-144">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="37abb-144">-ResourceName</span></span>
<span data-ttu-id="37abb-145">잠금이 적용 되는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="37abb-146">예를 들어 데이터베이스를 지정 하려면 서버 데이터베이스 형식으로 다음을 사용 합니다. `/`</span><span class="sxs-lookup"><span data-stu-id="37abb-146">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="37abb-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="37abb-147">-ResourceType</span></span>
<span data-ttu-id="37abb-148">잠금이 적용 되는 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-148">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="37abb-149">-범위</span><span class="sxs-lookup"><span data-stu-id="37abb-149">-Scope</span></span>
<span data-ttu-id="37abb-150">잠금이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-150">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="37abb-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="37abb-151">-TenantLevel</span></span>
<span data-ttu-id="37abb-152">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="37abb-153">-확인</span><span class="sxs-lookup"><span data-stu-id="37abb-153">-Confirm</span></span>
<span data-ttu-id="37abb-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37abb-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37abb-155">-WhatIf</span></span>
<span data-ttu-id="37abb-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37abb-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37abb-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37abb-158">CommonParameters</span></span>
<span data-ttu-id="37abb-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37abb-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37abb-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37abb-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37abb-161">입력</span><span class="sxs-lookup"><span data-stu-id="37abb-161">INPUTS</span></span>

## <span data-ttu-id="37abb-162">출력</span><span class="sxs-lookup"><span data-stu-id="37abb-162">OUTPUTS</span></span>

## <span data-ttu-id="37abb-163">상속자</span><span class="sxs-lookup"><span data-stu-id="37abb-163">NOTES</span></span>

## <span data-ttu-id="37abb-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37abb-164">RELATED LINKS</span></span>

[<span data-ttu-id="37abb-165">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="37abb-165">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="37abb-166">새로운 AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="37abb-166">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="37abb-167">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="37abb-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


