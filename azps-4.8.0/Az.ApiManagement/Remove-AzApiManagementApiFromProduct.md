---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: fd9e4cec821b08c9ac2bbd5cd2ac43e5e5b114ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213750"
---
# <span data-ttu-id="cc263-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="cc263-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="cc263-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc263-102">SYNOPSIS</span></span>
<span data-ttu-id="cc263-103">제품에서 API를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc263-103">Removes an API from a product.</span></span>

## <span data-ttu-id="cc263-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cc263-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc263-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cc263-105">DESCRIPTION</span></span>
<span data-ttu-id="cc263-106">**제거-AzApiManagementApiFromProduct** cmdlet은 제품에서 Azure API Management api를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc263-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="cc263-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cc263-107">EXAMPLES</span></span>

### <span data-ttu-id="cc263-108">예제 1: 제품에서 API 제거</span><span class="sxs-lookup"><span data-stu-id="cc263-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="cc263-109">이 명령은 지정 된 API를 제품에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc263-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="cc263-110">변수</span><span class="sxs-lookup"><span data-stu-id="cc263-110">PARAMETERS</span></span>

### <span data-ttu-id="cc263-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cc263-111">-ApiId</span></span>
<span data-ttu-id="cc263-112">제품에서 제거할 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc263-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="cc263-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="cc263-113">-Context</span></span>
<span data-ttu-id="cc263-114">**PsApiManagementContext** 를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc263-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="cc263-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc263-115">-DefaultProfile</span></span>
<span data-ttu-id="cc263-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc263-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc263-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc263-117">-PassThru</span></span>
<span data-ttu-id="cc263-118">이 cmdlet이 성공 하면 $True의 값을 반환 하거나, $False 그렇지 않은 경우에는, 그렇지 않은 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cc263-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="cc263-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="cc263-119">-ProductId</span></span>
<span data-ttu-id="cc263-120">API를 제거할 제품의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc263-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="cc263-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc263-121">CommonParameters</span></span>
<span data-ttu-id="cc263-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc263-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc263-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cc263-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc263-124">입력</span><span class="sxs-lookup"><span data-stu-id="cc263-124">INPUTS</span></span>

### <span data-ttu-id="cc263-125">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cc263-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cc263-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cc263-126">System.String</span></span>

### <span data-ttu-id="cc263-127">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cc263-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cc263-128">출력</span><span class="sxs-lookup"><span data-stu-id="cc263-128">OUTPUTS</span></span>

### <span data-ttu-id="cc263-129">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="cc263-129">System.Boolean</span></span>

## <span data-ttu-id="cc263-130">상속자</span><span class="sxs-lookup"><span data-stu-id="cc263-130">NOTES</span></span>

## <span data-ttu-id="cc263-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc263-131">RELATED LINKS</span></span>

[<span data-ttu-id="cc263-132">추가-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="cc263-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


