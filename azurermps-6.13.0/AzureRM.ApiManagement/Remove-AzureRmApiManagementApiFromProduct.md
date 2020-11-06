---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
ms.openlocfilehash: 4bed4b5022292639a5bc55e30fdd8de356dc818a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531500"
---
# <span data-ttu-id="00ee2-101">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="00ee2-101">Remove-AzureRmApiManagementApiFromProduct</span></span>

## <span data-ttu-id="00ee2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00ee2-102">SYNOPSIS</span></span>
<span data-ttu-id="00ee2-103">제품에서 API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="00ee2-103">Removes an API from a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00ee2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00ee2-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00ee2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="00ee2-105">DESCRIPTION</span></span>
<span data-ttu-id="00ee2-106">**제거-AzureRmApiManagementApiFromProduct** cmdlet은 제품에서 Azure API Management api를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="00ee2-106">The **Remove-AzureRmApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="00ee2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="00ee2-107">EXAMPLES</span></span>

### <span data-ttu-id="00ee2-108">예제 1: 제품에서 API 제거</span><span class="sxs-lookup"><span data-stu-id="00ee2-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="00ee2-109">이 주석 nd는 제품에서 지정 된 API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="00ee2-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="00ee2-110">변수</span><span class="sxs-lookup"><span data-stu-id="00ee2-110">PARAMETERS</span></span>

### <span data-ttu-id="00ee2-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="00ee2-111">-ApiId</span></span>
<span data-ttu-id="00ee2-112">제품에서 제거할 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00ee2-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="00ee2-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="00ee2-113">-Context</span></span>
<span data-ttu-id="00ee2-114">**PsApiManagementContext** 를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00ee2-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="00ee2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ee2-115">-DefaultProfile</span></span>
<span data-ttu-id="00ee2-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00ee2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00ee2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00ee2-117">-PassThru</span></span>
<span data-ttu-id="00ee2-118">이 cmdlet이 성공 하면 $True의 값을 반환 하거나, $False 그렇지 않은 경우에는, 그렇지 않은 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="00ee2-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="00ee2-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="00ee2-119">-ProductId</span></span>
<span data-ttu-id="00ee2-120">API를 제거할 제품의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00ee2-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="00ee2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ee2-121">CommonParameters</span></span>
<span data-ttu-id="00ee2-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00ee2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ee2-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00ee2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ee2-124">입력</span><span class="sxs-lookup"><span data-stu-id="00ee2-124">INPUTS</span></span>

### <span data-ttu-id="00ee2-125">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="00ee2-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="00ee2-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="00ee2-126">System.String</span></span>

### <span data-ttu-id="00ee2-127">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="00ee2-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="00ee2-128">출력</span><span class="sxs-lookup"><span data-stu-id="00ee2-128">OUTPUTS</span></span>

### <span data-ttu-id="00ee2-129">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="00ee2-129">System.Boolean</span></span>

## <span data-ttu-id="00ee2-130">상속자</span><span class="sxs-lookup"><span data-stu-id="00ee2-130">NOTES</span></span>

## <span data-ttu-id="00ee2-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00ee2-131">RELATED LINKS</span></span>

[<span data-ttu-id="00ee2-132">추가-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="00ee2-132">Add-AzureRmApiManagementApiToProduct</span></span>](./Add-AzureRmApiManagementApiToProduct.md)


