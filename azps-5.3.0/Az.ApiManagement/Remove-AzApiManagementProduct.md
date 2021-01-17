---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 33b00df9e0c9c5b5e0ef04d22b745942535effcb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381984"
---
# <span data-ttu-id="876f5-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="876f5-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="876f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="876f5-102">SYNOPSIS</span></span>
<span data-ttu-id="876f5-103">기존 API Management 제품을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="876f5-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="876f5-104">구문</span><span class="sxs-lookup"><span data-stu-id="876f5-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="876f5-105">설명</span><span class="sxs-lookup"><span data-stu-id="876f5-105">DESCRIPTION</span></span>
<span data-ttu-id="876f5-106">**Remove-AzApiManagementProduct** cmdlet은 기존 API Management 제품을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="876f5-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="876f5-107">예제</span><span class="sxs-lookup"><span data-stu-id="876f5-107">EXAMPLES</span></span>

### <span data-ttu-id="876f5-108">예제 1: 기존 제품 및 모든 구독 제거</span><span class="sxs-lookup"><span data-stu-id="876f5-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="876f5-109">이 명령은 기존 제품 및 모든 구독을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="876f5-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="876f5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="876f5-110">PARAMETERS</span></span>

### <span data-ttu-id="876f5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="876f5-111">-Context</span></span>
<span data-ttu-id="876f5-112">**PsApiManagementContext** 개체의 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="876f5-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="876f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="876f5-113">-DefaultProfile</span></span>
<span data-ttu-id="876f5-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="876f5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="876f5-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="876f5-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="876f5-116">제품에 대한 구독을 삭제할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="876f5-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="876f5-117">이 매개 변수를 설정하지 않은 경우 구독이 있으면 예외가 throw됩니다.</span><span class="sxs-lookup"><span data-stu-id="876f5-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="876f5-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="876f5-118">-PassThru</span></span>
<span data-ttu-id="876f5-119">이 cmdlet이 성공하는 경우 $True, 실패하는 경우 $False 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="876f5-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="876f5-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="876f5-120">-ProductId</span></span>
<span data-ttu-id="876f5-121">기존 제품의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="876f5-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="876f5-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="876f5-122">-Confirm</span></span>
<span data-ttu-id="876f5-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="876f5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="876f5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="876f5-124">-WhatIf</span></span>
<span data-ttu-id="876f5-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="876f5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="876f5-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="876f5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="876f5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="876f5-127">CommonParameters</span></span>
<span data-ttu-id="876f5-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="876f5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="876f5-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="876f5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="876f5-130">입력</span><span class="sxs-lookup"><span data-stu-id="876f5-130">INPUTS</span></span>

### <span data-ttu-id="876f5-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="876f5-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="876f5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="876f5-132">System.String</span></span>

### <span data-ttu-id="876f5-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="876f5-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="876f5-134">출력</span><span class="sxs-lookup"><span data-stu-id="876f5-134">OUTPUTS</span></span>

### <span data-ttu-id="876f5-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="876f5-135">System.Boolean</span></span>

## <span data-ttu-id="876f5-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="876f5-136">NOTES</span></span>

## <span data-ttu-id="876f5-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="876f5-137">RELATED LINKS</span></span>

[<span data-ttu-id="876f5-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="876f5-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="876f5-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="876f5-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="876f5-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="876f5-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


