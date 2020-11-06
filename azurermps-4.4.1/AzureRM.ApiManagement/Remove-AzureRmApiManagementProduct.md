---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 505a26c48e53fe05e8724d61d5ddb66981e87ee9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525775"
---
# <span data-ttu-id="d9bf3-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d9bf3-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="d9bf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bf3-103">기존 API 관리 제품을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9bf3-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9bf3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d9bf3-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9bf3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d9bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="d9bf3-106">**AzureRmApiManagementProduct** cmdlet에서는 기존 API Management 제품을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9bf3-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="d9bf3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d9bf3-107">EXAMPLES</span></span>

### <span data-ttu-id="d9bf3-108">예제 1: 기존 제품 및 모든 구독 제거</span><span class="sxs-lookup"><span data-stu-id="d9bf3-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>Remove-AzureRmApiManagementProduct -Context $APImContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="d9bf3-109">이 명령은 기존 제품 및 모든 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9bf3-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="d9bf3-110">변수</span><span class="sxs-lookup"><span data-stu-id="d9bf3-110">PARAMETERS</span></span>

### <span data-ttu-id="d9bf3-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d9bf3-111">-Context</span></span>
<span data-ttu-id="d9bf3-112">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9bf3-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d9bf3-113">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="d9bf3-113">-DeleteSubscriptions</span></span>
<span data-ttu-id="d9bf3-114">제품에 대 한 구독을 삭제할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d9bf3-114">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="d9bf3-115">이 매개 변수를 설정 하지 않으면 구독이 존재 하는 경우 예외가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9bf3-115">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="d9bf3-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9bf3-116">-PassThru</span></span>
<span data-ttu-id="d9bf3-117">이 cmdlet이 $True에 대 한 값을 반환 하거나, 성공할 경우, 오류가 발생 한 경우 $False 값을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d9bf3-117">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="d9bf3-118">-ProductId</span><span class="sxs-lookup"><span data-stu-id="d9bf3-118">-ProductId</span></span>
<span data-ttu-id="d9bf3-119">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9bf3-119">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="d9bf3-120">-확인</span><span class="sxs-lookup"><span data-stu-id="d9bf3-120">-Confirm</span></span>
<span data-ttu-id="d9bf3-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9bf3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9bf3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9bf3-122">-WhatIf</span></span>
<span data-ttu-id="d9bf3-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d9bf3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9bf3-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9bf3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9bf3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bf3-125">-DefaultProfile</span></span>
<span data-ttu-id="d9bf3-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9bf3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9bf3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bf3-127">CommonParameters</span></span>
<span data-ttu-id="d9bf3-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9bf3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9bf3-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9bf3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bf3-130">입력</span><span class="sxs-lookup"><span data-stu-id="d9bf3-130">INPUTS</span></span>

## <span data-ttu-id="d9bf3-131">출력</span><span class="sxs-lookup"><span data-stu-id="d9bf3-131">OUTPUTS</span></span>

### <span data-ttu-id="d9bf3-132">부울</span><span class="sxs-lookup"><span data-stu-id="d9bf3-132">bool</span></span>

## <span data-ttu-id="d9bf3-133">상속자</span><span class="sxs-lookup"><span data-stu-id="d9bf3-133">NOTES</span></span>

## <span data-ttu-id="d9bf3-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9bf3-134">RELATED LINKS</span></span>

[<span data-ttu-id="d9bf3-135">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d9bf3-135">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="d9bf3-136">새로운 AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d9bf3-136">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="d9bf3-137">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d9bf3-137">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)

