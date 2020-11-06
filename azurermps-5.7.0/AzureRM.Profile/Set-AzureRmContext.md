---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
ms.openlocfilehash: bffd818df21be78d0418bf3d2ac1ebea401dbf19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534748"
---
# <span data-ttu-id="a5998-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a5998-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="a5998-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5998-102">SYNOPSIS</span></span>
<span data-ttu-id="a5998-103">Cmdlet에 대 한 테 넌 트, 구독 및 환경을 현재 세션에서 사용할 수 있도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5998-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5998-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5998-104">SYNTAX</span></span>

### <span data-ttu-id="a5998-105">Context (기본값)</span><span class="sxs-lookup"><span data-stu-id="a5998-105">Context (Default)</span></span>
```
Set-AzureRmContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5998-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="a5998-106">TenantObject</span></span>
```
Set-AzureRmContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5998-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="a5998-107">SubscriptionObject</span></span>
```
Set-AzureRmContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5998-108">구독</span><span class="sxs-lookup"><span data-stu-id="a5998-108">Subscription</span></span>
```
Set-AzureRmContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5998-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="a5998-109">TenantNameOnly</span></span>
```
Set-AzureRmContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5998-110">설명은</span><span class="sxs-lookup"><span data-stu-id="a5998-110">DESCRIPTION</span></span>
<span data-ttu-id="a5998-111">Set-AzureRmContext cmdlet은 현재 세션에서 실행 하는 cmdlet에 대 한 인증 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5998-111">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="a5998-112">컨텍스트에는 테 넌 트, 구독 및 환경 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5998-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="a5998-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a5998-113">EXAMPLES</span></span>

### <span data-ttu-id="a5998-114">예제 1: 구독 컨텍스트 설정</span><span class="sxs-lookup"><span data-stu-id="a5998-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="a5998-115">이 명령은 지정 된 구독을 사용 하도록 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5998-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="a5998-116">변수</span><span class="sxs-lookup"><span data-stu-id="a5998-116">PARAMETERS</span></span>

### <span data-ttu-id="a5998-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a5998-117">-Context</span></span>
<span data-ttu-id="a5998-118">현재 세션에 대 한 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5998-118">Specifies the context for the current session.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5998-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5998-119">-DefaultProfile</span></span>
<span data-ttu-id="a5998-120">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5998-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5998-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="a5998-121">-ExtendedProperty</span></span>
<span data-ttu-id="a5998-122">추가 컨텍스트 속성</span><span class="sxs-lookup"><span data-stu-id="a5998-122">Additional context properties</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5998-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a5998-123">-Force</span></span>
<span data-ttu-id="a5998-124">기존 컨텍스트를 같은 이름으로 덮어씁니다 (있는 경우).</span><span class="sxs-lookup"><span data-stu-id="a5998-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="a5998-125">-이름</span><span class="sxs-lookup"><span data-stu-id="a5998-125">-Name</span></span>
<span data-ttu-id="a5998-126">컨텍스트의 이름</span><span class="sxs-lookup"><span data-stu-id="a5998-126">Name of the context</span></span>

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

### <span data-ttu-id="a5998-127">-범위</span><span class="sxs-lookup"><span data-stu-id="a5998-127">-Scope</span></span>
<span data-ttu-id="a5998-128">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5998-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="a5998-129">-구독</span><span class="sxs-lookup"><span data-stu-id="a5998-129">-Subscription</span></span>
<span data-ttu-id="a5998-130">구독 이름 또는 Id</span><span class="sxs-lookup"><span data-stu-id="a5998-130">Subscription Name or Id</span></span>

```yaml
Type: String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5998-131">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="a5998-131">-SubscriptionObject</span></span>
<span data-ttu-id="a5998-132">구독 개체</span><span class="sxs-lookup"><span data-stu-id="a5998-132">A subscription object</span></span>

```yaml
Type: PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5998-133">-테 넌 트</span><span class="sxs-lookup"><span data-stu-id="a5998-133">-Tenant</span></span>
<span data-ttu-id="a5998-134">테 넌 트 이름 또는 ID</span><span class="sxs-lookup"><span data-stu-id="a5998-134">Tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5998-135">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="a5998-135">-TenantObject</span></span>
<span data-ttu-id="a5998-136">테 넌 트 개체</span><span class="sxs-lookup"><span data-stu-id="a5998-136">A Tenant Object</span></span>

```yaml
Type: PSAzureTenant
Parameter Sets: TenantObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5998-137">-확인</span><span class="sxs-lookup"><span data-stu-id="a5998-137">-Confirm</span></span>
<span data-ttu-id="a5998-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5998-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5998-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5998-139">-WhatIf</span></span>
<span data-ttu-id="a5998-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5998-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5998-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5998-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5998-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5998-142">CommonParameters</span></span>
<span data-ttu-id="a5998-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5998-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5998-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5998-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5998-145">입력</span><span class="sxs-lookup"><span data-stu-id="a5998-145">INPUTS</span></span>

### <span data-ttu-id="a5998-146">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="a5998-146">PSAzureContext</span></span>
<span data-ttu-id="a5998-147">' Context ' 매개 변수는 파이프라인에서 ' PSAzureContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5998-147">Parameter 'Context' accepts value of type 'PSAzureContext' from the pipeline</span></span>

## <span data-ttu-id="a5998-148">출력</span><span class="sxs-lookup"><span data-stu-id="a5998-148">OUTPUTS</span></span>

### <span data-ttu-id="a5998-149">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="a5998-149">PSAzureContext</span></span>

## <span data-ttu-id="a5998-150">상속자</span><span class="sxs-lookup"><span data-stu-id="a5998-150">NOTES</span></span>

## <span data-ttu-id="a5998-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5998-151">RELATED LINKS</span></span>

[<span data-ttu-id="a5998-152">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="a5998-152">Get-AzureRMContext</span></span>](./Get-AzureRMContext.md)

