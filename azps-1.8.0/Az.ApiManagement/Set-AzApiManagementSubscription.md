---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: cbdc876368f55ace6f77c04172dc2f0a53b0a7f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701666"
---
# <span data-ttu-id="80e41-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="80e41-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="80e41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80e41-102">SYNOPSIS</span></span>
<span data-ttu-id="80e41-103">기존 구독 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="80e41-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80e41-104">SYNTAX</span></span>

```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Name <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80e41-105">설명은</span><span class="sxs-lookup"><span data-stu-id="80e41-105">DESCRIPTION</span></span>
<span data-ttu-id="80e41-106">**Set-AzApiManagementSubscription** cmdlet은 기존 구독 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-106">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="80e41-107">예제의</span><span class="sxs-lookup"><span data-stu-id="80e41-107">EXAMPLES</span></span>

### <span data-ttu-id="80e41-108">예제 1: 구독에 대 한 상태 및 기본 및 보조 키 설정</span><span class="sxs-lookup"><span data-stu-id="80e41-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="80e41-109">이 명령은 구독에 대 한 기본 및 보조 키를 설정 하 고 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="80e41-110">변수</span><span class="sxs-lookup"><span data-stu-id="80e41-110">PARAMETERS</span></span>

### <span data-ttu-id="80e41-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="80e41-111">-Context</span></span>
<span data-ttu-id="80e41-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80e41-113">-DefaultProfile</span></span>
<span data-ttu-id="80e41-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80e41-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="80e41-115">-ExpiresOn</span></span>
<span data-ttu-id="80e41-116">구독 만료 날짜를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="80e41-117">이 매개 변수의 기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-117">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="80e41-118">-이름</span><span class="sxs-lookup"><span data-stu-id="80e41-118">-Name</span></span>
<span data-ttu-id="80e41-119">구독 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="80e41-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80e41-120">-PassThru</span></span>
<span data-ttu-id="80e41-121">passthru</span><span class="sxs-lookup"><span data-stu-id="80e41-121">passthru</span></span>

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

### <span data-ttu-id="80e41-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="80e41-122">-PrimaryKey</span></span>
<span data-ttu-id="80e41-123">구독 기본 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="80e41-124">이 매개 변수는 지정 되지 않은 경우 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="80e41-125">이 매개 변수는 1 ~ 300 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="80e41-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="80e41-126">-SecondaryKey</span></span>
<span data-ttu-id="80e41-127">구독 보조 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="80e41-128">이 매개 변수는 지정 되지 않은 경우 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="80e41-129">이 매개 변수는 1 ~ 300 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="80e41-130">-상태</span><span class="sxs-lookup"><span data-stu-id="80e41-130">-State</span></span>
<span data-ttu-id="80e41-131">구독 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-131">Specifies the subscription state.</span></span>
<span data-ttu-id="80e41-132">이 매개 변수의 기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="80e41-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="80e41-133">-StateComment</span></span>
<span data-ttu-id="80e41-134">구독 상태 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="80e41-135">이 매개 변수의 기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="80e41-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80e41-136">-SubscriptionId</span></span>
<span data-ttu-id="80e41-137">구독 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-137">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e41-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80e41-138">CommonParameters</span></span>
<span data-ttu-id="80e41-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80e41-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80e41-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80e41-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80e41-141">입력</span><span class="sxs-lookup"><span data-stu-id="80e41-141">INPUTS</span></span>

### <span data-ttu-id="80e41-142">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="80e41-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="80e41-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="80e41-143">System.String</span></span>

### <span data-ttu-id="80e41-144">시스템 Null 허용 ' 1 [[ApiManagement]. ServiceManagement, PsApiManagementSubscriptionState, Microsoft azure. PowerShell. ApiManagement, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="80e41-144">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="80e41-145">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="80e41-145">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="80e41-146">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="80e41-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="80e41-147">출력</span><span class="sxs-lookup"><span data-stu-id="80e41-147">OUTPUTS</span></span>

### <span data-ttu-id="80e41-148">ApiManagement. ServiceManagement. \ PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="80e41-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="80e41-149">상속자</span><span class="sxs-lookup"><span data-stu-id="80e41-149">NOTES</span></span>

## <span data-ttu-id="80e41-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80e41-150">RELATED LINKS</span></span>

[<span data-ttu-id="80e41-151">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="80e41-151">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="80e41-152">새로운 AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="80e41-152">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="80e41-153">제거-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="80e41-153">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


