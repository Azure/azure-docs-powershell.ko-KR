---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 6b9a0b792b1a8a5572ce26561202284f3103d764
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876380"
---
# <span data-ttu-id="e2a19-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e2a19-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="e2a19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2a19-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a19-103">리소스 잠금을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-103">Removes a resource lock.</span></span>

## <span data-ttu-id="e2a19-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2a19-104">SYNTAX</span></span>

### <span data-ttu-id="e2a19-105">ByLockId (기본값)</span><span class="sxs-lookup"><span data-stu-id="e2a19-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a19-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e2a19-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a19-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="e2a19-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2a19-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="e2a19-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a19-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="e2a19-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2a19-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e2a19-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2a19-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="e2a19-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2a19-112">설명은</span><span class="sxs-lookup"><span data-stu-id="e2a19-112">DESCRIPTION</span></span>
<span data-ttu-id="e2a19-113">**AzResourceLock** Cmdlet은 Azure 리소스 잠금을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="e2a19-114">예제의</span><span class="sxs-lookup"><span data-stu-id="e2a19-114">EXAMPLES</span></span>

### <span data-ttu-id="e2a19-115">예제 1: 잠금 제거</span><span class="sxs-lookup"><span data-stu-id="e2a19-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="e2a19-116">이 명령은 ContosoSiteLock 라는 잠금을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="e2a19-117">변수</span><span class="sxs-lookup"><span data-stu-id="e2a19-117">PARAMETERS</span></span>

### <span data-ttu-id="e2a19-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e2a19-118">-ApiVersion</span></span>
<span data-ttu-id="e2a19-119">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e2a19-120">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e2a19-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2a19-121">-DefaultProfile</span></span>
<span data-ttu-id="e2a19-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e2a19-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a19-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e2a19-123">-Force</span></span>
<span data-ttu-id="e2a19-124">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e2a19-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e2a19-125">-InformationAction</span></span>
<span data-ttu-id="e2a19-126">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="e2a19-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e2a19-128">하기로</span><span class="sxs-lookup"><span data-stu-id="e2a19-128">Continue</span></span>
- <span data-ttu-id="e2a19-129">숨기기</span><span class="sxs-lookup"><span data-stu-id="e2a19-129">Ignore</span></span>
- <span data-ttu-id="e2a19-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="e2a19-130">Inquire</span></span>
- <span data-ttu-id="e2a19-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e2a19-131">SilentlyContinue</span></span>
- <span data-ttu-id="e2a19-132">중지가</span><span class="sxs-lookup"><span data-stu-id="e2a19-132">Stop</span></span>
- <span data-ttu-id="e2a19-133">대기</span><span class="sxs-lookup"><span data-stu-id="e2a19-133">Suspend</span></span>

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

### <span data-ttu-id="e2a19-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e2a19-134">-InformationVariable</span></span>
<span data-ttu-id="e2a19-135">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e2a19-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="e2a19-136">-LockId</span></span>
<span data-ttu-id="e2a19-137">이 cmdlet이 제거 하는 잠금의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e2a19-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="e2a19-138">-LockName</span></span>
<span data-ttu-id="e2a19-139">이 cmdlet이 제거 하는 잠금의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-139">Specifies the name of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e2a19-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="e2a19-140">-Pre</span></span>
<span data-ttu-id="e2a19-141">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e2a19-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2a19-142">-ResourceGroupName</span></span>
<span data-ttu-id="e2a19-143">잠금이 적용 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-143">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="e2a19-144">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="e2a19-144">-ResourceName</span></span>
<span data-ttu-id="e2a19-145">잠금이 적용 되는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="e2a19-146">예를 들어 데이터베이스를 지정 하려면 서버 데이터베이스 형식으로 다음을 사용 합니다. `/`</span><span class="sxs-lookup"><span data-stu-id="e2a19-146">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="e2a19-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e2a19-147">-ResourceType</span></span>
<span data-ttu-id="e2a19-148">잠금이 적용 되는 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-148">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="e2a19-149">-범위</span><span class="sxs-lookup"><span data-stu-id="e2a19-149">-Scope</span></span>
<span data-ttu-id="e2a19-150">잠금이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-150">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="e2a19-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="e2a19-151">-TenantLevel</span></span>
<span data-ttu-id="e2a19-152">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="e2a19-153">-확인</span><span class="sxs-lookup"><span data-stu-id="e2a19-153">-Confirm</span></span>
<span data-ttu-id="e2a19-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2a19-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2a19-155">-WhatIf</span></span>
<span data-ttu-id="e2a19-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2a19-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2a19-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a19-158">CommonParameters</span></span>
<span data-ttu-id="e2a19-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2a19-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a19-160">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2a19-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a19-161">입력</span><span class="sxs-lookup"><span data-stu-id="e2a19-161">INPUTS</span></span>

## <span data-ttu-id="e2a19-162">출력</span><span class="sxs-lookup"><span data-stu-id="e2a19-162">OUTPUTS</span></span>

## <span data-ttu-id="e2a19-163">상속자</span><span class="sxs-lookup"><span data-stu-id="e2a19-163">NOTES</span></span>

## <span data-ttu-id="e2a19-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2a19-164">RELATED LINKS</span></span>

[<span data-ttu-id="e2a19-165">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e2a19-165">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="e2a19-166">새로운 AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e2a19-166">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="e2a19-167">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e2a19-167">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


