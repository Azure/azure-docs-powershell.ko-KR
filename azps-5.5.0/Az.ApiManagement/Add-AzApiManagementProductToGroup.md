---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: a92387392c540c75cfa96ecaf4c4acf026ade9f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205840"
---
# <span data-ttu-id="92d6b-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="92d6b-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="92d6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="92d6b-103">그룹에 제품을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="92d6b-103">Adds a product to a group.</span></span>

## <span data-ttu-id="92d6b-104">구문</span><span class="sxs-lookup"><span data-stu-id="92d6b-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92d6b-105">설명</span><span class="sxs-lookup"><span data-stu-id="92d6b-105">DESCRIPTION</span></span>
<span data-ttu-id="92d6b-106">**Add-AzApiManagementProductToGroup** cmdlet은 기존 그룹에 제품을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="92d6b-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="92d6b-107">즉, 이 cmdlet은 제품에 그룹을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="92d6b-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="92d6b-108">예제</span><span class="sxs-lookup"><span data-stu-id="92d6b-108">EXAMPLES</span></span>

### <span data-ttu-id="92d6b-109">예제 1: 그룹에 제품 추가</span><span class="sxs-lookup"><span data-stu-id="92d6b-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="92d6b-110">이 명령은 기존 그룹에 제품을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="92d6b-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="92d6b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92d6b-111">PARAMETERS</span></span>

### <span data-ttu-id="92d6b-112">-Context</span><span class="sxs-lookup"><span data-stu-id="92d6b-112">-Context</span></span>
<span data-ttu-id="92d6b-113">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="92d6b-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="92d6b-114">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="92d6b-114">This parameter is required.</span></span>

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

### <span data-ttu-id="92d6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d6b-115">-DefaultProfile</span></span>
<span data-ttu-id="92d6b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92d6b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92d6b-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="92d6b-117">-GroupId</span></span>
<span data-ttu-id="92d6b-118">그룹 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="92d6b-118">Specifies the group ID.</span></span>
<span data-ttu-id="92d6b-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="92d6b-119">This parameter is required.</span></span>

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

### <span data-ttu-id="92d6b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92d6b-120">-PassThru</span></span>
<span data-ttu-id="92d6b-121">passthru</span><span class="sxs-lookup"><span data-stu-id="92d6b-121">passthru</span></span>

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

### <span data-ttu-id="92d6b-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="92d6b-122">-ProductId</span></span>
<span data-ttu-id="92d6b-123">제품 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="92d6b-123">Specifies the product ID.</span></span>
<span data-ttu-id="92d6b-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="92d6b-124">This parameter is required.</span></span>

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

### <span data-ttu-id="92d6b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d6b-125">CommonParameters</span></span>
<span data-ttu-id="92d6b-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="92d6b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d6b-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="92d6b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d6b-128">입력</span><span class="sxs-lookup"><span data-stu-id="92d6b-128">INPUTS</span></span>

### <span data-ttu-id="92d6b-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="92d6b-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="92d6b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="92d6b-130">System.String</span></span>

### <span data-ttu-id="92d6b-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="92d6b-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="92d6b-132">출력</span><span class="sxs-lookup"><span data-stu-id="92d6b-132">OUTPUTS</span></span>

### <span data-ttu-id="92d6b-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92d6b-133">System.Boolean</span></span>

## <span data-ttu-id="92d6b-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="92d6b-134">NOTES</span></span>

## <span data-ttu-id="92d6b-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92d6b-135">RELATED LINKS</span></span>

[<span data-ttu-id="92d6b-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="92d6b-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


