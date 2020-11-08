---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 33b00df9e0c9c5b5e0ef04d22b745942535effcb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056576"
---
# <span data-ttu-id="3cb97-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3cb97-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="3cb97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cb97-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb97-103">기존 API 관리 제품을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb97-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="3cb97-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3cb97-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cb97-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3cb97-105">DESCRIPTION</span></span>
<span data-ttu-id="3cb97-106">**AzApiManagementProduct** cmdlet에서는 기존 API Management 제품을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb97-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="3cb97-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3cb97-107">EXAMPLES</span></span>

### <span data-ttu-id="3cb97-108">예제 1: 기존 제품 및 모든 구독 제거</span><span class="sxs-lookup"><span data-stu-id="3cb97-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="3cb97-109">이 명령은 기존 제품 및 모든 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb97-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="3cb97-110">변수</span><span class="sxs-lookup"><span data-stu-id="3cb97-110">PARAMETERS</span></span>

### <span data-ttu-id="3cb97-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="3cb97-111">-Context</span></span>
<span data-ttu-id="3cb97-112">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb97-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3cb97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb97-113">-DefaultProfile</span></span>
<span data-ttu-id="3cb97-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb97-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cb97-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="3cb97-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="3cb97-116">제품에 대 한 구독을 삭제할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3cb97-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="3cb97-117">이 매개 변수를 설정 하지 않으면 구독이 존재 하는 경우 예외가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb97-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="3cb97-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cb97-118">-PassThru</span></span>
<span data-ttu-id="3cb97-119">이 cmdlet이 $True에 대 한 값을 반환 하거나, 성공할 경우, 오류가 발생 한 경우 $False 값을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3cb97-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="3cb97-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="3cb97-120">-ProductId</span></span>
<span data-ttu-id="3cb97-121">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb97-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="3cb97-122">-확인</span><span class="sxs-lookup"><span data-stu-id="3cb97-122">-Confirm</span></span>
<span data-ttu-id="3cb97-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb97-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cb97-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cb97-124">-WhatIf</span></span>
<span data-ttu-id="3cb97-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3cb97-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cb97-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3cb97-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cb97-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb97-127">CommonParameters</span></span>
<span data-ttu-id="3cb97-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb97-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb97-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3cb97-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb97-130">입력</span><span class="sxs-lookup"><span data-stu-id="3cb97-130">INPUTS</span></span>

### <span data-ttu-id="3cb97-131">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3cb97-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3cb97-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3cb97-132">System.String</span></span>

### <span data-ttu-id="3cb97-133">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="3cb97-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3cb97-134">출력</span><span class="sxs-lookup"><span data-stu-id="3cb97-134">OUTPUTS</span></span>

### <span data-ttu-id="3cb97-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="3cb97-135">System.Boolean</span></span>

## <span data-ttu-id="3cb97-136">상속자</span><span class="sxs-lookup"><span data-stu-id="3cb97-136">NOTES</span></span>

## <span data-ttu-id="3cb97-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3cb97-137">RELATED LINKS</span></span>

[<span data-ttu-id="3cb97-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3cb97-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="3cb97-139">새로운 AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3cb97-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="3cb97-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3cb97-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


