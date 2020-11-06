---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 5c5bd7d0b7df385645bdb51d684616f2c0d7eaa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525396"
---
# <span data-ttu-id="42557-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="42557-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="42557-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42557-102">SYNOPSIS</span></span>
<span data-ttu-id="42557-103">기존 API 관리 제품을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="42557-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42557-104">구문과</span><span class="sxs-lookup"><span data-stu-id="42557-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42557-105">설명은</span><span class="sxs-lookup"><span data-stu-id="42557-105">DESCRIPTION</span></span>
<span data-ttu-id="42557-106">**AzureRmApiManagementProduct** cmdlet에서는 기존 API Management 제품을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="42557-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="42557-107">예제의</span><span class="sxs-lookup"><span data-stu-id="42557-107">EXAMPLES</span></span>

### <span data-ttu-id="42557-108">예제 1: 기존 제품 및 모든 구독 제거</span><span class="sxs-lookup"><span data-stu-id="42557-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProduct -Context $apimContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="42557-109">이 명령은 기존 제품 및 모든 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="42557-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="42557-110">변수</span><span class="sxs-lookup"><span data-stu-id="42557-110">PARAMETERS</span></span>

### <span data-ttu-id="42557-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="42557-111">-Context</span></span>
<span data-ttu-id="42557-112">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42557-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42557-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42557-113">-DefaultProfile</span></span>
<span data-ttu-id="42557-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42557-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42557-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="42557-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="42557-116">제품에 대 한 구독을 삭제할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="42557-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="42557-117">이 매개 변수를 설정 하지 않으면 구독이 존재 하는 경우 예외가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="42557-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42557-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42557-118">-PassThru</span></span>
<span data-ttu-id="42557-119">이 cmdlet이 $True에 대 한 값을 반환 하거나, 성공할 경우, 오류가 발생 한 경우 $False 값을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="42557-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42557-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="42557-120">-ProductId</span></span>
<span data-ttu-id="42557-121">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42557-121">Specifies the identifier of the existing product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42557-122">-확인</span><span class="sxs-lookup"><span data-stu-id="42557-122">-Confirm</span></span>
<span data-ttu-id="42557-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="42557-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42557-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42557-124">-WhatIf</span></span>
<span data-ttu-id="42557-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="42557-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42557-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42557-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42557-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42557-127">CommonParameters</span></span>
<span data-ttu-id="42557-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="42557-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42557-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42557-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42557-130">입력</span><span class="sxs-lookup"><span data-stu-id="42557-130">INPUTS</span></span>

### <span data-ttu-id="42557-131">않아야</span><span class="sxs-lookup"><span data-stu-id="42557-131">None</span></span>
<span data-ttu-id="42557-132">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42557-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42557-133">출력</span><span class="sxs-lookup"><span data-stu-id="42557-133">OUTPUTS</span></span>

### <span data-ttu-id="42557-134">부울</span><span class="sxs-lookup"><span data-stu-id="42557-134">bool</span></span>

## <span data-ttu-id="42557-135">상속자</span><span class="sxs-lookup"><span data-stu-id="42557-135">NOTES</span></span>

## <span data-ttu-id="42557-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42557-136">RELATED LINKS</span></span>

[<span data-ttu-id="42557-137">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="42557-137">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="42557-138">새로운 AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="42557-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="42557-139">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="42557-139">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


