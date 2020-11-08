---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: 82c49524566293adcd8dcbdcb36359e83360158c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226439"
---
# <span data-ttu-id="20925-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="20925-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="20925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20925-102">SYNOPSIS</span></span>
<span data-ttu-id="20925-103">기존 구독 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20925-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="20925-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20925-104">SYNTAX</span></span>

### <span data-ttu-id="20925-105">ByInputObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="20925-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20925-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="20925-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20925-107">설명은</span><span class="sxs-lookup"><span data-stu-id="20925-107">DESCRIPTION</span></span>
<span data-ttu-id="20925-108">**Set-AzApiManagementSubscription** cmdlet은 기존 구독 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20925-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="20925-109">예제의</span><span class="sxs-lookup"><span data-stu-id="20925-109">EXAMPLES</span></span>

### <span data-ttu-id="20925-110">예제 1: 구독에 대 한 상태 및 기본 및 보조 키 설정</span><span class="sxs-lookup"><span data-stu-id="20925-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="20925-111">이 명령은 구독에 대 한 기본 및 보조 키를 설정 하 고 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="20925-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="20925-112">변수</span><span class="sxs-lookup"><span data-stu-id="20925-112">PARAMETERS</span></span>

### <span data-ttu-id="20925-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="20925-113">-Context</span></span>
<span data-ttu-id="20925-114">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20925-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20925-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20925-115">-DefaultProfile</span></span>
<span data-ttu-id="20925-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20925-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20925-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="20925-117">-ExpiresOn</span></span>
<span data-ttu-id="20925-118">구독 만료 날짜를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20925-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="20925-119">이 매개 변수의 기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="20925-119">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20925-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20925-120">-InputObject</span></span>
<span data-ttu-id="20925-121">PsApiManagementSubscription의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="20925-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="20925-122">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="20925-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20925-123">-이름</span><span class="sxs-lookup"><span data-stu-id="20925-123">-Name</span></span>
<span data-ttu-id="20925-124">구독 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20925-124">Specifies a subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20925-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20925-125">-PassThru</span></span>
<span data-ttu-id="20925-126">passthru</span><span class="sxs-lookup"><span data-stu-id="20925-126">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20925-127">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="20925-127">-PrimaryKey</span></span>
<span data-ttu-id="20925-128">구독 기본 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20925-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="20925-129">이 매개 변수는 지정 되지 않은 경우 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20925-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="20925-130">이 매개 변수는 1 ~ 300 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20925-130">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20925-131">-범위</span><span class="sxs-lookup"><span data-stu-id="20925-131">-Scope</span></span>
<span data-ttu-id="20925-132">Api 범위/Apis/{apiid} 또는 Product Scope/products/{productId} 또는 전역 범위/전역 scope/api 인지 여부에 관계 없이 구독의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="20925-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="20925-133">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="20925-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20925-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="20925-134">-SecondaryKey</span></span>
<span data-ttu-id="20925-135">구독 보조 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20925-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="20925-136">이 매개 변수는 지정 되지 않은 경우 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20925-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="20925-137">이 매개 변수는 1 ~ 300 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20925-137">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20925-138">-상태</span><span class="sxs-lookup"><span data-stu-id="20925-138">-State</span></span>
<span data-ttu-id="20925-139">구독 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20925-139">Specifies the subscription state.</span></span>
<span data-ttu-id="20925-140">이 매개 변수의 기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="20925-140">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20925-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="20925-141">-StateComment</span></span>
<span data-ttu-id="20925-142">구독 상태 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20925-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="20925-143">이 매개 변수의 기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="20925-143">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20925-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20925-144">-SubscriptionId</span></span>
<span data-ttu-id="20925-145">구독 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20925-145">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20925-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="20925-146">-UserId</span></span>
<span data-ttu-id="20925-147">구독 소유자입니다.</span><span class="sxs-lookup"><span data-stu-id="20925-147">The owner of the subscription.</span></span> <span data-ttu-id="20925-148">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="20925-148">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20925-149">-확인</span><span class="sxs-lookup"><span data-stu-id="20925-149">-Confirm</span></span>
<span data-ttu-id="20925-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="20925-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20925-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20925-151">-WhatIf</span></span>
<span data-ttu-id="20925-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="20925-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20925-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20925-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20925-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20925-154">CommonParameters</span></span>
<span data-ttu-id="20925-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20925-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20925-156">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="20925-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20925-157">입력</span><span class="sxs-lookup"><span data-stu-id="20925-157">INPUTS</span></span>

### <span data-ttu-id="20925-158">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="20925-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="20925-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="20925-159">System.String</span></span>

### <span data-ttu-id="20925-160">시스템 Null 허용 ' 1 [[ApiManagement]. ServiceManagement, PsApiManagementSubscriptionState, Microsoft azure. PowerShell. ApiManagement, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="20925-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="20925-161">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="20925-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="20925-162">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="20925-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="20925-163">출력</span><span class="sxs-lookup"><span data-stu-id="20925-163">OUTPUTS</span></span>

### <span data-ttu-id="20925-164">ApiManagement. ServiceManagement. \ PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="20925-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="20925-165">상속자</span><span class="sxs-lookup"><span data-stu-id="20925-165">NOTES</span></span>

## <span data-ttu-id="20925-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20925-166">RELATED LINKS</span></span>

[<span data-ttu-id="20925-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="20925-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="20925-168">새로운 AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="20925-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="20925-169">제거-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="20925-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


