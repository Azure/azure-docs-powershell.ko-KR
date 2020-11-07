---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
ms.openlocfilehash: e5fbecea64a15569fbd6319f3f3be5ff4102153e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711315"
---
# <span data-ttu-id="286bc-101">Disconnect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="286bc-101">Disconnect-AzureRmAccount</span></span>

## <span data-ttu-id="286bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="286bc-102">SYNOPSIS</span></span>
<span data-ttu-id="286bc-103">연결 된 Azure 계정의 연결을 끊고 해당 계정과 관련 된 모든 자격 증명과 컨텍스트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="286bc-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="286bc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="286bc-104">SYNTAX</span></span>

### <span data-ttu-id="286bc-105">컨텍스트 이름 (기본값)</span><span class="sxs-lookup"><span data-stu-id="286bc-105">ContextName (Default)</span></span>
```
Disconnect-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="286bc-106">UserId</span><span class="sxs-lookup"><span data-stu-id="286bc-106">UserId</span></span>
```
Disconnect-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="286bc-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="286bc-107">ServicePrincipal</span></span>
```
Disconnect-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="286bc-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="286bc-108">AccountObject</span></span>
```
Disconnect-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="286bc-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="286bc-109">ContextObject</span></span>
```
Disconnect-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="286bc-110">설명은</span><span class="sxs-lookup"><span data-stu-id="286bc-110">DESCRIPTION</span></span>
<span data-ttu-id="286bc-111">Disconnect-AzureRmAccount cmdlet은 연결 된 Azure 계정의 연결을 끊고 해당 계정과 연결 된 모든 자격 증명과 컨텍스트 (구독 및 테 넌 트 정보)를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="286bc-111">The Disconnect-AzureRmAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="286bc-112">이 cmdlet을 실행 한 후에는 Connect-AzureRmAccount를 사용 하 여 다시 로그인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="286bc-112">After executing this cmdlet, you will need to login again using Connect-AzureRmAccount.</span></span>

## <span data-ttu-id="286bc-113">예제의</span><span class="sxs-lookup"><span data-stu-id="286bc-113">EXAMPLES</span></span>

### <span data-ttu-id="286bc-114">현재 계정 로그 아웃</span><span class="sxs-lookup"><span data-stu-id="286bc-114">Logout of the current account</span></span>
```
PS C:\> Disconnect-AzureRmAccount
```

<span data-ttu-id="286bc-115">현재 컨텍스트와 연결 된 Azure 계정에서 로그 아웃 합니다.</span><span class="sxs-lookup"><span data-stu-id="286bc-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="286bc-116">특정 컨텍스트와 연결 된 계정 로그 아웃</span><span class="sxs-lookup"><span data-stu-id="286bc-116">Logout of the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Disconnect-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="286bc-117">지정 된 컨텍스트 (' Work ')와 연결 된 계정을 로그 아웃 합니다.</span><span class="sxs-lookup"><span data-stu-id="286bc-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="286bc-118">이는 ' CurrentUser ' 범위를 사용 하기 때문에 모든 자격 증명과 컨텍스트는 영구적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="286bc-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="286bc-119">특정 사용자 로그 아웃</span><span class="sxs-lookup"><span data-stu-id="286bc-119">Log out a particular user</span></span>
```
PS C:\> Disconnect-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="286bc-120">' user1@contoso.org ' 사용자-모든 자격 증명을 로그 아웃 하 고이 사용자와 연결 된 모든 컨텍스트가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="286bc-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="286bc-121">변수</span><span class="sxs-lookup"><span data-stu-id="286bc-121">PARAMETERS</span></span>

### <span data-ttu-id="286bc-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="286bc-122">-ApplicationId</span></span>
<span data-ttu-id="286bc-123">ServicePrincipal id (전역 고유 id)</span><span class="sxs-lookup"><span data-stu-id="286bc-123">ServicePrincipal id (globally unique id)</span></span>

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

### <span data-ttu-id="286bc-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="286bc-124">-AzureContext</span></span>
<span data-ttu-id="286bc-125">상황별</span><span class="sxs-lookup"><span data-stu-id="286bc-125">Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: ContextObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="286bc-126">-컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="286bc-126">-ContextName</span></span>
<span data-ttu-id="286bc-127">로그 아웃할 컨텍스트의 이름</span><span class="sxs-lookup"><span data-stu-id="286bc-127">Name of the context to log out of</span></span>

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

### <span data-ttu-id="286bc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="286bc-128">-DefaultProfile</span></span>
<span data-ttu-id="286bc-129">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="286bc-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="286bc-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="286bc-130">-InputObject</span></span>
<span data-ttu-id="286bc-131">제거할 account 개체</span><span class="sxs-lookup"><span data-stu-id="286bc-131">The account object to remove</span></span>

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

### <span data-ttu-id="286bc-132">-범위</span><span class="sxs-lookup"><span data-stu-id="286bc-132">-Scope</span></span>
<span data-ttu-id="286bc-133">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="286bc-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="286bc-134">-TenantId</span><span class="sxs-lookup"><span data-stu-id="286bc-134">-TenantId</span></span>
<span data-ttu-id="286bc-135">테 넌 트 id (전역 고유 id)</span><span class="sxs-lookup"><span data-stu-id="286bc-135">Tenant id (globally unique id)</span></span>

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

### <span data-ttu-id="286bc-136">-사용자 이름</span><span class="sxs-lookup"><span data-stu-id="286bc-136">-Username</span></span>
<span data-ttu-id="286bc-137">' ' 양식의 사용자 이름입니다. user@contoso.org</span><span class="sxs-lookup"><span data-stu-id="286bc-137">User name of the form 'user@contoso.org'</span></span>

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

### <span data-ttu-id="286bc-138">-확인</span><span class="sxs-lookup"><span data-stu-id="286bc-138">-Confirm</span></span>
<span data-ttu-id="286bc-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="286bc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="286bc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="286bc-140">-WhatIf</span></span>
<span data-ttu-id="286bc-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="286bc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="286bc-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="286bc-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="286bc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286bc-143">CommonParameters</span></span>
<span data-ttu-id="286bc-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="286bc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286bc-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="286bc-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286bc-146">입력</span><span class="sxs-lookup"><span data-stu-id="286bc-146">INPUTS</span></span>

### <span data-ttu-id="286bc-147">PSAzureRmAccount (. \*)</span><span class="sxs-lookup"><span data-stu-id="286bc-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>
<span data-ttu-id="286bc-148">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="286bc-148">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="286bc-149">Microsoft. Azure. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="286bc-149">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="286bc-150">매개 변수: AzureContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="286bc-150">Parameters: AzureContext (ByValue)</span></span>

## <span data-ttu-id="286bc-151">출력</span><span class="sxs-lookup"><span data-stu-id="286bc-151">OUTPUTS</span></span>

### <span data-ttu-id="286bc-152">PSAzureRmAccount (. \*)</span><span class="sxs-lookup"><span data-stu-id="286bc-152">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="286bc-153">상속자</span><span class="sxs-lookup"><span data-stu-id="286bc-153">NOTES</span></span>

## <span data-ttu-id="286bc-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="286bc-154">RELATED LINKS</span></span>
