---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: d5c9061921f6ab345a027eeec69b4d6cd7230211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703415"
---
# <span data-ttu-id="8e5bd-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="8e5bd-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="8e5bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e5bd-102">SYNOPSIS</span></span>
<span data-ttu-id="8e5bd-103">제품에 API를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e5bd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e5bd-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e5bd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8e5bd-105">DESCRIPTION</span></span>
<span data-ttu-id="8e5bd-106">**Add-AzureRmApiManagementApiToProduct** cmdlet은 제품에 Azure API Management api를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="8e5bd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8e5bd-107">EXAMPLES</span></span>

### <span data-ttu-id="8e5bd-108">예제 1: 제품에 API 추가</span><span class="sxs-lookup"><span data-stu-id="8e5bd-108">Example 1: Add an API to a product</span></span>
```
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="8e5bd-109">이 명령은 지정 된 제품에 지정한 API를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="8e5bd-110">변수</span><span class="sxs-lookup"><span data-stu-id="8e5bd-110">PARAMETERS</span></span>

### <span data-ttu-id="8e5bd-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8e5bd-111">-ApiId</span></span>
<span data-ttu-id="8e5bd-112">제품에 추가할 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="8e5bd-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="8e5bd-113">-Context</span></span>
<span data-ttu-id="8e5bd-114">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8e5bd-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e5bd-115">-PassThru</span></span>
<span data-ttu-id="8e5bd-116">passthru</span><span class="sxs-lookup"><span data-stu-id="8e5bd-116">passthru</span></span>

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

### <span data-ttu-id="8e5bd-117">-ProductId</span><span class="sxs-lookup"><span data-stu-id="8e5bd-117">-ProductId</span></span>
<span data-ttu-id="8e5bd-118">API를 추가할 제품의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-118">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="8e5bd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e5bd-119">-DefaultProfile</span></span>
<span data-ttu-id="8e5bd-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e5bd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e5bd-121">CommonParameters</span></span>
<span data-ttu-id="8e5bd-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e5bd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e5bd-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e5bd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e5bd-124">입력</span><span class="sxs-lookup"><span data-stu-id="8e5bd-124">INPUTS</span></span>

## <span data-ttu-id="8e5bd-125">출력</span><span class="sxs-lookup"><span data-stu-id="8e5bd-125">OUTPUTS</span></span>

### <span data-ttu-id="8e5bd-126">나타내는</span><span class="sxs-lookup"><span data-stu-id="8e5bd-126">Boolean</span></span>

## <span data-ttu-id="8e5bd-127">상속자</span><span class="sxs-lookup"><span data-stu-id="8e5bd-127">NOTES</span></span>

## <span data-ttu-id="8e5bd-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e5bd-128">RELATED LINKS</span></span>

[<span data-ttu-id="8e5bd-129">제거-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="8e5bd-129">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


