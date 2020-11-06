---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: c45d78b815586e54c9f39cfd536fed5a26c2eb19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532943"
---
# <span data-ttu-id="81eac-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="81eac-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="81eac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81eac-102">SYNOPSIS</span></span>
<span data-ttu-id="81eac-103">리소스 잠금을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81eac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="81eac-104">SYNTAX</span></span>

### <span data-ttu-id="81eac-105">잠금 (Id 기준)입니다. (기본값)</span><span class="sxs-lookup"><span data-stu-id="81eac-105">A lock, by Id. (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81eac-106">리소스 그룹 범위에서 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-106">A lock at the resource group scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81eac-107">리소스 그룹 리소스 범위에서 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-107">A lock at the resource group resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81eac-108">지정 된 범위에 있는 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-108">A lock at the specified scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81eac-109">구독 범위에서 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-109">A lock at the subscription scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81eac-110">구독 리소스 범위에서 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-110">A lock at the subscription resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81eac-111">테 넌 트 리소스 범위에서 잠금입니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-111">A lock at the tenant resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81eac-112">설명은</span><span class="sxs-lookup"><span data-stu-id="81eac-112">DESCRIPTION</span></span>
<span data-ttu-id="81eac-113">**AzureRmResourceLock** Cmdlet은 Azure 리소스 잠금을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="81eac-114">예제의</span><span class="sxs-lookup"><span data-stu-id="81eac-114">EXAMPLES</span></span>

### <span data-ttu-id="81eac-115">예제 1: 잠금 제거</span><span class="sxs-lookup"><span data-stu-id="81eac-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="81eac-116">이 명령은 ContosoSiteLock 라는 잠금을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="81eac-117">변수</span><span class="sxs-lookup"><span data-stu-id="81eac-117">PARAMETERS</span></span>

### <span data-ttu-id="81eac-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="81eac-118">-ApiVersion</span></span>
<span data-ttu-id="81eac-119">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="81eac-120">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="81eac-121">-Force</span><span class="sxs-lookup"><span data-stu-id="81eac-121">-Force</span></span>
<span data-ttu-id="81eac-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="81eac-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="81eac-123">-InformationAction</span></span>
<span data-ttu-id="81eac-124">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="81eac-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81eac-126">하기로</span><span class="sxs-lookup"><span data-stu-id="81eac-126">Continue</span></span>
- <span data-ttu-id="81eac-127">숨기기</span><span class="sxs-lookup"><span data-stu-id="81eac-127">Ignore</span></span>
- <span data-ttu-id="81eac-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="81eac-128">Inquire</span></span>
- <span data-ttu-id="81eac-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="81eac-129">SilentlyContinue</span></span>
- <span data-ttu-id="81eac-130">중지가</span><span class="sxs-lookup"><span data-stu-id="81eac-130">Stop</span></span>
- <span data-ttu-id="81eac-131">대기</span><span class="sxs-lookup"><span data-stu-id="81eac-131">Suspend</span></span>

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

### <span data-ttu-id="81eac-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="81eac-132">-InformationVariable</span></span>
<span data-ttu-id="81eac-133">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="81eac-134">-LockId</span><span class="sxs-lookup"><span data-stu-id="81eac-134">-LockId</span></span>
<span data-ttu-id="81eac-135">이 cmdlet이 제거 하는 잠금의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-135">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="81eac-136">-LockName</span><span class="sxs-lookup"><span data-stu-id="81eac-136">-LockName</span></span>
<span data-ttu-id="81eac-137">이 cmdlet이 제거 하는 잠금의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-137">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81eac-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="81eac-138">-Pre</span></span>
<span data-ttu-id="81eac-139">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="81eac-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81eac-140">-ResourceGroupName</span></span>
<span data-ttu-id="81eac-141">잠금이 적용 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-141">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="81eac-142">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="81eac-142">-ResourceName</span></span>
<span data-ttu-id="81eac-143">잠금이 적용 되는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-143">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="81eac-144">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-144">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="81eac-145">서버 `/` 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="81eac-145">Server`/`Database</span></span>

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

### <span data-ttu-id="81eac-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="81eac-146">-ResourceType</span></span>
<span data-ttu-id="81eac-147">잠금이 적용 되는 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-147">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="81eac-148">-범위</span><span class="sxs-lookup"><span data-stu-id="81eac-148">-Scope</span></span>
<span data-ttu-id="81eac-149">잠금이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-149">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="81eac-150">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="81eac-150">-TenantLevel</span></span>
<span data-ttu-id="81eac-151">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-151">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="81eac-152">-확인</span><span class="sxs-lookup"><span data-stu-id="81eac-152">-Confirm</span></span>
<span data-ttu-id="81eac-153">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81eac-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81eac-154">-WhatIf</span></span>
<span data-ttu-id="81eac-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81eac-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81eac-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81eac-157">-DefaultProfile</span></span>
<span data-ttu-id="81eac-158">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81eac-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81eac-159">CommonParameters</span></span>
<span data-ttu-id="81eac-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81eac-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81eac-161">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81eac-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81eac-162">입력</span><span class="sxs-lookup"><span data-stu-id="81eac-162">INPUTS</span></span>

## <span data-ttu-id="81eac-163">출력</span><span class="sxs-lookup"><span data-stu-id="81eac-163">OUTPUTS</span></span>

### <span data-ttu-id="81eac-164">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="81eac-164">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="81eac-165">상속자</span><span class="sxs-lookup"><span data-stu-id="81eac-165">NOTES</span></span>

## <span data-ttu-id="81eac-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81eac-166">RELATED LINKS</span></span>

[<span data-ttu-id="81eac-167">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="81eac-167">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="81eac-168">새로운 AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="81eac-168">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="81eac-169">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="81eac-169">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


