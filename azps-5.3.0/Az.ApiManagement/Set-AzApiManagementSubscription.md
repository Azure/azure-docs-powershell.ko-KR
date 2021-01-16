---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: 82c49524566293adcd8dcbdcb36359e83360158c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381627"
---
# <span data-ttu-id="65fc6-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="65fc6-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="65fc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="65fc6-103">기존 구독 세부 정보를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="65fc6-104">구문</span><span class="sxs-lookup"><span data-stu-id="65fc6-104">SYNTAX</span></span>

### <span data-ttu-id="65fc6-105">ByInputObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="65fc6-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65fc6-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="65fc6-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65fc6-107">설명</span><span class="sxs-lookup"><span data-stu-id="65fc6-107">DESCRIPTION</span></span>
<span data-ttu-id="65fc6-108">**Set-AzApiManagementSubscription** cmdlet은 기존 구독 세부 정보를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="65fc6-109">예제</span><span class="sxs-lookup"><span data-stu-id="65fc6-109">EXAMPLES</span></span>

### <span data-ttu-id="65fc6-110">예제 1: 구독에 대한 상태 및 기본 및 보조 키 설정</span><span class="sxs-lookup"><span data-stu-id="65fc6-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="65fc6-111">이 명령은 구독에 대한 기본 및 보조 키를 설정하고 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="65fc6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65fc6-112">PARAMETERS</span></span>

### <span data-ttu-id="65fc6-113">-Context</span><span class="sxs-lookup"><span data-stu-id="65fc6-113">-Context</span></span>
<span data-ttu-id="65fc6-114">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="65fc6-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="65fc6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65fc6-115">-DefaultProfile</span></span>
<span data-ttu-id="65fc6-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65fc6-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="65fc6-117">-ExpiresOn</span></span>
<span data-ttu-id="65fc6-118">구독 만료 날짜를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="65fc6-119">이 매개 변수의 기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="65fc6-119">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="65fc6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65fc6-120">-InputObject</span></span>
<span data-ttu-id="65fc6-121">PsApiManagementSubscription의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="65fc6-122">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-122">This parameter is required.</span></span>

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

### <span data-ttu-id="65fc6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="65fc6-123">-Name</span></span>
<span data-ttu-id="65fc6-124">구독 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-124">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="65fc6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65fc6-125">-PassThru</span></span>
<span data-ttu-id="65fc6-126">passthru</span><span class="sxs-lookup"><span data-stu-id="65fc6-126">passthru</span></span>

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

### <span data-ttu-id="65fc6-127">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="65fc6-127">-PrimaryKey</span></span>
<span data-ttu-id="65fc6-128">구독 기본 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="65fc6-129">이 매개 변수는 지정되지 않은 경우 자동으로 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="65fc6-130">이 매개 변수는 1~300자 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-130">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="65fc6-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="65fc6-131">-Scope</span></span>
<span data-ttu-id="65fc6-132">구독 범위는 Api Scope /apis/{apiId} 또는 제품 범위 /products/{productId} 또는 글로벌 API 범위 /apis 또는 전역 범위 /입니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="65fc6-133">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-133">This parameter is required.</span></span>

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

### <span data-ttu-id="65fc6-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="65fc6-134">-SecondaryKey</span></span>
<span data-ttu-id="65fc6-135">구독 보조 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="65fc6-136">이 매개 변수는 지정되지 않은 경우 자동으로 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="65fc6-137">이 매개 변수는 1~300자 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-137">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="65fc6-138">-State</span><span class="sxs-lookup"><span data-stu-id="65fc6-138">-State</span></span>
<span data-ttu-id="65fc6-139">구독 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-139">Specifies the subscription state.</span></span>
<span data-ttu-id="65fc6-140">이 매개 변수의 기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="65fc6-140">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="65fc6-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="65fc6-141">-StateComment</span></span>
<span data-ttu-id="65fc6-142">구독 상태 주석을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="65fc6-143">이 매개 변수의 기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="65fc6-143">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="65fc6-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65fc6-144">-SubscriptionId</span></span>
<span data-ttu-id="65fc6-145">구독 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-145">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="65fc6-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="65fc6-146">-UserId</span></span>
<span data-ttu-id="65fc6-147">구독의 소유자입니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-147">The owner of the subscription.</span></span> <span data-ttu-id="65fc6-148">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="65fc6-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65fc6-149">-Confirm</span></span>
<span data-ttu-id="65fc6-150">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65fc6-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65fc6-151">-WhatIf</span></span>
<span data-ttu-id="65fc6-152">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="65fc6-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65fc6-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65fc6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65fc6-154">CommonParameters</span></span>
<span data-ttu-id="65fc6-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65fc6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65fc6-156">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="65fc6-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65fc6-157">입력</span><span class="sxs-lookup"><span data-stu-id="65fc6-157">INPUTS</span></span>

### <span data-ttu-id="65fc6-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="65fc6-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="65fc6-159">System.String</span><span class="sxs-lookup"><span data-stu-id="65fc6-159">System.String</span></span>

### <span data-ttu-id="65fc6-160">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="65fc6-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="65fc6-161">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="65fc6-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="65fc6-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="65fc6-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="65fc6-163">출력</span><span class="sxs-lookup"><span data-stu-id="65fc6-163">OUTPUTS</span></span>

### <span data-ttu-id="65fc6-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="65fc6-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="65fc6-165">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65fc6-165">NOTES</span></span>

## <span data-ttu-id="65fc6-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65fc6-166">RELATED LINKS</span></span>

[<span data-ttu-id="65fc6-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="65fc6-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="65fc6-168">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="65fc6-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="65fc6-169">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="65fc6-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


