---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/new-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
ms.openlocfilehash: 4e40665e4fdb7332865342132982d6d598bd8d30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181900"
---
# <span data-ttu-id="a8720-101">New-AzBotService</span><span class="sxs-lookup"><span data-stu-id="a8720-101">New-AzBotService</span></span>

## <span data-ttu-id="a8720-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8720-102">SYNOPSIS</span></span>
<span data-ttu-id="a8720-103">매개 변수로 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a8720-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="a8720-104">구문</span><span class="sxs-lookup"><span data-stu-id="a8720-104">SYNTAX</span></span>

### <span data-ttu-id="a8720-105">등록(기본값)</span><span class="sxs-lookup"><span data-stu-id="a8720-105">Registration (Default)</span></span>
```
New-AzBotService -ApplicationId <String> -Location <String> [-BotTemplateType <String>]
 [-Description <String>] [-DisplayName <String>] [-Endpoint <String>] [-Language <String>] [-Name <String>]
 [-Registration] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a8720-106">WebApp</span><span class="sxs-lookup"><span data-stu-id="a8720-106">WebApp</span></span>
```
New-AzBotService -ApplicationId <String> -ApplicationSecret <SecureString> -Location <String>
 [-BotTemplateType <String>] [-Description <String>] [-ExistingServerFarmId <String>] [-Language <String>]
 [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Webapp] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a8720-107">설명</span><span class="sxs-lookup"><span data-stu-id="a8720-107">DESCRIPTION</span></span>
<span data-ttu-id="a8720-108">매개 변수로 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a8720-108">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="a8720-109">예제</span><span class="sxs-lookup"><span data-stu-id="a8720-109">EXAMPLES</span></span>

### <span data-ttu-id="a8720-110">예제 1: 새 봇 만들기</span><span class="sxs-lookup"><span data-stu-id="a8720-110">Example 1: Create a new bot</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-bot1 -ApplicationId "af5fce4d-ee68-4b25-be09-f3222582e133"-Location eastus -Sku F0 -Description "123134" -Registration

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="a8720-111">ResourceGroupName 및 ApplicationId로 새 봇 만들기</span><span class="sxs-lookup"><span data-stu-id="a8720-111">Create a new Bot by ResourceGroupName and ApplicationId</span></span>

### <span data-ttu-id="a8720-112">예제 2: 새 웹앱 만들기</span><span class="sxs-lookup"><span data-stu-id="a8720-112">Example 2: Create a new Web App</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-apptest14 -ApplicationId "b1ab1727-0465-4255-a1bb-976210af972c" -Location eastus -Sku F0 -Description "123134" -Webapp

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest14 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="a8720-113">ResourceGroupName 및 ApplicationId로 새 웹앱 만들기</span><span class="sxs-lookup"><span data-stu-id="a8720-113">Create a new Web App by ResourceGroupName and ApplicationId</span></span>

## <span data-ttu-id="a8720-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8720-114">PARAMETERS</span></span>

### <span data-ttu-id="a8720-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a8720-115">-ApplicationId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8720-116">-ApplicationSecret</span><span class="sxs-lookup"><span data-stu-id="a8720-116">-ApplicationSecret</span></span>


```yaml
Type: System.Security.SecureString
Parameter Sets: WebApp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8720-117">-BotTemplateType</span><span class="sxs-lookup"><span data-stu-id="a8720-117">-BotTemplateType</span></span>


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

### <span data-ttu-id="a8720-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8720-118">-DefaultProfile</span></span>
<span data-ttu-id="a8720-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8720-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8720-120">-Description</span><span class="sxs-lookup"><span data-stu-id="a8720-120">-Description</span></span>


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

### <span data-ttu-id="a8720-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a8720-121">-DisplayName</span></span>


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8720-122">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="a8720-122">-Endpoint</span></span>


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8720-123">-ExistingServerFarmId</span><span class="sxs-lookup"><span data-stu-id="a8720-123">-ExistingServerFarmId</span></span>


```yaml
Type: System.String
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8720-124">-Language</span><span class="sxs-lookup"><span data-stu-id="a8720-124">-Language</span></span>


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

### <span data-ttu-id="a8720-125">-Location</span><span class="sxs-lookup"><span data-stu-id="a8720-125">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8720-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a8720-126">-Name</span></span>
<span data-ttu-id="a8720-127">봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8720-127">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8720-128">-Registration</span><span class="sxs-lookup"><span data-stu-id="a8720-128">-Registration</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8720-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8720-129">-ResourceGroupName</span></span>
<span data-ttu-id="a8720-130">사용자 구독의 봇 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8720-130">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="a8720-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="a8720-131">-Sku</span></span>
<span data-ttu-id="a8720-132">SKU 이름</span><span class="sxs-lookup"><span data-stu-id="a8720-132">The sku name</span></span>

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

### <span data-ttu-id="a8720-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8720-133">-SubscriptionId</span></span>
<span data-ttu-id="a8720-134">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a8720-134">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8720-135">-Webapp</span><span class="sxs-lookup"><span data-stu-id="a8720-135">-Webapp</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8720-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8720-136">CommonParameters</span></span>
<span data-ttu-id="a8720-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a8720-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8720-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a8720-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8720-139">입력</span><span class="sxs-lookup"><span data-stu-id="a8720-139">INPUTS</span></span>

## <span data-ttu-id="a8720-140">출력</span><span class="sxs-lookup"><span data-stu-id="a8720-140">OUTPUTS</span></span>

### <span data-ttu-id="a8720-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="a8720-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="a8720-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a8720-142">NOTES</span></span>

<span data-ttu-id="a8720-143">별칭</span><span class="sxs-lookup"><span data-stu-id="a8720-143">ALIASES</span></span>

## <span data-ttu-id="a8720-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8720-144">RELATED LINKS</span></span>

