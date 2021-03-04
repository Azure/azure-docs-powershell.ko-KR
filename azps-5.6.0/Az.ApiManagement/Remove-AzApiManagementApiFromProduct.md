---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: af83bb3d6daa11eb62de81378e4e7d3e040b2db4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959051"
---
# <span data-ttu-id="b0bf5-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="b0bf5-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="b0bf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="b0bf5-103">제품에서 API를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf5-103">Removes an API from a product.</span></span>

## <span data-ttu-id="b0bf5-104">구문</span><span class="sxs-lookup"><span data-stu-id="b0bf5-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0bf5-105">설명</span><span class="sxs-lookup"><span data-stu-id="b0bf5-105">DESCRIPTION</span></span>
<span data-ttu-id="b0bf5-106">**Remove-AzApiManagementApiFromProduct** cmdlet은 제품에서 Azure API Management API를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf5-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="b0bf5-107">예제</span><span class="sxs-lookup"><span data-stu-id="b0bf5-107">EXAMPLES</span></span>

### <span data-ttu-id="b0bf5-108">예제 1: 제품에서 API 제거</span><span class="sxs-lookup"><span data-stu-id="b0bf5-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="b0bf5-109">이 명령은 제품에서 지정된 API를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf5-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="b0bf5-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b0bf5-110">PARAMETERS</span></span>

### <span data-ttu-id="b0bf5-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b0bf5-111">-ApiId</span></span>
<span data-ttu-id="b0bf5-112">제품에서 제거할 API의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf5-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="b0bf5-113">-Context</span><span class="sxs-lookup"><span data-stu-id="b0bf5-113">-Context</span></span>
<span data-ttu-id="b0bf5-114">**PsApiManagementContext 를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="b0bf5-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="b0bf5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0bf5-115">-DefaultProfile</span></span>
<span data-ttu-id="b0bf5-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0bf5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0bf5-117">-PassThru</span></span>
<span data-ttu-id="b0bf5-118">이 cmdlet이 성공하거나 그렇지 않은 경우 $True 값을 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf5-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="b0bf5-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="b0bf5-119">-ProductId</span></span>
<span data-ttu-id="b0bf5-120">API를 제거할 제품의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf5-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="b0bf5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0bf5-121">CommonParameters</span></span>
<span data-ttu-id="b0bf5-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b0bf5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0bf5-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0bf5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0bf5-124">입력</span><span class="sxs-lookup"><span data-stu-id="b0bf5-124">INPUTS</span></span>

### <span data-ttu-id="b0bf5-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b0bf5-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b0bf5-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b0bf5-126">System.String</span></span>

### <span data-ttu-id="b0bf5-127">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b0bf5-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b0bf5-128">출력</span><span class="sxs-lookup"><span data-stu-id="b0bf5-128">OUTPUTS</span></span>

### <span data-ttu-id="b0bf5-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b0bf5-129">System.Boolean</span></span>

## <span data-ttu-id="b0bf5-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b0bf5-130">NOTES</span></span>

## <span data-ttu-id="b0bf5-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0bf5-131">RELATED LINKS</span></span>

[<span data-ttu-id="b0bf5-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="b0bf5-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


