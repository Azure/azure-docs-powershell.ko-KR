---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: fd9e4cec821b08c9ac2bbd5cd2ac43e5e5b114ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358366"
---
# <span data-ttu-id="896fd-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="896fd-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="896fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="896fd-102">SYNOPSIS</span></span>
<span data-ttu-id="896fd-103">제품에서 API를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="896fd-103">Removes an API from a product.</span></span>

## <span data-ttu-id="896fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="896fd-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="896fd-105">설명</span><span class="sxs-lookup"><span data-stu-id="896fd-105">DESCRIPTION</span></span>
<span data-ttu-id="896fd-106">**Remove-AzApiManagementApiFromProduct** cmdlet은 제품에서 Azure API Management API를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="896fd-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="896fd-107">예제</span><span class="sxs-lookup"><span data-stu-id="896fd-107">EXAMPLES</span></span>

### <span data-ttu-id="896fd-108">예제 1: 제품에서 API 제거</span><span class="sxs-lookup"><span data-stu-id="896fd-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="896fd-109">이 명령은 제품에서 지정된 API를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="896fd-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="896fd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="896fd-110">PARAMETERS</span></span>

### <span data-ttu-id="896fd-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="896fd-111">-ApiId</span></span>
<span data-ttu-id="896fd-112">제품에서 제거할 API의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="896fd-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="896fd-113">-Context</span><span class="sxs-lookup"><span data-stu-id="896fd-113">-Context</span></span>
<span data-ttu-id="896fd-114">**PsApiManagementContext를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="896fd-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="896fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="896fd-115">-DefaultProfile</span></span>
<span data-ttu-id="896fd-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="896fd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="896fd-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="896fd-117">-PassThru</span></span>
<span data-ttu-id="896fd-118">이 cmdlet이 성공하는 경우 $True, 그렇지 않은 경우 $False 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="896fd-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="896fd-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="896fd-119">-ProductId</span></span>
<span data-ttu-id="896fd-120">API를 제거할 제품의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="896fd-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="896fd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="896fd-121">CommonParameters</span></span>
<span data-ttu-id="896fd-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="896fd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="896fd-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="896fd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="896fd-124">입력</span><span class="sxs-lookup"><span data-stu-id="896fd-124">INPUTS</span></span>

### <span data-ttu-id="896fd-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="896fd-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="896fd-126">System.String</span><span class="sxs-lookup"><span data-stu-id="896fd-126">System.String</span></span>

### <span data-ttu-id="896fd-127">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="896fd-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="896fd-128">출력</span><span class="sxs-lookup"><span data-stu-id="896fd-128">OUTPUTS</span></span>

### <span data-ttu-id="896fd-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="896fd-129">System.Boolean</span></span>

## <span data-ttu-id="896fd-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="896fd-130">NOTES</span></span>

## <span data-ttu-id="896fd-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="896fd-131">RELATED LINKS</span></span>

[<span data-ttu-id="896fd-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="896fd-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


