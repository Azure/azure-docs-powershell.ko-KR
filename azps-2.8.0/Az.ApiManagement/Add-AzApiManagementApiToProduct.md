---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: 8676a90e533217fe291e47fce40ffbd43929031a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698146"
---
# <span data-ttu-id="cca01-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="cca01-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="cca01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cca01-102">SYNOPSIS</span></span>
<span data-ttu-id="cca01-103">제품에 API를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cca01-103">Adds an API to a product.</span></span>

## <span data-ttu-id="cca01-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cca01-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cca01-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cca01-105">DESCRIPTION</span></span>
<span data-ttu-id="cca01-106">**Add-AzApiManagementApiToProduct** cmdlet은 제품에 Azure API Management api를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cca01-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="cca01-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cca01-107">EXAMPLES</span></span>

### <span data-ttu-id="cca01-108">예제 1: 제품에 API 추가</span><span class="sxs-lookup"><span data-stu-id="cca01-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="cca01-109">이 명령은 지정 된 제품에 지정한 API를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cca01-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="cca01-110">변수</span><span class="sxs-lookup"><span data-stu-id="cca01-110">PARAMETERS</span></span>

### <span data-ttu-id="cca01-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cca01-111">-ApiId</span></span>
<span data-ttu-id="cca01-112">제품에 추가할 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cca01-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="cca01-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="cca01-113">-Context</span></span>
<span data-ttu-id="cca01-114">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cca01-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cca01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca01-115">-DefaultProfile</span></span>
<span data-ttu-id="cca01-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cca01-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cca01-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cca01-117">-PassThru</span></span>
<span data-ttu-id="cca01-118">passthru</span><span class="sxs-lookup"><span data-stu-id="cca01-118">passthru</span></span>

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

### <span data-ttu-id="cca01-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="cca01-119">-ProductId</span></span>
<span data-ttu-id="cca01-120">API를 추가할 제품의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cca01-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="cca01-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca01-121">CommonParameters</span></span>
<span data-ttu-id="cca01-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cca01-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca01-123">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cca01-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca01-124">입력</span><span class="sxs-lookup"><span data-stu-id="cca01-124">INPUTS</span></span>

### <span data-ttu-id="cca01-125">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cca01-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cca01-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cca01-126">System.String</span></span>

### <span data-ttu-id="cca01-127">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cca01-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cca01-128">출력</span><span class="sxs-lookup"><span data-stu-id="cca01-128">OUTPUTS</span></span>

### <span data-ttu-id="cca01-129">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="cca01-129">System.Boolean</span></span>

## <span data-ttu-id="cca01-130">상속자</span><span class="sxs-lookup"><span data-stu-id="cca01-130">NOTES</span></span>

## <span data-ttu-id="cca01-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cca01-131">RELATED LINKS</span></span>

[<span data-ttu-id="cca01-132">제거-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="cca01-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)


