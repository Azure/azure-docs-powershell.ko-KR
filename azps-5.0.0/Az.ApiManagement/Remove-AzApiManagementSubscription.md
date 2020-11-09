---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 8c6bc7a9e29d6f187285cacdc9df3621fcba8d0f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309726"
---
# <span data-ttu-id="02365-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="02365-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="02365-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02365-102">SYNOPSIS</span></span>
<span data-ttu-id="02365-103">기존 구독을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="02365-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="02365-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02365-104">SYNTAX</span></span>

### <span data-ttu-id="02365-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="02365-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02365-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="02365-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02365-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="02365-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02365-108">설명은</span><span class="sxs-lookup"><span data-stu-id="02365-108">DESCRIPTION</span></span>
<span data-ttu-id="02365-109">**제거-AzApiManagementSubscription** cmdlet은 기존 구독을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="02365-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="02365-110">예제의</span><span class="sxs-lookup"><span data-stu-id="02365-110">EXAMPLES</span></span>

### <span data-ttu-id="02365-111">예제 1: 구독 삭제</span><span class="sxs-lookup"><span data-stu-id="02365-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="02365-112">이 명령은 기존 구독을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="02365-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="02365-113">변수</span><span class="sxs-lookup"><span data-stu-id="02365-113">PARAMETERS</span></span>

### <span data-ttu-id="02365-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="02365-114">-Context</span></span>
<span data-ttu-id="02365-115">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02365-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02365-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02365-116">-DefaultProfile</span></span>
<span data-ttu-id="02365-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02365-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02365-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02365-118">-InputObject</span></span>
<span data-ttu-id="02365-119">PsApiManagementSubscription의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="02365-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="02365-120">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="02365-120">This parameter is required.</span></span>

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

### <span data-ttu-id="02365-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02365-121">-PassThru</span></span>
<span data-ttu-id="02365-122">이 cmdlet이 $True 값을 반환 하거나, 성공할 경우, $false의 값이 반환 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="02365-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="02365-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02365-123">-ResourceId</span></span>
<span data-ttu-id="02365-124">구독의 팔 인 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="02365-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="02365-125">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="02365-125">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02365-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02365-126">-SubscriptionId</span></span>
<span data-ttu-id="02365-127">구독 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02365-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="02365-128">-확인</span><span class="sxs-lookup"><span data-stu-id="02365-128">-Confirm</span></span>
<span data-ttu-id="02365-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="02365-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02365-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02365-130">-WhatIf</span></span>
<span data-ttu-id="02365-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="02365-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02365-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02365-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02365-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02365-133">CommonParameters</span></span>
<span data-ttu-id="02365-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02365-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02365-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="02365-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02365-136">입력</span><span class="sxs-lookup"><span data-stu-id="02365-136">INPUTS</span></span>

### <span data-ttu-id="02365-137">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="02365-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="02365-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="02365-138">System.String</span></span>

### <span data-ttu-id="02365-139">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="02365-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="02365-140">출력</span><span class="sxs-lookup"><span data-stu-id="02365-140">OUTPUTS</span></span>

### <span data-ttu-id="02365-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="02365-141">System.Boolean</span></span>

## <span data-ttu-id="02365-142">상속자</span><span class="sxs-lookup"><span data-stu-id="02365-142">NOTES</span></span>

## <span data-ttu-id="02365-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02365-143">RELATED LINKS</span></span>

[<span data-ttu-id="02365-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="02365-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="02365-145">새로운 AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="02365-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="02365-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="02365-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


