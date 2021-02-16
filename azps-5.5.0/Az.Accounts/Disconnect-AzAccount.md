---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disconnect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
ms.openlocfilehash: 23689d4e84228d4eaeaae82e2efe53b6450d44f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178129"
---
# <span data-ttu-id="10b9a-101">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="10b9a-101">Disconnect-AzAccount</span></span>

## <span data-ttu-id="10b9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="10b9a-103">연결된 Azure 계정의 연결을 끊고 해당 계정과 연결된 모든 자격 증명 및 컨텍스트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="10b9a-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

## <span data-ttu-id="10b9a-104">구문</span><span class="sxs-lookup"><span data-stu-id="10b9a-104">SYNTAX</span></span>

### <span data-ttu-id="10b9a-105">ContextName(기본값)</span><span class="sxs-lookup"><span data-stu-id="10b9a-105">ContextName (Default)</span></span>
```
Disconnect-AzAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10b9a-106">UserId</span><span class="sxs-lookup"><span data-stu-id="10b9a-106">UserId</span></span>
```
Disconnect-AzAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10b9a-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="10b9a-107">ServicePrincipal</span></span>
```
Disconnect-AzAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10b9a-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="10b9a-108">AccountObject</span></span>
```
Disconnect-AzAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10b9a-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="10b9a-109">ContextObject</span></span>
```
Disconnect-AzAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10b9a-110">설명</span><span class="sxs-lookup"><span data-stu-id="10b9a-110">DESCRIPTION</span></span>
<span data-ttu-id="10b9a-111">이 Disconnect-AzAccount cmdlet은 연결된 Azure 계정의 연결을 끊고 해당 계정과 연결된 모든 자격 증명 및 컨텍스트(구독 및 테넌트 정보)를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="10b9a-111">The Disconnect-AzAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="10b9a-112">이 cmdlet을 실행한 후 Connect-AzAccount를 사용하여 다시 로그인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="10b9a-112">After executing this cmdlet, you will need to login again using Connect-AzAccount.</span></span>

## <span data-ttu-id="10b9a-113">예제</span><span class="sxs-lookup"><span data-stu-id="10b9a-113">EXAMPLES</span></span>

### <span data-ttu-id="10b9a-114">예제 1: 현재 계정 로그아웃</span><span class="sxs-lookup"><span data-stu-id="10b9a-114">Example 1: Logout of the current account</span></span>
```powershell
PS C:\> Disconnect-AzAccount
```

<span data-ttu-id="10b9a-115">현재 컨텍스트와 연결된 Azure 계정에서 로그아웃합니다.</span><span class="sxs-lookup"><span data-stu-id="10b9a-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="10b9a-116">예제 2: 특정 컨텍스트와 연결된 계정 로그아웃</span><span class="sxs-lookup"><span data-stu-id="10b9a-116">Example 2: Logout of the account associated with a particular context</span></span>
```powershell
PS C:\> Get-AzContext "Work" | Disconnect-AzAccount -Scope CurrentUser
```

<span data-ttu-id="10b9a-117">지정한 컨텍스트('Work'라는 이름)와 연결된 계정을 로그아웃합니다.</span><span class="sxs-lookup"><span data-stu-id="10b9a-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="10b9a-118">'CurrentUser' 범위를 사용하기 때문에 모든 자격 증명 및 컨텍스트가 영구적으로 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="10b9a-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="10b9a-119">예제 3: 특정 사용자 로그아웃</span><span class="sxs-lookup"><span data-stu-id="10b9a-119">Example 3: Log out a particular user</span></span>
```powershell
PS C:\> Disconnect-AzAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="10b9a-120">'' 사용자 로그아웃 - 이 사용자와 연결된 모든 자격 증명 및 모든 컨텍스트가 user1@contoso.org 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="10b9a-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="10b9a-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10b9a-121">PARAMETERS</span></span>

### <span data-ttu-id="10b9a-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="10b9a-122">-ApplicationId</span></span>
<span data-ttu-id="10b9a-123">ServicePrincipal ID(전역적으로 고유한 ID)</span><span class="sxs-lookup"><span data-stu-id="10b9a-123">ServicePrincipal id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b9a-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="10b9a-124">-AzureContext</span></span>
<span data-ttu-id="10b9a-125">컨텍스트</span><span class="sxs-lookup"><span data-stu-id="10b9a-125">Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: ContextObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10b9a-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="10b9a-126">-ContextName</span></span>
<span data-ttu-id="10b9a-127">로그아웃할 컨텍스트의 이름</span><span class="sxs-lookup"><span data-stu-id="10b9a-127">Name of the context to log out of</span></span>

```yaml
Type: System.String
Parameter Sets: ContextName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b9a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b9a-128">-DefaultProfile</span></span>
<span data-ttu-id="10b9a-129">Azure와의 통신에 사용되는 자격 증명, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="10b9a-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10b9a-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10b9a-130">-InputObject</span></span>
<span data-ttu-id="10b9a-131">제거할 계정 개체</span><span class="sxs-lookup"><span data-stu-id="10b9a-131">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10b9a-132">-Scope</span><span class="sxs-lookup"><span data-stu-id="10b9a-132">-Scope</span></span>
<span data-ttu-id="10b9a-133">컨텍스트 변경 범위(예: 변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용되는지 여부)를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="10b9a-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b9a-134">-TenantId</span><span class="sxs-lookup"><span data-stu-id="10b9a-134">-TenantId</span></span>
<span data-ttu-id="10b9a-135">테넌트 ID(전역적으로 고유한 ID)</span><span class="sxs-lookup"><span data-stu-id="10b9a-135">Tenant id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b9a-136">-Username</span><span class="sxs-lookup"><span data-stu-id="10b9a-136">-Username</span></span>
<span data-ttu-id="10b9a-137">'폼의 사용자 user@contoso.org 이름'</span><span class="sxs-lookup"><span data-stu-id="10b9a-137">User name of the form 'user@contoso.org'</span></span>

```yaml
Type: System.String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b9a-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10b9a-138">-Confirm</span></span>
<span data-ttu-id="10b9a-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="10b9a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10b9a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10b9a-140">-WhatIf</span></span>
<span data-ttu-id="10b9a-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="10b9a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10b9a-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10b9a-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="10b9a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b9a-143">CommonParameters</span></span>
<span data-ttu-id="10b9a-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="10b9a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b9a-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="10b9a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b9a-146">입력</span><span class="sxs-lookup"><span data-stu-id="10b9a-146">INPUTS</span></span>

### <span data-ttu-id="10b9a-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="10b9a-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="10b9a-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="10b9a-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="10b9a-149">출력</span><span class="sxs-lookup"><span data-stu-id="10b9a-149">OUTPUTS</span></span>

### <span data-ttu-id="10b9a-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="10b9a-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="10b9a-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="10b9a-151">NOTES</span></span>

## <span data-ttu-id="10b9a-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10b9a-152">RELATED LINKS</span></span>
