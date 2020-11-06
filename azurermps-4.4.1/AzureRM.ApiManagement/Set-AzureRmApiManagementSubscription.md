---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 3b6d07577a6df05a57ed7675f5d14c847e8c33fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527744"
---
# <span data-ttu-id="b8987-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b8987-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="b8987-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8987-102">SYNOPSIS</span></span>
<span data-ttu-id="b8987-103">기존 구독 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8987-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8987-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8987-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b8987-105">DESCRIPTION</span></span>
<span data-ttu-id="b8987-106">**Set-AzureRmApiManagementSubscription** cmdlet은 기존 구독 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="b8987-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b8987-107">EXAMPLES</span></span>

### <span data-ttu-id="b8987-108">예제 1: 구독에 대 한 상태 및 기본 및 보조 키 설정</span><span class="sxs-lookup"><span data-stu-id="b8987-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SencondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="b8987-109">이 명령은 구독에 대 한 기본 및 보조 키를 설정 하 고 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="b8987-110">변수</span><span class="sxs-lookup"><span data-stu-id="b8987-110">PARAMETERS</span></span>

### <span data-ttu-id="b8987-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b8987-111">-Context</span></span>
<span data-ttu-id="b8987-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b8987-113">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="b8987-113">-ExpiresOn</span></span>
<span data-ttu-id="b8987-114">구독 만료 날짜를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-114">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="b8987-115">이 매개 변수의 기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-115">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="b8987-116">-이름</span><span class="sxs-lookup"><span data-stu-id="b8987-116">-Name</span></span>
<span data-ttu-id="b8987-117">구독 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-117">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="b8987-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8987-118">-PassThru</span></span>
<span data-ttu-id="b8987-119">passthru</span><span class="sxs-lookup"><span data-stu-id="b8987-119">passthru</span></span>

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

### <span data-ttu-id="b8987-120">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b8987-120">-PrimaryKey</span></span>
<span data-ttu-id="b8987-121">구독 기본 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-121">Specifies the subscription primary key.</span></span>
<span data-ttu-id="b8987-122">이 매개 변수는 지정 되지 않은 경우 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-122">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="b8987-123">이 매개 변수는 1 ~ 300 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-123">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="b8987-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="b8987-124">-SecondaryKey</span></span>
<span data-ttu-id="b8987-125">구독 보조 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-125">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="b8987-126">이 매개 변수는 지정 되지 않은 경우 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-126">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="b8987-127">이 매개 변수는 1 ~ 300 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="b8987-128">-상태</span><span class="sxs-lookup"><span data-stu-id="b8987-128">-State</span></span>
<span data-ttu-id="b8987-129">구독 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-129">Specifies the subscription state.</span></span>
<span data-ttu-id="b8987-130">이 매개 변수의 기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-130">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="b8987-131">-StateComment</span><span class="sxs-lookup"><span data-stu-id="b8987-131">-StateComment</span></span>
<span data-ttu-id="b8987-132">구독 상태 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-132">Specifies the subscription state comment.</span></span>
<span data-ttu-id="b8987-133">이 매개 변수의 기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="b8987-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8987-134">-SubscriptionId</span></span>
<span data-ttu-id="b8987-135">구독 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-135">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="b8987-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8987-136">-DefaultProfile</span></span>
<span data-ttu-id="b8987-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8987-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8987-138">CommonParameters</span></span>
<span data-ttu-id="b8987-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8987-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8987-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8987-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8987-141">입력</span><span class="sxs-lookup"><span data-stu-id="b8987-141">INPUTS</span></span>

## <span data-ttu-id="b8987-142">출력</span><span class="sxs-lookup"><span data-stu-id="b8987-142">OUTPUTS</span></span>

### <span data-ttu-id="b8987-143">ApiManagement. ServiceManagement. \ PsApiManagementSubscripition</span><span class="sxs-lookup"><span data-stu-id="b8987-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="b8987-144">상속자</span><span class="sxs-lookup"><span data-stu-id="b8987-144">NOTES</span></span>

## <span data-ttu-id="b8987-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8987-145">RELATED LINKS</span></span>

[<span data-ttu-id="b8987-146">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b8987-146">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="b8987-147">새로운 AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b8987-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="b8987-148">제거-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b8987-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


