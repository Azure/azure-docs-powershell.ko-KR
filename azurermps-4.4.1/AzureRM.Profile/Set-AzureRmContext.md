---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
ms.openlocfilehash: 99adb0cb38cd5c1e43dbd9f7dd5f81a4bef26beb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703343"
---
# <span data-ttu-id="75fb1-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="75fb1-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="75fb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="75fb1-103">Cmdlet에 대 한 테 넌 트, 구독 및 환경을 현재 세션에서 사용할 수 있도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75fb1-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75fb1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75fb1-104">SYNTAX</span></span>

### <span data-ttu-id="75fb1-105">Context (기본값)</span><span class="sxs-lookup"><span data-stu-id="75fb1-105">Context (Default)</span></span>
```
Set-AzureRmContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75fb1-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="75fb1-106">TenantObject</span></span>
```
Set-AzureRmContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75fb1-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="75fb1-107">SubscriptionObject</span></span>
```
Set-AzureRmContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75fb1-108">구독</span><span class="sxs-lookup"><span data-stu-id="75fb1-108">Subscription</span></span>
```
Set-AzureRmContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75fb1-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="75fb1-109">TenantNameOnly</span></span>
```
Set-AzureRmContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75fb1-110">설명은</span><span class="sxs-lookup"><span data-stu-id="75fb1-110">DESCRIPTION</span></span>
<span data-ttu-id="75fb1-111">Set-AzureRmContext cmdlet은 현재 세션에서 실행 하는 cmdlet에 대 한 인증 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75fb1-111">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="75fb1-112">컨텍스트에는 테 넌 트, 구독 및 환경 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75fb1-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="75fb1-113">예제의</span><span class="sxs-lookup"><span data-stu-id="75fb1-113">EXAMPLES</span></span>

### <span data-ttu-id="75fb1-114">예제 1: 구독 컨텍스트 설정</span><span class="sxs-lookup"><span data-stu-id="75fb1-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="75fb1-115">이 명령은 지정 된 구독을 사용 하도록 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75fb1-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="75fb1-116">변수</span><span class="sxs-lookup"><span data-stu-id="75fb1-116">PARAMETERS</span></span>

### <span data-ttu-id="75fb1-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="75fb1-117">-Context</span></span>
<span data-ttu-id="75fb1-118">현재 세션에 대 한 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75fb1-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75fb1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75fb1-119">-DefaultProfile</span></span>
<span data-ttu-id="75fb1-120">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75fb1-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75fb1-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="75fb1-121">-ExtendedProperty</span></span>
<span data-ttu-id="75fb1-122">추가 컨텍스트 속성</span><span class="sxs-lookup"><span data-stu-id="75fb1-122">Additional context properties</span></span>

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

### <span data-ttu-id="75fb1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="75fb1-123">-Force</span></span>
<span data-ttu-id="75fb1-124">기존 컨텍스트를 같은 이름으로 덮어씁니다 (있는 경우).</span><span class="sxs-lookup"><span data-stu-id="75fb1-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="75fb1-125">-이름</span><span class="sxs-lookup"><span data-stu-id="75fb1-125">-Name</span></span>
<span data-ttu-id="75fb1-126">컨텍스트의 이름</span><span class="sxs-lookup"><span data-stu-id="75fb1-126">Name of the context</span></span>

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

### <span data-ttu-id="75fb1-127">-범위</span><span class="sxs-lookup"><span data-stu-id="75fb1-127">-Scope</span></span>
<span data-ttu-id="75fb1-128">Wheher 변경 내용이 cusrrent 프로세스 또는이 사용자가 시작한 모든 세션에만 적용 되는 경우와 같이 컨텍스트 변경의 범위를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75fb1-128">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="75fb1-129">-구독</span><span class="sxs-lookup"><span data-stu-id="75fb1-129">-Subscription</span></span>
<span data-ttu-id="75fb1-130">구독 이름 또는 Id</span><span class="sxs-lookup"><span data-stu-id="75fb1-130">Subscription Name or Id</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75fb1-131">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="75fb1-131">-SubscriptionObject</span></span>
<span data-ttu-id="75fb1-132">구독 개체</span><span class="sxs-lookup"><span data-stu-id="75fb1-132">A subscription object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75fb1-133">-테 넌 트</span><span class="sxs-lookup"><span data-stu-id="75fb1-133">-Tenant</span></span>
<span data-ttu-id="75fb1-134">테 넌 트 이름 또는 ID</span><span class="sxs-lookup"><span data-stu-id="75fb1-134">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75fb1-135">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="75fb1-135">-TenantObject</span></span>
<span data-ttu-id="75fb1-136">테 넌 트 개체</span><span class="sxs-lookup"><span data-stu-id="75fb1-136">A Tenant Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureTenant
Parameter Sets: TenantObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75fb1-137">-확인</span><span class="sxs-lookup"><span data-stu-id="75fb1-137">-Confirm</span></span>
<span data-ttu-id="75fb1-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="75fb1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75fb1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75fb1-139">-WhatIf</span></span>
<span data-ttu-id="75fb1-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="75fb1-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75fb1-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75fb1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75fb1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75fb1-142">CommonParameters</span></span>
<span data-ttu-id="75fb1-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75fb1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75fb1-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75fb1-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75fb1-145">입력</span><span class="sxs-lookup"><span data-stu-id="75fb1-145">INPUTS</span></span>

### <span data-ttu-id="75fb1-146">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="75fb1-146">PSAzureContext</span></span>
<span data-ttu-id="75fb1-147">' Context ' 매개 변수는 파이프라인에서 ' PSAzureContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75fb1-147">Parameter 'Context' accepts value of type 'PSAzureContext' from the pipeline</span></span>

## <span data-ttu-id="75fb1-148">출력</span><span class="sxs-lookup"><span data-stu-id="75fb1-148">OUTPUTS</span></span>

### <span data-ttu-id="75fb1-149">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="75fb1-149">PSAzureContext</span></span>

## <span data-ttu-id="75fb1-150">상속자</span><span class="sxs-lookup"><span data-stu-id="75fb1-150">NOTES</span></span>

## <span data-ttu-id="75fb1-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75fb1-151">RELATED LINKS</span></span>

[<span data-ttu-id="75fb1-152">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="75fb1-152">Get-AzureRMContext</span></span>](./Get-AzureRMContext.md)

