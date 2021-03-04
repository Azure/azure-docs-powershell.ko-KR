---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: 748dc399c68a299ef0d567fbd65ec7154061869c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954907"
---
# <span data-ttu-id="5132e-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="5132e-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="5132e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5132e-102">SYNOPSIS</span></span>
<span data-ttu-id="5132e-103">그룹에 제품을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5132e-103">Adds a product to a group.</span></span>

## <span data-ttu-id="5132e-104">구문</span><span class="sxs-lookup"><span data-stu-id="5132e-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5132e-105">설명</span><span class="sxs-lookup"><span data-stu-id="5132e-105">DESCRIPTION</span></span>
<span data-ttu-id="5132e-106">**Add-AzApiManagementProductToGroup** cmdlet은 제품을 기존 그룹에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5132e-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="5132e-107">즉, 이 cmdlet은 제품에 그룹을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="5132e-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="5132e-108">예제</span><span class="sxs-lookup"><span data-stu-id="5132e-108">EXAMPLES</span></span>

### <span data-ttu-id="5132e-109">예제 1: 그룹에 제품 추가</span><span class="sxs-lookup"><span data-stu-id="5132e-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="5132e-110">이 명령은 제품을 기존 그룹에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5132e-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="5132e-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5132e-111">PARAMETERS</span></span>

### <span data-ttu-id="5132e-112">-Context</span><span class="sxs-lookup"><span data-stu-id="5132e-112">-Context</span></span>
<span data-ttu-id="5132e-113">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="5132e-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="5132e-114">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5132e-114">This parameter is required.</span></span>

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

### <span data-ttu-id="5132e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5132e-115">-DefaultProfile</span></span>
<span data-ttu-id="5132e-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5132e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5132e-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="5132e-117">-GroupId</span></span>
<span data-ttu-id="5132e-118">그룹 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5132e-118">Specifies the group ID.</span></span>
<span data-ttu-id="5132e-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5132e-119">This parameter is required.</span></span>

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

### <span data-ttu-id="5132e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5132e-120">-PassThru</span></span>
<span data-ttu-id="5132e-121">passthru</span><span class="sxs-lookup"><span data-stu-id="5132e-121">passthru</span></span>

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

### <span data-ttu-id="5132e-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="5132e-122">-ProductId</span></span>
<span data-ttu-id="5132e-123">제품 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5132e-123">Specifies the product ID.</span></span>
<span data-ttu-id="5132e-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5132e-124">This parameter is required.</span></span>

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

### <span data-ttu-id="5132e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5132e-125">CommonParameters</span></span>
<span data-ttu-id="5132e-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5132e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5132e-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5132e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5132e-128">입력</span><span class="sxs-lookup"><span data-stu-id="5132e-128">INPUTS</span></span>

### <span data-ttu-id="5132e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5132e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5132e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5132e-130">System.String</span></span>

### <span data-ttu-id="5132e-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5132e-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5132e-132">출력</span><span class="sxs-lookup"><span data-stu-id="5132e-132">OUTPUTS</span></span>

### <span data-ttu-id="5132e-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5132e-133">System.Boolean</span></span>

## <span data-ttu-id="5132e-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5132e-134">NOTES</span></span>

## <span data-ttu-id="5132e-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5132e-135">RELATED LINKS</span></span>

[<span data-ttu-id="5132e-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="5132e-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


