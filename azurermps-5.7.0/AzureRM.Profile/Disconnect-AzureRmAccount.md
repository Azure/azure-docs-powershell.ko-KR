---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
ms.openlocfilehash: e72e326fd3251a9b3150b9def06e2fb60afb7d82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704018"
---
# <span data-ttu-id="a9293-101">Disconnect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="a9293-101">Disconnect-AzureRmAccount</span></span>

## <span data-ttu-id="a9293-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9293-102">SYNOPSIS</span></span>
<span data-ttu-id="a9293-103">연결 된 Azure 계정의 연결을 끊고 해당 계정과 관련 된 모든 자격 증명과 컨텍스트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9293-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9293-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a9293-104">SYNTAX</span></span>

### <span data-ttu-id="a9293-105">컨텍스트 이름 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a9293-105">ContextName (Default)</span></span>
```
Disconnect-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9293-106">UserId</span><span class="sxs-lookup"><span data-stu-id="a9293-106">UserId</span></span>
```
Disconnect-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9293-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a9293-107">ServicePrincipal</span></span>
```
Disconnect-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9293-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a9293-108">AccountObject</span></span>
```
Disconnect-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9293-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="a9293-109">ContextObject</span></span>
```
Disconnect-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9293-110">설명은</span><span class="sxs-lookup"><span data-stu-id="a9293-110">DESCRIPTION</span></span>
<span data-ttu-id="a9293-111">Disconnect-AzureRmAccount cmdlet은 연결 된 Azure 계정의 연결을 끊고 해당 계정과 연결 된 모든 자격 증명과 컨텍스트 (구독 및 테 넌 트 정보)를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9293-111">The Disconnect-AzureRmAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>

<span data-ttu-id="a9293-112">이 cmdlet을 실행 한 후에는 Connect-AzureRmAccount를 사용 하 여 다시 로그인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9293-112">After executing this cmdlet, you will need to login again using Connect-AzureRmAccount.</span></span>

## <span data-ttu-id="a9293-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a9293-113">EXAMPLES</span></span>

### <span data-ttu-id="a9293-114">현재 계정 로그 아웃</span><span class="sxs-lookup"><span data-stu-id="a9293-114">Logout of the current account</span></span>
```
PS C:\> Disconnect-AzureRmAccount
```

<span data-ttu-id="a9293-115">현재 컨텍스트와 연결 된 Azure 계정에서 로그 아웃 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9293-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="a9293-116">특정 컨텍스트와 연결 된 계정 로그 아웃</span><span class="sxs-lookup"><span data-stu-id="a9293-116">Logout of the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Disconnect-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="a9293-117">지정 된 컨텍스트 (' Work ')와 연결 된 계정을 로그 아웃 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9293-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="a9293-118">이는 ' CurrentUser ' 범위를 사용 하기 때문에 모든 자격 증명과 컨텍스트는 영구적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9293-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="a9293-119">특정 사용자 로그 아웃</span><span class="sxs-lookup"><span data-stu-id="a9293-119">Log out a particular user</span></span>
```
PS C:\> Disconnect-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="a9293-120">' user1@contoso.org ' 사용자-모든 자격 증명을 로그 아웃 하 고이 사용자와 연결 된 모든 컨텍스트가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9293-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="a9293-121">변수</span><span class="sxs-lookup"><span data-stu-id="a9293-121">PARAMETERS</span></span>

### <span data-ttu-id="a9293-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a9293-122">-ApplicationId</span></span>
<span data-ttu-id="a9293-123">ServicePrincipal id (전역 고유 id)</span><span class="sxs-lookup"><span data-stu-id="a9293-123">ServicePrincipal id (globally unique id)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9293-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="a9293-124">-AzureContext</span></span>
<span data-ttu-id="a9293-125">상황별</span><span class="sxs-lookup"><span data-stu-id="a9293-125">Context</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: ContextObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9293-126">-컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="a9293-126">-ContextName</span></span>
<span data-ttu-id="a9293-127">로그 아웃할 컨텍스트의 이름</span><span class="sxs-lookup"><span data-stu-id="a9293-127">Name of the context to log out of</span></span>

```yaml
Type: String
Parameter Sets: ContextName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9293-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9293-128">-DefaultProfile</span></span>
<span data-ttu-id="a9293-129">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a9293-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9293-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9293-130">-InputObject</span></span>
<span data-ttu-id="a9293-131">제거할 account 개체</span><span class="sxs-lookup"><span data-stu-id="a9293-131">The account object to remove</span></span>

```yaml
Type: PSAzureRmAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9293-132">-범위</span><span class="sxs-lookup"><span data-stu-id="a9293-132">-Scope</span></span>
<span data-ttu-id="a9293-133">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9293-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9293-134">-TenantId</span><span class="sxs-lookup"><span data-stu-id="a9293-134">-TenantId</span></span>
<span data-ttu-id="a9293-135">테 넌 트 id (전역 고유 id)</span><span class="sxs-lookup"><span data-stu-id="a9293-135">Tenant id (globally unique id)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9293-136">-사용자 이름</span><span class="sxs-lookup"><span data-stu-id="a9293-136">-Username</span></span>
<span data-ttu-id="a9293-137">' ' 양식의 사용자 이름입니다. user@contoso.org</span><span class="sxs-lookup"><span data-stu-id="a9293-137">User name of the form 'user@contoso.org'</span></span>

```yaml
Type: String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9293-138">-확인</span><span class="sxs-lookup"><span data-stu-id="a9293-138">-Confirm</span></span>
<span data-ttu-id="a9293-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9293-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9293-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9293-140">-WhatIf</span></span>
<span data-ttu-id="a9293-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a9293-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9293-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9293-142">The cmdlet is not executed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9293-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9293-143">CommonParameters</span></span>
<span data-ttu-id="a9293-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9293-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9293-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9293-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9293-146">입력</span><span class="sxs-lookup"><span data-stu-id="a9293-146">INPUTS</span></span>

### <span data-ttu-id="a9293-147">PSAzureRmAccount (. \*)</span><span class="sxs-lookup"><span data-stu-id="a9293-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="a9293-148">Microsoft. Azure. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="a9293-148">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="a9293-149">출력</span><span class="sxs-lookup"><span data-stu-id="a9293-149">OUTPUTS</span></span>

### <span data-ttu-id="a9293-150">PSAzureRmAccount (. \*)</span><span class="sxs-lookup"><span data-stu-id="a9293-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="a9293-151">상속자</span><span class="sxs-lookup"><span data-stu-id="a9293-151">NOTES</span></span>

## <span data-ttu-id="a9293-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9293-152">RELATED LINKS</span></span>
